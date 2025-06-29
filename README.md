lsblk #列出設備訊息<br>
ssh-keygen #生成鑰匙對<br>
eval "$(ssh-agent -s)" #開啟ssh-agent<br>
ssh-add ~/.ssh/key.pem #將key.pem放入快取列表<br>
ssh-copy-id name@<host IP> #將key.pub複製進目標主機的authorized_keys<br>
ansible all -m ping #ping所有主機，與一般的ping不一樣<br>
ssh <host IP> #以ssh與目標host連線<br>
ansible-playbook site.yml #自動部屬nginx網頁<br>
ansible-playbook jinja2.yml #jinja2範例<br>
cat /tmp/jinja2-demo-localhost.md #觀察與原檔區別<br>
ansible-playbook jinja2.yml -e ansible_os_family=RedHat #及時帶入變數進入檔案內<br>
cat /tmp/jinja2-demo-localhost.md #再次觀察<br>
