# ServerVM
Graphical Interface for Servers
       
    apt install novnc psmisc x11vnc tigervnc-standalone-server xterm terminator dbus-x11 python-py python3-pip xfce4 xorg -y

# Copy and paste the novnc_proxy into novnc directory:

    wget https://github.com/cristiancmoises/servervm/blob/main/novnc_proxy
    mv novncproxy /usr/share/novnc/utils/

# StartVnc Server
     
     tigervncserver -geometry 1366x768 -xstartup /usr/bin/terminator

# Start NOVNC

    /usr/share/novnc/utils/novnc_proxy --listen 8080 --vnc localhost:5901

# Access Your Server:

     http://SERVERIP:8080/vnc.html
  
# Kill the connection:
    fuser -k 8080/tcp
