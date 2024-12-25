# 中文Word 公文模板

主要设置了以下格式：

- 标题
- 副标题
- 标题1
- 标题2
- 标题3
- 页边距
- 页脚页码

配合使用 default.openxml 来输出文件内容

注：不建议使用新版的 Word/WPS 来修改模板文件，使用 zip 解压后修改 style.xml 等文件来实现模板变更。

因为新版的 Word/WPS 已经不再使用命名的样式ID，而是使用了幻数代码，不好识别。Pandoc 好像也识别不出来，它使用的是固定命名的样式ID。

# 使用指令

```sh
pandoc -f gfm -t docx \
    -M toc-title:"目录" \
    --reference-doc=$HOME/.pandoc/templates/reference.docx \
    -o $outfile \
```
