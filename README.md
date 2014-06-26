a little something for load testing nginx+lua websocket performance out of the box.

**how to use**

1. install openresty following the instructions on the openresty site.
2. unpack this repo somewhere
3. from the top-level of the repo, start nginx relative to the pwd: ``nginx -p `pwd`/ -c conf/nginx.conf``
4. make sure `ulimit -n` says something biggish if you want to really load test
5. you're ready to rock:
  * surf to `127.0.0.1:8080/websockets.html` to play with it manually
  * or hit `ws://127.0.0.1:8080/` directly
  * active connection count available at `127.0.0.1:8080/stats` (whenever i get it working)


**etc**

mostly borrowed code, nabbed from
* http://openresty.org/#GettingStarted
and
* https://medium.com/technology-and-programming/websockets-with-openresty-1778601c9e05

see also https://github.com/lipp/lua-websockets for other implementation ideas.

license: whatever licenses the other authors used (idk) + Apache 2 for my changes

![vroooom](http://media.giphy.com/media/rriYfsQZRE9Pi/giphy.gif)
