# IMG_Spider
用Python3爬取各种网站上的图片


通过二进制图片结尾 '\xd9' 来判断
下载过程中，判断该图片是否为完整图片
同时对于已经下载的图片仍旧判断是否为完整图片 不完整则重新下载
牺牲了一定的性能，但是保证完整性

## 环境

    python3
    所需库:
    requests
    lxml

   

## 目录:
![目录][2]

    .
    ├── AISSaisi                # 爱丝图集
    ├── luyilu                  # 撸一撸图集
    ├── meiyanshe               # 魅妍社图集
    ├── meiyuanguan             # 美媛馆图集
    ├── tuinvlang               # 推女郎图集
    ├── youguo                  # 尤果图集
    ├── README.md               # readme
    ├── seeds_list.txt          # 所有图片url
    ├── image_list.txt          # 所有图集url
    ├── download_imags.py       # 图片下载
    └── download_seeds.py       # 种子下载 

## 启动方式

    下载种子:
    python3 download_seeds.py
    
    自动遍历该网站所有分类，然后遍历各个分类里具体的图集，并保存下url
    
    下载图片:
    默认是 10个进程下载，需要的话，自己进代码里修改
    
    python3 download_images.py
