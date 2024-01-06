## SensorData Docker Compose Files


### Usage

### Install
- home brew
    - `brew install docker`
    - `brew install docker-compose`

### Running
 - `docker-compose config` - checks if the config files are correct
 - `docker-compose up` - starts up the docker-compose containers in foreground
 - `docker-compose -d up` Detached mode runs containers in the background
   - More info here: https://docs.docker.com/engine/reference/commandline/compose_up/

### Stopping
 - `docker-compose stop`

e.g.

<table border="0px">
<tr>docker-compose stop</tr>
<tr>[+] Stopping 2/2</tr>
<tr>✔ Container docker_files-sensor-api-1  Stopped</tr>
<tr> ✔ Container docker_files-sensor-ui-1   Stopped</tr>
</table>

### Logs
 - `docker-compose logs` - shows logs from all services
 - `docker-compose logs <SERVICE NAME>` e.g. `docker-compose logs sensor-ui`
 - `docker-compose logs -f <SERVICE NAME>` tails the log files e.g. `docker-compose logs -f sensor-ui`

### Health
 - `docker-compose ps` - shows the state of running services e.g
   <table>
   <tr>
    <th>NAME</th><th>IMAGE</th><th>COMMAND</th><th>SERVICE</th><th>CREATED</th><th>STATUS</th><th>PORTS</th>
   </tr>
   <tr>
      <td>docker_files-sensor-api-1</td>
      <td>welchie99/dynamo.sensordata:0.0.9-SNAPSHOT-PROD</td>
      <td>"java -jar dynamo.se…"</td>
      <td>sensor-api</td>
      <td>2 hours ago</td>
      <td>Up 5 seconds (health: starting)</td>
      <td>0.0.0.0:80->8080/tcp</td>
   </tr>
   <tr>
      <td>docker_files-sensor-ui-1</td>
      <td>welchie99/sensor-ui:0.0.3-SNAPSHOT</td>
      <td>"docker-entrypoint.s…"</td>
      <td>sensor-ui</td>
      <td>2 hours ago</td>
      <td>Up 5 seconds (health: starting)</td>
      <td>0.0.0.0:3000->3000/tcp</td>
   </tr>
   </table>
