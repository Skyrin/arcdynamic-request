## Network request wrapper for ArcDynamic services

This function handles batching & caching of ArcDynamic requests. It will can return a promise (default) or invoke a callback, depending on the import.

### Example (promise):

```
import request from 'arcdynamic-request'

request(PATH_TO_API, {
	service: 'cart',
	action: 'store.product.get',
	schema: '[name,sku,price]',
	options: {
		limit: {
			count: 10,
			offset: 0,
		},
	},
}, {
	expires: 1000*60*60,
})
.then(res => /* do something */)
.catch(err => /* handle network error */);

```

### Example (callback):

```
import request from 'arcdynamic-request/request'

request(PATH_TO_API, {
	service: 'cart',
	action: 'store.product.get',
	schema: '[name,sku,price]',
	options: {
		limit: {
			count: 10,
			offset: 0,
		},
	},
}, {
	expires: 1000*60*60,
}, function(err, res){
	if (err) {
		/* handle network error */
	} else {
		/* do something */
	}
})

```