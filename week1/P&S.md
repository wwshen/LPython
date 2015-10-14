####P1 新书编辑后无法发布
    缘起：创建新书时选择了github模板，而非basic模板
    表现：编辑好文字保存后，再回到dashboard，始终提示我的书没有发布。
        另外github模板下，我也不会写table of contents，每次尝试输入，都被认为没有输入valid ref
    解决：重新创建，并选择basic模板。
    探究：
        1）github模板和basic模板的起始文件有差异。basic模板设置了一些基本文件，如gitignore。github模板完全靠自己架设。
        是否是缺少gitignore导致电子书无法发布呢？我现在说不上来。因为我现在的这个版本也没有gitignore（不知道是不是被我误删-_-），但是发布是可以的。
        2）格式设置不对。原电已删，无从考证。
    下一步：可以再次尝试github模板。
关于[gitignore](https://help.github.com/articles/ignoring-files/)：If you create a file in your repository named .gitignore, Git uses it to determine which files and directories to ignore, before you make a commit.
####P2 插入图片不能正确显示及相关问题
    缘起：编辑文字过程中使用tab作为每段起始（首行tab后，每行会自动tab）
    表现：插入图片发现仅显示文字编码，如![xxx](xxx.jpg)。
    解决：行首去掉tab。示范如下：1：行首无tab 2：行首有tab
1：哈哈哈![wave](wave.gif)

    2：哈哈哈![wave](wave.gif)
    
    探究：编辑的时候加上tab，文件预览中可以看见，相关段落的文字有浅色灰框框住，而且如文字很长，会有拖动条出现。且加tab的文字与顶格写的文字字体不同。提示tab后的文字是特殊性质（纯文本）的文字。在tab后的文字里使用文字修饰的命令都不管用，如*斜体*，**粗体**等。
         而顶格写的文字可以被各种命令修饰。但顶格写的文字在编辑界面enter分行后，实际网页显示并不分行，需要再加一个enter。
         下面把这两段文字用顶格写的方式再重复一遍。

探究：编辑的时候加上tab，文件预览中可以看见，相关段落的文字有浅色灰框框住，而且如文字很长，会有拖动条出现。且加tab的文字与顶格写的文字字体不同。提示tab后的文字是特殊性质（纯文本）的文字。在tab后的文字里使用文字修饰的命令都不管用，如*斜体*，**粗体**等。
而顶格写的文字可以被各种命令修饰。但顶格写的文字在编辑界面enter分行后，实际网页显示并不分行，需要再加一个enter。
####P3 创建新的md文档
    缘起：因为windows的习惯，创建新文档时没有加后缀
    表现：发现格式不对，无法显示。
    解决：每个md文档在命名时都应该加上后缀。
####P4 电子书更新失败
    缘起：本来以为是网络问题，但今早一再出现，发现可能还是格式问题。
    表现：反复提示更新失败。查看具体信息，显示的最后一行为未找到README.MD。
        打开编辑界面，我的table of Contents里有两个Introduction。
        点击第一个Introduction，立即跳出需要添加文件READMEMD.md的对话框（因我已有一个readme.md）。
        这个Introduction无法手动删除。
        在SUMMARY.md中删除第一个introduction，依然无法发布。
    解决：1）在SUMMARY.md中删除第一个introduction
         2）把files tree中的readme.md改成README.md
         随即首个introduction自动合并消失。
    探究：看来跟文件的大小写有密切关系。该大小的时候千万不能偷懒小写。