lsblk #列出設備訊息
ssh-keygen #生成鑰匙對
eval "$(ssh-agent -s)" #開啟ssh-agent
ssh-add ~/.ssh/key.pem #將key.pem放入快取列表
ssh-copy-id name@<host IP> #將key.pub複製進目標主機的authorized_keys
ansible all -m ping #ping所有主機，與一般的ping不一樣
ssh <host IP> #以ssh與目標host連線
ansible-playbook site.yml #自動部屬nginx網頁
ansible-playbook jinja2.yml #jinja2範例
cat /tmp/jinja2-demo-localhost.md #觀察與原檔區別
ansible-playbook jinja2.yml -e ansible_os_family=RedHat #及時帶入變數進入檔案內
cat /tmp/jinja2-demo-localhost.md #再次觀察
