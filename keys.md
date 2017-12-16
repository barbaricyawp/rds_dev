** YELP **
Client ID:
eyE3u4VscKZH4ic4t_G08A
Client Secret:
pcFnK4jgARXJ4EpNRCp8b3Rx5iGAPP32onh4ubn49MjFVbHoWql23JJAazwCKHA8


yelp token

'use strict';
 
const yelp = require('yelp-fusion');
 
const token = yelp.accessToken(eyE3u4VscKZH4ic4t_G08A, pcFnK4jgARXJ4EpNRCp8b3Rx5iGAPP32onh4ubn49MjFVbHoWql23JJAazwCKHA8).then(response => {
  console.log(response.jsonBody.access_token);
}).catch(e => {
  console.log(e);
});

const client = yelp.client(token);
 
client.business('gary-danko-san-francisco').then(response => {
  console.log(response.jsonBody.name);
}).catch(e => {
  console.log(e);
});