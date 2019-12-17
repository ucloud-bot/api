# 删除UMem备份-DeleteUMemBackup

删除UMem备份

# Request Parameters
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Region|string|地域。 参见 [地域和可用区列表](api/summary/regionlist)|**Yes**|
|Zone|string|可用区。参见 [可用区列表](api/summary/regionlist)|**Yes**|
|ProjectId|string|项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](api/summary/get_project_list)|No|
|SpaceId|string|资源id|**Yes**|
|BackupId|string|备份id|**Yes**|

# Response Elements
|Parameter name|Type|Description|Required|
|---|---|---|---|
|RetCode|int|返回码|**Yes**|
|Action|string|操作名称|**Yes**|

# Request Example
```
https://api.ucloud.cn/?Action=DeleteUMemBackup
&Region=cn-zj
&Zone=cn-zj-01
&ProjectId=bCasIwjT
&SpaceId=WSBOPyAy
&BackupId=mUjmLmyu
```

# Response Example
```
{
    "Action": "DeleteUMemBackupResponse", 
    "RetCode": 0
}
```
