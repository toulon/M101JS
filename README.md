M101JS
======

Mongodb Development class for Javascript

Search for TODO: hw2.3 in users.js.orig to see what they are asking Look in my users.js to see what I added. My code is missing something. I don't want you to do my homework, but just give me a nudge in the right direction. 
I think I am really close but missing something little.
I am not getting any error even in console on Chrome Developer. It only times out and stops.

I added the user tom with password tom and received the following messages
^CMFN-LT-0067:blog toulon$ node app.js 
Express server listening on port 3000
'Successfully inserted: [{"_id":"tom","password":"$2a$10$kEP0qTEnbZqSmetQL9GSPOEhEIQEijL9JTHxsQiw/6Hd.8FrBlT8C"}]'

events.js:71
        throw arguments[1]; // Unhandled 'error' event
                       ^
MongoError: E11000 duplicate key error index: blog.users.$_id_  dup key: { : "tom" }
    at Object.toError (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/utils.js:110:11)
    at /Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/collection.js:345:24
    at Server.Base._callHandler (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/connection/base.js:382:41)
    at Server.connect.connectionPool.on.server._serverState (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/connection/server.js:472:18)
    at MongoReply.parseBody (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/responses/mongo_reply.js:68:5)
    at Server.connect.connectionPool.on.server._serverState (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/connection/server.js:430:20)
    at EventEmitter.emit (events.js:96:17)
    at _connect (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/connection/connection_pool.js:191:13)
    at EventEmitter.emit (events.js:99:17)
    at Socket.exports.Connection.createDataHandler (/Users/toulon/M101JS/Week_2/hw2/hw2-3/blog/node_modules/mongodb/lib/mongodb/connection/connection.js:384:22)

Somewhere I am adding the user again. Hmm... not quite sure where

> db.posts.count()
0
> db.users.find()
{ "_id" : "tom", "password" : "$2a$10$kEP0qTEnbZqSmetQL9GSPOEhEIQEijL9JTHxsQiw/6Hd.8FrBlT8C" }
> 
