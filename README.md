# Cách sử dụng

Link docker image .tar:
https://drive.google.com/file/d/1-1Ln_0MOQm8TnSK2TtA2EoUlzMGJWuSG/view?usp=sharing

### Load docker image

```
docker load < fiba.tar
```

Báo như dưới đây là thành công:
```
Loaded image: fiba:latest
```

Khởi động docker

```
docker run -it fiba:latest
```

Nếu máy server k có giao diện thì dùng tmux để chạy server

### Chạy tmux thứ nhất

```
tmux new -s rasa-server
```

Gõ:
```
rasa run -m 20210411-183030.tar.gz --enable-api --cors "*" --debug
```
Ctrl B D để thoát

### Chạy tmux thứ hai

```
tmux new -s rasa-custom
```

Gõ

```
python3 rasa-custom.py
```

Endpoint:

```
<domain ngrok>/webhooks/rest/webhook
```
