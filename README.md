# Cách sử dụng

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
tmux new -s ngrok-extend
```

Gõ:
```
./ngrok http 5005
```

Ctrl B D để thoát

### Chạy tmux thứ ba

```
tmux new -s rasa-custom
```

Gõ

```
python3 rasa-custom.py
```
