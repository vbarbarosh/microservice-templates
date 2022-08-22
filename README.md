Microservices

## User-friendly status

```javascript
const fs = require('fs');
// Treat /dev/fd/3 as a special file for user friendly messages. If no such
// file was open, then nobody cares about such messages.
function user_friendly_status(status)
{
    fs.write(3, `${status}\n`, () => 0);
}
```
