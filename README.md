#dotfiles
$B$3$l$H(Bvim$B4XO"$N;2>H85$r0J2<$K$^$H$a$k(B
- [$BC&=i?4<T$rL\;X$9(BVimmer$B$K%*%9%9%a$7$?$$(BVim$B%W%i%0%$%s$d(B.vimrc$B$N@_Dj(B](http://qiita.com/jnchito/items/5141b3b01bced9f7f48f)
  - $B$3$3$G7G:\$5$l$F$$$k(Bvimrc$B$r$H$j$"$($:40A4$K%Q%/$C$?(B
- [$B$=$m$=$m$7$C$+$j(Bvim$B$r;H$&!#(Bdotfiles$B$N(Bgithub$B4IM}$H(Bvundle$B$NF3F~!#(B](http://holypp.hatenablog.com/entry/20110515/1305443997)
- [NeoBundle$B$NF3F~(B](http://qiita.com/puriketu99/items/1c32d3f24cc2919203eb)
  - $B>e$NFs$D$rAH$_9g$o$;$FF3F~$7$?!#F~NO$7$?%3%^%s%I$O<B:]$K$O0J2<$NDL$j!#(B
```
mkdir ~/dotfiles
cd ~/dotfiles
touch _vimrc #.vimrc$B$N<BBN(B_vimrc$B$N:n@.(B
ln -s ~/dotfiles/_vimrc ~/.vimrc #$B%[!<%`%G%#%l%/%H%j$+$i<BBN$X$N%7%s%\%j%C%/%j%s%/$rD%$k(B
git init
git commit -m 'first commit'
git submodule add https://github.com/Shougo/neobundle.vim ~/dotfiles/vimfiles/bundle/neobundle.vim
git commit -m 'modified vimrc for added neobundle'
git remote add origin https://github.com/r-takahama/dotfiles.git
git push origin HEAD:master
```
- [src refspec master does not match any when pushing commits in git](http://stackoverflow.com/questions/4181861/src-refspec-master-does-not-match-any-when-pushing-commits-in-git)
  - $B%l%]%8%H%j!&%m!<%+%k%G%#%l%/%H%j$N:n@.$r=*$($F!"(B`git push origin mastar`$B$7$h$&$H$7$?:]5/$-$?%(%i!<$KBP=h$9$k$N$KMQ$$$?!#(B
  $BFs$DL\$N2rEz$,;29M$K$J$j!"(B`git push origin HEAD:master`$B$H$7$?$i(Bpush$B$G$-$?!#(B
