# cobblemon_server
Game server deployed on Oracle Cloud

TO DO LIST:

- Edit configs 

Scripts:

# launch server
java -Xmx12G -jar fabric-server-mc.1.20.1-loader.0.17.3-launcher.1.1.0.jar nogui

# Push configs
cd ~/cobblemon_server/server

    # Push config directory
    rsync -av -e "ssh -i ssh-key-2025-11-11.key" \
    ./config/ \
    opc@170.9.225.235:/mnt/cobblemon/server/config/

    # Push defaultconfigs (if you edit those)
    rsync -av -e "ssh -i ssh-key-2025-11-11.key" \
    ./defaultconfigs/ \
    opc@170.9.225.235:/mnt/cobblemon/server/defaultconfigs/

    # Push server.properties
    rsync -av -e "ssh -i ssh-key-2025-11-11.key" \
    ./server.properties \
    opc@170.9.225.235:/mnt/cobblemon/server/

