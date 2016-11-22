#React Native Event Source
Base On: https://github.com/eohland/EventSource


#install for node,react-native:
    npm install event-source-any-where --save
#install for HTML:
    <script src="https://github.com/Shinichi52/EventSource/blob/master/eventsource.min.js"></script>

# Using On React Navtive, NodeJS (not require in html5)
    require('event-source-any-where'); // for overwrite EventSource

# Using EventSource
```javascript
    let _consumer = new EventSourceEx(YourUrl);

    // add event
    _consumer.addEventListener(YourKey, Callback);
    // remove event
    _consumer.removeEventListener(YourKey, Callback);
    // close connection
    _consumer.close();
```
    
#Example:
```javascript
        require('event-source-any-where');
        this._consumer = new EventSourceEx(CONFIG.urlAuth + CONFIG.serviceConsumer);
        this._consumer.addEventListener("message", this.onReceiveMessage);
        this._consumer.addEventListener("error", this.onConnectError);
```
