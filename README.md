# zipboom

## introduce
	
### zip crack based shell,easy to use

## dependence
	
 - unzip  	
 - dict    important！！
 
## coding

    #!/bin/bash
    password=($(cat 123))
    file=IMG_9367.zip
    count=1
    for p in ${password[@]}
    do
    echo "$p($count/${#password[@]})"
    unzip -t -P $p $file >/dev/null 2>&1
    if [ $(echo $?) = "0" ];then
    echo "zip password:$p"
    echo "zip password:$p">zip_password
    exit
    else
    count=$(( count + 1 ))
    continue
    fi
    done



## project

[zipboom版本仓库](https://github.com/blackjack550/zipboom)