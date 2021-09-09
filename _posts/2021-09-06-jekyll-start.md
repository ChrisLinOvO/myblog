---
title: Jekyll(1)-環境安裝
author: ChrisLin
layout: post
---
<h2>在Github使用Jekyll&SEO(1)  Ruby & Jekyll安裝</h2>

# 1.macOS 使用Homebrew安裝環境  *[參考連結](https://jekyllrb.com/docs/installation/macos/){:target="_blank"}* 
* 安裝 Homebrew
```js
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
* 安裝 Ruby 
```js
# Install Ruby
brew install ruby
```
* 將 brew ruby​​ 和 gems 路徑添加到您的 shell 配置中
```js
# If you're using Zsh
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH"' >> ~/.zshrc
# If you're using Bash
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH"' >> ~/.bash_profile
# Unsure which shell you are using? Type
echo $SHELL
``` 
* 重新啟動您的終端並檢查您的 Ruby 設置
```js
which ruby
# /usr/local/opt/ruby/bin/ruby
ruby -v
ruby 3.0.0p0 (2020-12-25 revision 95aff21468)
``` 

# 2.安裝 bundler 和 jekyll gems
```js
gem install --user-install bundler jekyll
```

# 3.創立Jekyll專案並cd帶該目錄中
```js
jekyll new myblog
cd myblog
```

# 4.執行專案
* 第一次用
```js
bundle exec jekyll serve 
```
* 若Jekyll 服務在 Ruby 3.0 上失敗 缺少 webrick *[參考連結](https://github.com/github/pages-gem/issues/752){:target="_blank"}* 
```js
bundle add webrick  
```
* 之後都用
```js
jekyll serve
```
* 本地端開啟
```js
瀏覽到http://localhost:4000
```

