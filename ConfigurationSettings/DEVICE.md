# DEVICE

## SCAN
Đưa thiết bị vào mạng
### Gửi đi

```json
{
     "CMD":"SCAN"
}
```
### Mẫu phản hồi
Bản tin phản hồi khi 1 thiết bị được thêm vào mạng
```json
{
   "CMD": "TYPE_DEVICE",
   "DATA": 
           {
                   "DEVICE_UNICAST_ID": 123,
                   "DEVICE_ID": "b717f8d86f1843c0ae4669c32998f653", 
                   "DEVICE_KEY": "b717f8d86f1843c0ae4669c32998f653",
                   "NET_KEY": "b717f8d86f1843c0ae4669c32998f653",
                   "APP_KEY": "b717f8d86f1843c0ae4669c32998f653",
                   "CATEGORY_ID":   23002                
           }   
}
```

## STOP
Dừng quá trình đưa thiết bị vào mạng
### Gửi đi

```json
{
     "CMD":"STOP"
}
```
### Mẫu phản hồi
```json
{
     "CMD":"STOP"
}
```




## RESET_NODE
Xóa 1 hoặc nhiều thiết bị trong mạng
### Gửi đi

```json
{
     "CMD":"RESET_NODE",
      "DATA": [
               {
                       "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
                       "DEVICE_UNICAST_ID": 9
               },
               {
                       "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f654",
                       "DEVICE_UNICAST_ID": 8
               },
               {
                       "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f655",
                       "DEVICE_UNICAST_ID": 7
               }
            ]
}
```
### Mẫu phản hồi
Từng thiết bị sẽ phản hồi về sau khi xóa khỏi mạng BLE

```json

{
     "CMD":"RESET_NODE",
      "DEVICES": 
               {
                       "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
                       "DEVICE_UNICAST_ID": 9
               }
}
```