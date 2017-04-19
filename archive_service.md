

<!-- Start src\app\services\acquisition\archive.service.js -->

#ARCHIVE SERVICE

Provides methods to retrieve archived data.

## DataRequest(dataId, frameId, deviceId, aggregate, columnName, units, min, max, defaultValue)

DataRequest constructor

### Params:

* **string** *dataId* 
* **string** *frameId* 
* **string** *deviceId* 
* **string** *aggregate* selected aggregate algorithm (optional)
* **string** *columnName* name of the column corresponding to the data in the request result (optional)
* **string** *units* (optional)
* *min* (optional)
* *max* (optional)
* *defaultValue* (optional)

### Return:

* DataRequest object. 

### Example:
    dataRequest = new archiveService.DataRequest('watertemp', 'weather', 'BATOS001');

##PUBLIC METHODS

## getData

Sends an archive request to retrieve data (return a promise)

### Params:

* **String** *dataId:* string to be escaped
* *frameId* 

### Return:

* **DataRequest** data request object        dataList, startDate, endDate, maxNumValues, strategy, referenceOrResampleInterval, intervalStampFraction

## getDataSimple

Simple method to retrieve data

### Params:

* **String** *dataId:* string to be escaped
* *frameId* 

### Return:

* **DataRequest** data request object. 
       dataId, frameId, deviceId, start, end, maxNumValues, interval

## getLastData(dataId:, frameId)

Get the last archived data; specify the duration (in secondes).

### Params:

* **String** *dataId:* string to be escaped
* *frameId* 

### Return:

* **DataRequest** data request object 

### Example:
    new DataRequest()

## downloadFile

Download a file (csv or netCDF) with the archived data

### Params:

* **String** *dataId:* string to be escaped
* *frameId* 

### Return:

* **DataRequest** data request object 

      format,
      dataList,
      startDate, // UTC format !
      endDate, // UTC format !
      maxNumValues,
      strategy,
      referenceOrResampleInterval,
      intervalStampFraction

<!-- End src\app\services\acquisition\archive.service.js -->

