##SphinxAPI for TeaJs##
```javascript
  var sphinx = new (require('sphinxapi')).SphinxClient();

  sphinx.SetServer('127.0.0.1', 9312);
  sphinx.SetConnectTimeout(5);
  sphinx.SetMaxQueryTime(10000);
  sphinx.SetArrayResult(true);
  sphinx.SetMatchMode(sphinx.SPH_MATCH_EXTENDED2);
  sphinx.SetLimits(0, 100);
  
  var results = sphinx.Query('find me', 'index_name');
	
```

To use this API with NodeJS, you should change the "exports.SphinxClient" to the "module.exports" convention, and use relevant Node libraries in require().
