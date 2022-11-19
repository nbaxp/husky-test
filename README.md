# husky test

使用 husky + lint-staged,在不依赖编辑器的环境下,在提交时使用 eslint 自动检测并修复暂存区的脚本文件

1. 安装 eslint\husky\lint-staged 作为开发依赖
1. 配置 scripts.prepare
1. 执行 `npm run prepare`
1. 添加 hook `npx husky add .husky/pre-commit "npx --no-install lint-staged"`
1. 配置 lint-staged 节点

注意:

1. exlint 的 --fix 参数要放到最后
1. lint-staged 必须写明文件类型,使用 * 会对每个文件执行命令
1. lint-staged 只对暂存区的文件起效,提交时要注意是否要提交的文件都已暂存

详见 package.json
