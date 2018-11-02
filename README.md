# k8s-deployments
kubernetes deployment files

To use: Simply clone the configuration file and modify value as needed. Then apply using kubectl

<table>
    <tr>
        <th>File</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>grafana.yaml</td>
        <td>Installs 1 instance of grafana, mounts NFS path to /var/lib/grafana , exposes web frontend on NodeIP:3000 </td>
    </tr>
    <tr>
        <td>telegraf.yaml</td>
        <td>Installs 1 instance of telegraf, mounts NFS path to /etc/telegraf </td>
    </tr>
    <tr>
        <td>influxdb.yaml</td>
        <td>Installs 1 instance of influxdb, mounts NFS paths to /var/lib/influxdb and /etc/influxdb , exposes frontend on NodeIP:8086 </td>
    </tr>
    <tr>
        <td>jumphost.yaml</td>
        <td>Deploys 3 instances of docker jumphost, exposes ssh frontend on NodeIP:31122 </td>
    </tr>
    <tr>
        <td>nfs-test.yaml</td>
        <td>Tests writing to the NFS mounted volume /mnt</td>
    </tr>
    <tr>
        <td>nfs-volume.yaml</td>
        <td>Template for presenting nfs volume to a deployment </td>
    </tr>
    <tr>
        <td>pms.yaml</td>
        <td>Deploys 1 instance of Plex Media Server container, mounts /config, /transcode, and /data volume via NFS exposes web frontend on NodeIP:32400 </td>
    </tr>
     <tr>
        <td>dashboard-adminuser.yaml</td>
        <td>NOT WORKING: Attempts installation of GUI frontend for kubernetes</td>
    </tr>
     <tr>
        <td>unifi.yaml</td>
        <td>NOT WORKING, possibly L3 adoption only: Installs unifi controller, mounts /unifi via NFS, exposes web and discovery frontend /</td>
    </tr>
    
</table>


unifi.yaml	add port 8080 to unifi
