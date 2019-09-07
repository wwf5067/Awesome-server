# Awesome-server
## 1 Run RSShub on server
`https://docs.rsshub.app/install/`
## 2 Run ttrss on server
`https://ttrss.henry.wang/zh/
`
### 2.1 mercury
`docker run -p 3002:3000 -d wangqiru/mercury-parser-api`

### 2.2 opencc
`docker run -d -p 3001:3000 --restart=always wangqiru/opencc-api-server`

## 3 Run qq-telegram on server
### 3.1 Method 1
`https://milkice.me/2018/09/17/efb-how-to-send-and-receive-messages-from-qq-on-telegram/`
### 3.2 Method 2
`https://github.com/Earth-Online/efb-qq-coolq-docker`
### 3.3 Config
`cat ~/.ehforwarderbot/profiles/default/milkice.qq/config.yaml `

Client: CoolQ \
CoolQ: \
        type: HTTP \
        access_token: ac0f790e1fb74ebcaf45da77a6f9de47 \
        api_root: http://127.0.0.1:5700/ \
        host: 127.0.0.1 \
        port: 8000 \
        is_pro: true 

`run command`

docker run -ti --rm --name cqhttp-test --net="host" \
     -v $(pwd)/coolq:/home/user/coolq      \
     -p 9000:9000                          \
     -p 5700:5700                          \
     -e VNC_PASSWD=12345678                \
     -e COOLQ_PORT=5700                    \
     -e COOLQ_ACCOUNT=851202772              \
     -e CQHTTP_POST_URL=http://127.0.0.1:8000    \
     -e CQHTTP_SERVE_DATA_FILES=yes       \
     -e CQHTTP_ACCESS_TOKEN=ac0f790e1fb74ebcaf45da77a6f9de47  \
     -e CQHTTP_POST_MESSAGE_FORMAT=array   \
     -e COOLQ_URL="http://dlsec.cqp.me/cqp-tuling"   \
     richardchien/cqhttp:latest

### 3.4 Instruction
`https://www.moerats.com/archives/931/`

## 4 Run wechat-telegram on server
`https://github.com/mikubill/efb-wechat-docker`

### 4.1 Instruction
`https://www.moerats.com/archives/931/`

## Run server-monitor on server
`https://github.com/NavePnow/server-telegram`


