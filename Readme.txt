33 LIFE-CHANGING HACKS - https://www.youtube.com/watch?v=jqaUcIk-Maw
	01.牙膏 VS 輕微燙傷
	02.去耳屎 (ear candle耳燭療法)-東森新說是騙人了
	03.被打熊貓眼 VS (1/2杯 rubbing alcohol+1杯 dish soap)
	04.驅趕蚊子 VS (檸檬+丁香)
	05.牙痛 VS (鹽+胡椒+水)
	06.口紅+透明無痕膠帶 偷取指紋 解鎖手機 [start 8:56]
	07.電鑽自製簡易吸塵器 [start 12:46]

GIT 簡易指令教學 - https://mp.weixin.qq.com/s/iIZNynZFKDMcnXZPfx2iqA
	01.msysgit是 windows版
	02.利用BAT建立版本庫(啟用 git bash)
		cd D:
		cd 00_GitHub
		cd git-bat-test
		pwd
		git init #變成 倉庫了
		#手動新增 readme.txt 内容如下：11111111
		git add readme.txt #添加到暂存区里面去
		git commit -m 'add readme.txt' #提交檔案加上對應註解
		git status #来查看是否还有文件未提交
		#但是我现在继续来改下readme.txt内容，比如我在下面添加一行2222222222内容
		git status #来查看是否还有文件未提交
		git diff readme.txt # 查看異動差異
		#提交修改和提交文件是一样的2步(第一步是git add 第二步是：git commit)。
		git add readme.txt
		git commit -m 'add readme.txt-2222222222'
		#但是我现在继续来改下readme.txt内容，比如我在下面添加一行3333333333333内容
		git add readme.txt
		git commit -m 'add readme.txt-3333333333333'
		git log # 查看紀錄
		git log --pretty=oneline # 查看紀錄-簡潔資訊版
		#倒退版本
		git reset --hard HEAD^ #那么如果要回退到上上个版本只需把HEAD^ 改成 HEAD^^ 以此类推
		#git reset --hard HEAD~100 #倒退到前100个版本
		cat readme.txt #檢查倒退結果
		#有3333333333333的内容要如何恢复呢
		git reflog #取得過往紀錄
			#420ec03 HEAD@{0}: reset: moving to HEAD^
			#71b51b2 HEAD@{1}: commit: add readme.txt-3333333333333
			#420ec03 HEAD@{2}: commit: add readme.txt-2222222222
			#2ce498e HEAD@{3}: commit (initial): add readme.txt
		git reset --hard 71b51b2
		cat readme.txt #檢查還原結果
		#我想直接想使用撤销命令该如何操作呢？首先在做撤销之前，我们可以先用 git status 查看下当前的状态
		git status
		#可以发现，Git会告诉你，git checkout -- file 可以丢弃工作区的修改
		git checkout -- readme.txt
		#假如我现在版本库目录添加一个文件b.txt,然后提交