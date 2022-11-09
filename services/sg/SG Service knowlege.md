# src/client/service.rs
This seems to be the location for every service and its reference in code. it shows that the current services that the most up to date version of our xombie has
- Presence
- Matchmaking
- Terms of Use

Matchmaking is a weird one as it is not working at all on Goplex Live, we are looking into this but we dont know whats wrong with it.
User Account Creation has a ForwardTCP which is probably in place for the 4 green dots and connections working.
We are also looking into UAC and everything for Goplex Live.

I am wondering if i attach the same forwarder, will that help improve our list of potentially working games? no. but it changed a ton of errors to "Xbox Live is not responding"

# src/client/service/matchmaking.rs
This one is a strange one. its all there, except a few TODO's but it should in theory work. but not a single game on Goplex Live can matchmake. all of them return errors. I have a few ideas im going to perform in order to get a larger idea on how the service works and how we can provide matchmaking.

We are looking into this as a high priority for Goplex Live. this is needed in order to even use the service the way it is intended.

```xombie-sg-1       | 2022-11-09T18:45:42.619Z ERROR [sg::client::service::matchmaking] Unknown search request title_id, procedure_index tuple Search { header: SearchHeader { total_length: 104, title_id: 1229389860, procedure_index: 1, client_address: Addr { addr: InAddr([10, 0, 2, 15]), addr_online: InAddr([86, 140, 129, 50]), port_online: 524, enet: 00:50:f2:e5:cf:ab, online: [10, 0, 0, 100, 0, 2, 0, 0, 170, 169, 163, 116, 56, 245, 154, 249, 0, 0, 0, 0] }, num_users: 1, flags: 0, num_attributes: 3 }, attributes: [SearchAttribute { tag: 0, kind: Integer(0) }, SearchAttribute { tag: 0, kind: Integer(0) }, SearchAttribute { tag: 0, kind: Integer(100) }] }```
The error provided when matchmaking on Unreal Championship.

Seems to be searching for the titleID but we dont know where these are stored.
