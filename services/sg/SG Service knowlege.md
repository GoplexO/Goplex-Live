# src/client/service.rs
This seems to be the location for every service and its reference in code. it shows that the current services that the most up to date version of our xombie has
- Presence
- Matchmaking
- Terms of Use

Matchmaking is a weird one as it is not working at all on Goplex Live, we are looking into this but we dont know whats wrong with it.
User Account Creation has a ForwardTCP which is probably in place for the 4 green dots and connections working.
We are also looking into UAC and everything for Goplex Live.

I am wondering if i attach the same forwarder, will that help improve our list of potentially working games? I will answer that soon.

# src/client/service/matchmaking.rs
This one is a strange one. its all there, except a few TODO's but it should in theory work. but not a single game on Goplex Live can matchmake. all of them return errors. I have a few ideas im going to perform in order to get a larger idea on how the service works and how we can provide matchmaking.

We are looking into this as a high priority for Goplex Live. this is needed in order to even use the service the way it is intended.
