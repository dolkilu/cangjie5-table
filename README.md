# cangjie5-table

## Credits

[倉頡之友](https://www.chinesecj.com/forum/forum.php?mod=viewthread&tid=195320)

[Jackchows/Cangjie5 倉頡五代補完計劃](https://github.com/Jackchows/Cangjie5)

## Files
`cj5-13053-default.txt` :  倉頡之友 五倉繁體

`cj5-20902.txt`:  倉頡之友 五倉通用 

`cj5-90000.txt`:  倉頡之友 五倉世紀

`cj5-13053-modified.txt` : 五倉繁體 + 部份五倉通用 

`cangjie5.main-default.dict` :  cangjie5.main.dict from fcitx5 

`cangjie5.main.dict` : `cj5-13053-modified.txt` -> fcitx5 format



## How to

1. Install `libime`

	Arch

		sudo pacman -S libime

	Debian

		sudo apt install libime-bin

2. 
	Fcitx5 tables location  `/usr/share/fcitx5/table`

	User's table location `~/.local/share/fcitx5/table`

3. Backup the default table by copying or exporting them. 

4. Converting from .dict to .txt


		libime_tabledict -d /usr/share/fcitx5/table/cangjie5.main.dict cangjie5-default.txt


6. Modify the table to your own preference

7. Ensure your table's format is correct by comparing the first few lines of `fcitx5's default table`

8. Converting from .txt to .dict

		libime_tabledict your-table.txt cangjie5.main.dict

10. Overwrite `.dict` with `sudo`

11. Restart fcixt5
