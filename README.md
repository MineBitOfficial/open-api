# MineBit APIs

### General Descriptions for All Endpoints

* All endpoints will return as in json format
* The return values of all endpoints will include but not limited to :
```json
{
    "status"   : "success",
    "err_no"   : 0,
    "msg"      : "success",
    "timestamp": 1543402251708,
}
```
```status```:    

Status | Description       
------------ | ------------   
success | Successful request    
fail | failed request    

```err_no```:        
  
err_no | Description   
------------ | ------------    
99999 | Signature not match      
99998 | Expired signature     
99997 | Missing parameters     
99996 | unauthorized accesskey    
99995 | Unexpected parameters     
99994 | Unsupported parameter type    
99993 | Request timeout      
99992 | Reqeust too frequently     


```msg```:       
Response message         

```timestamp```:          


### Base URL
* http://api.minebit.com/openapi

### Limits

* All endpoints can not be requested over 60 times per minute      

### Parameters

* Parameters can be passed by either GET method or POST    method      

### Public Endpoints

<details><summary>Exchange information</summary>

    /openapi/v1/market/exchangeInfo    

Get exchange general information    

Parameters:
```
NO PARAMETERS REQUIRED
```

Responses:
```
{
    "timezone": "UTC",
    "serverTime": 1543413226042,
    "exchangeFilters": [],
    "symbols": [{
        "symbol": "ETH_BTC",
        "status": "TRADING",
        "baseAsset": "ETH",
        "quoteAsset": "BTC",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00280266",
            "maxPrice": "0.28026610",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "ELF_BTC",
        "status": "TRADING",
        "baseAsset": "ELF",
        "quoteAsset": "BTC",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00000294",
            "maxPrice": "0.00029350",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "MBT_ETH",
        "status": "TRADING",
        "baseAsset": "MBT",
        "quoteAsset": "ETH",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00001140",
            "maxPrice": "0.00114000",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "ELF_ETH",
        "status": "TRADING",
        "baseAsset": "ELF",
        "quoteAsset": "ETH",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00010448",
            "maxPrice": "0.01044790",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "WTC_ETH",
        "status": "TRADING",
        "baseAsset": "WTC",
        "quoteAsset": "ETH",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00100077",
            "maxPrice": "0.10007680",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "LRC_ETH",
        "status": "TRADING",
        "baseAsset": "LRC",
        "quoteAsset": "ETH",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00003300",
            "maxPrice": "0.00330020",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "KST_ETH",
        "status": "TRADING",
        "baseAsset": "KST",
        "quoteAsset": "ETH",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "0.00000771",
            "maxPrice": "0.00077050",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "BTC_USDT",
        "status": "TRADING",
        "baseAsset": "BTC",
        "quoteAsset": "USDT",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "418.30400000",
            "maxPrice": "41830.40000000",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }, {
        "symbol": "ETH_USDT",
        "status": "TRADING",
        "baseAsset": "ETH",
        "quoteAsset": "USDT",
        "baseAssetPrecision": 8,
        "quotePrecision": 8,
        "orderTypes": ["LIMIT"],
        "icebergAllowed": false,
        "filters": [{
            "minPrice": "11.71600000",
            "maxPrice": "1171.60000000",
            "filterType": "PRICE_FILTER",
            "tickSize": "0.00000100"
        }, {
            "stepSize": "0.00000100",
            "filterType": "LOT_SIZE",
            "maxQty": "50000000.00000000",
            "minQty": "0.01000000"
        }]
    }],
    "rateLimits": [{
        "rateLimitType": "REQUEST_WEIGHT",
        "interval": "MINUTE",
        "intervalNum": 1,
        "limit": 1200
    }, {
        "rateLimitType": "ORDERS",
        "interval": "SECOND",
        "intervalNum": 1,
        "limit": 10
    }, {
        "rateLimitType": "ORDERS",
        "interval": "DAY",
        "intervalNum": 1,
        "limit": 100000
    }]
}
```
</details>

<details><summary>Recent Trading Records</summary>

    /openapi/v1/market/transaction_record

Get recent trading records, 100 at most.

Parameters:
``` 
{
    "symbol" : "btc_usdt", // market pair, separate by "_"
    "size"   : "10", // optional, 1-100
}
```

Responses:
```
{
    "status": "success",
    "ch": "market.btc_usdt.trade.detail",
    "err_no": 0,
    "msg": "success",
    "timestamp": 1543402521132,
    "data": [
        {
            "timestamp": 1543402413,
            "price": 4090.4,
            "amount": 0.0276,
            "side": "sell"
        }
    ]
}
```
</details>

<details><summary>All Market Pairs</summary>

    /openapi/v1/market/products

Get all available market pairs.

Parameters:
```
NO PARAMETERS REQUIRED
```

Responses:
```
{
    "status":"success",
    "err_no":0,
    "msg":"success",
    "data":[  // entry list 
        {  
            "id":"ETH_BTC",     // market pair 
            "fromSymbol":"ETH", // major part
            "toSymbol":"BTC"    // minor part
        },
    ],
}
```

</details>

<details><summary>24 Hours Volume for All Market Pairs</summary>

    /openapi/v1/market/all_quote
Get volumes of all market pairs in pass 24 hours

Parameters:
```
NO PARAMETERS REQUIRED
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg"   : "success",
    "data": [
        {
            "id": 1534636800,
            "close": 0.06,
            "vol": 1074.4,
            "amount": 1074.4,
            "count": 559,
            "high": 22,
            "low": 0.04,
            "open": 9,
            "symbol": "eth_btc"
        }
    ]
}
```
</details>

<details><summary>Kline/Candlestick Data</summary>
    
    /openapi/v1/market/history
Get Klines or candlestick charts

Parameters:
```
{
    "symbol" : "btc_usdt", //market pair, get all available pair
    "period" : "1min", // available periods 1min, 5min, 15min, 30min, 60min, 1day, 1mon, 1week, 1year
    "size"   : "10", // 1 - 300
}
```

Responses:
```
{
    "status": "success",
    "ch": "market.btc_usdt.kline.1min", // will not be used
    "err_no": 0,
    "msg": "success",
    "timestamp": 1543412353359,
    "data": [                             // entry list 
        {
            "id"     : 1543415340 // timestamp
            "close"  : 4196.16,   // closing price
            "vol"    : 2480.6624, // total price of transactions as last part of pair,usdt in this case
            "amount" : 0.5909,    // total amount of transactions as first part of pair, btc in this case
            "count"  : 8,         // amount of complete transactions 
            "high"   : 4199.8,    // highest price
            "low"    : 4195.96,   // lowest price
            "open"   : 4199.8     // openning price
        }
    ]
}
```
</details>

<details><summary>Recent trades list</summary>

    /openapi/v1/market/transaction_record
Returns the entries of successful transactions by specific market pair

Parameters:
```
{
    "symbol" : "btc_usdt", //market pair, get all available pair
    "size" : "10", // 1 - 100
}
```

Responses:
```
{
    "status": "success", // return "fail" if request failed
    "ch": "market.btc_usdt.trade.detail", // will not be used
    "err_no": 0, // 0 for successful request and 99992 for request too frequently
    "msg": "success", // return message
    "timestamp": 1543402521132, //Responses time
    "data": [ // entry list of transactions
        {
            "timestamp": 1543402413, // when this transaction was finished
            "price": 4090.4, // the price of this transaction as in last part of pair, usdt in this case
            "amount": 0.0276, // the amount of the first part of this pair, btc in this case
            "side": "sell" // sell for a selling transaction and buy for a buying transaction
        }
    ]
}
```

</details>

<details><summary>Markets Summary</summary>

    POST /openapi/v1/market/quote

Get daily markets summary

Parameters:
```
{
    "symbol" : "eth_btc"
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "success",
    "data": [
        {
            "close": 9,
            "vol": 81.355,
            "amount": 81.355,
            "count": 69,
            "high": 13,
            "low": 0.000001,
            "open": 0.01,
            "symbol": "eth_btc",
            "buy": 6,
            "sell": 9
        }
    ]
}
```

</details>

<details><summary>Depth</summary>

    openapi/v1/market/depth

Depth

Parameters:
```
{
    "symbol" : "eth_btc",
    "type"   : "1", 
    "side"   : "0"
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "get depth success",
    "data": {
        "depth": {
            "buy": [
                {
                    "price": 0.05,
                    "amount": 9.807
                }
            ],
            "sell": [
                {
                    "price": 0.1,
                    "amount": 1.029
                }
            ]
        }
    }
}
```



</details>

### Private Endpoints

For private endpoints:
You have to have the corresponding accesskey and secretkey,
and the following steps are necessary.

```
 a. Arrange all request parameters in alphabetical order by request parameter names:Key=value&key=value&...key=value. For example, sort the strings atong=1, mrong=2, crong=3 as: arong=1, crong=3, mrong=2. Then merge the parameters into follows: arrhong=1&crong=3&mrong=2. FILES parameters do not participate in merging.
b. Add secretkey to the end of the parameter string ,then encrypt the string with MD5. The encrypted string needs to be uppercase.just get the signature now.Merge &signature=signature with the parameters string derived from a.
```

call api：https://api.minebit.com/openapi/v1/trade/order  
request method：post    
request parameter：    
accesskey=app_key    
signature=BCC7C71CF93F9CDBDB88671B701D8A35    
timestamp=1534591800543    
parameter1=value1    
parameter2 =value2    
…….    

Note：The secretkey is only used for encryption. Please do not use it in the request parameters in case of data leakage.    
As above,the timestamp will be used to verify whether or not the request is expired.So even if the request link is been taken entirely,the data will be secure.    

<details><summary>Unexcuted Orders Detail</summary>

    POST /openapi/v1/trade/order_info

Get unexcuted orders detail

Parameters:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "order_id"  : "order id",
    "symbol"    : "trading pair"
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "get order detail success.",
    "data": {
        "error": null,n
        "result": {
            "amount": "0.05",
            "addtime": 1534322265304,
            "deal_amount": "0",
            "order_id": 1888,
            "avg_price": "0.1",
            "status": 0,
            "type": 1,
            "side": 1,
            "symbol": "eth_btc"
        },
        "id": 1534336146847
    }
}
```


</details>

<details><summary>Query Unexcuted Orders</summary>

    POST /openapi/v1/trade/pending_orders

query unexcuted orders

Parameters:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "order_id"  : "order id",
    "symbol"    : "trading pair",
    "offset"    : 0, 
    "limit"     : 10, // how much entries will be return
    "type"      : 1,  // 1 limit order, 2 market order (optional)
    "side"      : 0,  // 0=>all, 1=>for buying, 2=>for selling 
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "get pending orders success",
    "data": [
        {
            "side":2,
            "addtime": 1534265644610,
            "type": 1,
            "price": "0.1",
            "deal_amount": "0e-16",
            "order_id": 1867,
            "amount": "0.12",
            "symbol": "eth_btc"
        }
    ]
}
```

</details>



<details><summary>Make Order</summary>

    POST /openapi/v1/trade/order

Make order

Parameter:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "price"     : "price",
    "amount"    : "amount",
    "symbol"    : "trading pair",
    "type"      : 1,  // 1 limit order, 2 market order (temporary disabled)
    "side"      : 0,  // 0=>all, 1=>for buying, 2=>for selling 
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "put order success",
    "data": {
        "error": null,
        "result": {
            "order_id": 116783
        },
        "id": 1534590591
    }
}
```

</details>



<details><summary>Cancel Order</summary>

    POST /openapi/v1/trade/cancel_order

Cancel order by order id

Parameter:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "order_id"  : "order id",
    "symbol"    : "trading pair",
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "put order success",
    "data": {
        "error": null,
        "result": {
            "order_id": 116783
        },
        "id": 1534590591
    }
}
```

</details>


<details><summary>Get Balance</summary>

    POST /openapi/v1/userasset/balances

Get balance

Parameter:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "coin"      : "coin",
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "get user total balance success.",
    "data": [
        {
            "coinname": "eos",
            "coin_amount": "0",
            "coin_trade_frozen": "0"
        },
    ]
}
```

</details>



<details><summary>Get Finished Orders</summary>

    POST /openapi/v1/trade/finished_orders

Get Finished_orders

Parameter:
```
{
    "accesskey" : "access key",
    "timestamp" : "timestamp",
    "signature" : "signature",
    "order_id"  : "order id",
    "symbol"    : "trading pair",
    "offset"    : 0, 
    "limit"     : 10, // how much entries will be return
    "type"      : 1,  // 1 limit order, 2 market order (optional)
    "side"      : 0,  // 0=>all, 1=>for buying, 2=>for selling 
}
```

Responses:
```
{
    "status": "success",
    "err_no": 0,
    "msg": "get finished orders success.",
    "data": [
        {
            "side": 2,
            "addtime": 1534677163694,
            "type": 1,
            "price": "0.5",
            "avg_price": 0.093,
            "amount": "1",
            "symbol": "eth_btc",
            "finishtime": 1534924649050,
            "status": 1,
            "deal_amount": "0.068122",
            "order_id": 116875
        }
    ]
}
```

</details>


