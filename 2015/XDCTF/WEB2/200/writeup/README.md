首先题目提示了git，进入页面后发现有.git目录，不过403，根据.git目录的惯例爬文件，不过HEAD里面没什么东西，后来看到tag1.0之类的字样，就把refs/tags下面的文件拿来，根据hash去objects里面抓文件，拿来后扔zlib里解压，发现是一个树节点，依次把里面提到的objects都取来后在index页面里发现flag