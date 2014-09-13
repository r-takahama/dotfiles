#dotfiles
## Usage
```
cd ~/
git clone add https://github.com/r-takahama/dotfiles.git
cd ~/dotfiles/
sh dotfilesSetup.sh
```

## Memo
これとvim関連の参照元を以下にまとめる
- [脱初心者を目指すVimmerにオススメしたいVimプラグインや.vimrcの設定](http://qiita.com/jnchito/items/5141b3b01bced9f7f48f)
  - ここで掲載されているvimrcをとりあえず完全にパクった
- [そろそろしっかりvimを使う。dotfilesのgithub管理とvundleの導入。](http://holypp.hatenablog.com/entry/20110515/1305443997)
- [NeoBundleの導入](http://qiita.com/puriketu99/items/1c32d3f24cc2919203eb)
  - 上の二つを組み合わせて導入した。入力したコマンドは実際には以下の通り。
```
mkdir ~/dotfiles
cd ~/dotfiles
touch _vimrc #.vimrcの実体_vimrcの作成
ln -s ~/dotfiles/_vimrc ~/.vimrc #ホームディレクトリから実体へのシンボリックリンクを張る
git init
git commit -m 'first commit'
git submodule add https://github.com/Shougo/neobundle.vim ~/dotfiles/vimfiles/bundle/neobundle.vim
git commit -m 'modified vimrc for added neobundle'
git remote add origin https://github.com/r-takahama/dotfiles.git
git push origin HEAD:master
```
- [src refspec master does not match any when pushing commits in git](http://stackoverflow.com/questions/4181861/src-refspec-master-does-not-match-any-when-pushing-commits-in-git)
  - レポジトリ・ローカルディレクトリの作成を終えて、`git push origin mastar`しようとした際起きたエラーに対処するのに用いた。
  二つ目の解答が参考になり、`git push origin HEAD:master`としたらpushできた。
