# zipboom

## introduce
	
### zip crack based shell,easy to use

## dependence
	
 - unzip  	
 - dict    important！！
 
## coding

    #!/bin/sh
    password=$(cat all_password)
    file=jiedaibao1.zip
    for p in $password
    do
    echo "$p"
    unzip -t -P $p $file >/dev/null 2>&1
    if [ $(echo $?) = "0" ];then
    echo "zip password:$p"
    echo "zip password:$p">zip_password
    exit
    else
    continue
    fi
    done


## project

[zipboom版本仓库](https://github.com/blackjack550/zipboom)