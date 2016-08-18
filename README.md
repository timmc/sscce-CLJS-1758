# SSCCE: CLJS browser REPL

**Resolution**: Was missing the body element in the HTML.

```bash
rlwrap java -cp cljs-1.9.216.jar:src clojure.main repl.clj
```

Observe that output stops at `Waiting for browser to connect ...` and
execution pauses.

Navigate to http://localhost:9000/ and observe browser console output:

```
12:9:57.879 log:CrossPageChannel created: ip8qPdw9n3

12:9:57.885 log:createPeerIframe()

Hello, world!

at core.js (line 132)

TypeError: parentElm is null                            
parentElm.appendChild(iframeElm);

at crosspagechannel.js (line 482, col 7)
```

REPL does not appear in terminal.
