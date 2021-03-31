# GROUP

## Tạo một nhóm "TYPE": "CREATE"
Tạo một nhóm mới gồm 3 thiết bị
### Gửi đi

```json
{
      "CMD": "GROUP",
      "TYPE": "CREATE",
      "DATA": {
           "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
           "CATEGORY_ID": 12,
           "NAME": "abc",
           "DEVICES": [
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
}
```
### Mẫu phản hồi
```json
Thành công
{
     "CMD": "GROUP",
     "TYPE": "DEVxICE_RESPONSE",
     "DATA": {
          "GROUP_ID": "aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
          "GROUP_UNICAST_ID": 49152,
          "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
          "DEVICE_UNICAST_ID": 5,
          "STATUS": "SUCCESS"
      }
}
```
## Thêm thiết bị vào nhóm "TYPE": "ADD_DEVICE"
 Thêm 3 thiêt bị vào nhóm đã có sẵn
 
 ### Gửi đi
```json
{
      "CMD": "GROUP",
      "TYPE": "ADD_DEVICE",
      "DATA": {
           "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
           "GROUP_UNICAST_ID": 49152,
           "DEVICES": [
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
}
```
### Mẫu phản hồi
```json
Thành công
{
     "CMD": "GROUP",
     "TYPE": "DEVxICE_RESPONSE",
     "DATA": {
          "GROUP_ID": "aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
          "GROUP_UNICAST_ID": 49152,
          "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
          "DEVICE_UNICAST_ID": 5,
          "STATUS": "SUCCESS"
      }
}
```

## Xóa thiết bị trong nhóm "TYPE": "REMOVE_DEVICE" 

Xóa 3 thiết bị trong nhóm
### Gửi đi
```json
{
      "CMD": "GROUP",
      "TYPE": "REMOVE_DEVICE",
      "DATA": {
           "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
           "GROUP_UNICAST_ID": 49152,
           "DEVICES": [
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
}
```
### Mẫu phản hồi
```json
{
      "CMD": "GROUP",
      "TYPE": "REMOVE_DEVICE",
      "DATA": {
           "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
           "GROUP_UNICAST_ID": 49152,
           "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
          "DEVICE_UNICAST_ID": 5,
          "STATUS": "SUCCESS"
      }
}
```

## Xóa cả nhóm "TYPE": "DELETE"
Xóa nhóm đang tồn tại
### Gửi đi
```json
{
      "CMD": "GROUP",
      "TYPE": "DELETE",
      "DATA":
      {
             "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
             "GROUP_UNICAST_ID": 49152
      }      
}
```
### Mẫu phản hồi
```json
{
      "CMD": "GROUP",
      "TYPE": "DELETE",
      "DATA":
      {
             "GROUP_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
             "GROUP_UNICAST_ID": 49152
      }      
}
```
 