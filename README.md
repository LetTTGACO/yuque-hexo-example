# yuque-hexo配置示例文件

# 如何设置环境变量
## 本地调试
本地调试时可以在package.json中使用dotenv来指定.env文件，然后就可以把相关环境变量写在本地即可。
```
"scripts": {
  "yuque:sync": "dotenv -e .env yuque-hexo sync",
},
```
在根目录新建.env文件，并写入以下内容，如果不使用图床服务，SECRET_ID和SECRET_KEY可以不用配置。
```
YUQUE_TOKEN=xxx
SECRET_ID=xxx
SECRET_KEY=xxx
```
> ⚠️ 注意 ⚠️ 一定不要把`.env`文件提交到线上仓库，并将`.env`加入到`.gitignore`

## 线上部署
线上部署时，如果使用github action进行部署，则可以使用自带的secret来配置环境变量

# 图床服务配置示例
## 腾讯云图床
```
"yuqueConfig": {
    "postPath": "source/_posts",
    "baseUrl": "https://www.yuque.com/api/v2",
    "lastGeneratePath": "./last-generate-timestamp.txt",
    "login": "1874w",
    "repo": "yuque-hexo-demo",
    "onlyPublished": true,
    "onlyPublic": true,
    "imgCdn": {
      "concurrency": 0,
      "imageBed": "cos",
      "enabled": true,
      "bucket": "image",
      "region": "ap-guangzhou",
      "prefixKey": "blog-images"
    }
  }
```
## 阿里云图床
```
"yuqueConfig": {
    "postPath": "source/_posts",
    "baseUrl": "https://www.yuque.com/api/v2",
    "lastGeneratePath": "./last-generate-timestamp.txt",
    "login": "1874w",
    "repo": "yuque-hexo-demo",
    "onlyPublished": true,
    "onlyPublic": true,
    "imgCdn": {
      "concurrency": 0,
      "imageBed": "oss",
      "enabled": true,
      "bucket": "test-letttgaco",
      "region": "oss-cn-shenzhen",
      "prefixKey": "blog-images"
    }
  }
```
## 七牛云图床
```
"yuqueConfig": {
    "postPath": "source/_posts",
    "baseUrl": "https://www.yuque.com/api/v2",
    "lastGeneratePath": "./last-generate-timestamp.txt",
    "login": "1874w",
    "repo": "yuque-hexo-demo",
    "onlyPublished": true,
    "onlyPublic": true,
    "imgCdn": {
      "concurrency": 0,
      "imageBed": "qiniu",
      "enabled": true,
      "bucket": "test-letttgaco",
      "region": "Zone_z2",
      "host": "https://qiniu.1874.cool",
      "prefixKey": "blog-images"
    }
  }
```
## Github图床
```
"yuqueConfig": {
    "postPath": "source/_posts",
    "baseUrl": "https://www.yuque.com/api/v2",
    "lastGeneratePath": "./last-generate-timestamp.txt",
    "login": "1874w",
    "repo": "yuque-hexo-demo",
    "onlyPublished": true,
    "onlyPublic": true,
    "imgCdn": {
      "concurrency": 1,
      "imageBed": "github",
      "enabled": true,
      "bucket": "LetTTGACO",
      "host": "cdn.jsdelivr.net",
      "prefixKey": "blog-images"
    }
  }
```
## 又拍云图床
```
"yuqueConfig": {
    "postPath": "source/_posts",
    "baseUrl": "https://www.yuque.com/api/v2",
    "lastGeneratePath": "./last-generate-timestamp.txt",
    "login": "1874w",
    "repo": "yuque-hexo-demo",
    "onlyPublished": true,
    "onlyPublic": true,
    "imgCdn": {
      "concurrency": 0,
      "imageBed": "upyun",
      "enabled": true,
      "bucket": "letttgaco",
      "host": "https://upyun.1874.cool",
      "prefixKey": "blog-images"
    }
  }
```
