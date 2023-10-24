# Note
baseUrl：https://apiv2.cascad3.com/cascad3-client

Before calling the Endpoint, you need to create a cascade（https://www.cascad3.com/） and get the cascadeId, and set it in the request header

Cascadeinfo：{"cascadeId":"cascadeIdValue"}

like this：

![img_1.png](img_1.png)



## 1、Pagination data of pieces
#### Endpoint 
GET /client/cascade/home/pageHomePieces

### Request parameters

| name      |  type    | Required | Description   |
|-----------|---------|------|-------------------|
| keyword   |  string  | no   | search keyword    |
| pageIndex |  integer | no    | Current page number  |
| pageSize  |  integer | no    | Number of records displayed per page    |
| sortBy    | integer | no    | Sort type: 0: Created time descending (default), 1: Number of likes,2: Number of comments,3: Number of reads,4: Number of downStreams,5: Amount of rewards |

### Response：
```json
{
    "data": {
        "data": [
            {
                "arId": "string",              
                "authorFaceUrl": "string",
                "authorUsername": "string",
                "commentCount": 0,
                "coverUrl": "string",
                "createBy": 0,
                "createByAddress": "string",
                "createTime": "2019-08-24T14:15:22Z",
                "downstreamCount": 0,
                "featured": true,
                "id": 0,
                "likeCount": 0,
                "rewardAmount": 0,
                "subTitle": "string",
                "tagInfos": [
                    {
                        "id": 0,
                        "tag": "string",
                        "tagColor": "string"
                    }
                ],
                "title": "string",
                "uuid": "string"
            }
        ],
        "pageCount": 0,
        "pageIndex": 0,
        "pageSize": 0,
        "totalRecords": 0
    },
    "msg": "string",
    "status": 0
}
```
![img.png](img.png)


## 2、Piece detail
#### Endpoint
GET /client/cascade/home/pieceInfo

### Request parameters
| name      |  type    | Required | Description |
|-----------|---------|------|-----------|
|pieceUuid|string| yes |pieceUuid|

### Response：
```json
{
  "data": {
    "arId": "string",
    "author": {
      "bio": "string",
      "dailyStreamArId": "string",
      "email": "string",
      "faceUrl": "string",
      "id": 0,
      "inStream": 0,
      "outStream": 0,
      "tokenAmount": 0,
      "username": "string",
      "walletAddress": "string"
    },
    "authorFaceUrl": "string",
    "authorUsername": "string",
    "commentCount": 0,
    "content": "string",
    "coverUrl": "string",
    "createBy": 0,
    "createByAddress": "string",
    "createTime": "2019-08-24T14:15:22Z",
    "currState": 0,
    "downstreamCount": 0,
    "featured": true,
    "id": 0,
    "isLike": true,
    "likeCount": 0,
    "pieceEditorId": 0,
    "ratio": 0,
    "readCount": 0,
    "rewardAmount": 0,
    "subTitle": "string",
    "tagInfos": [
      {
        "id": 0,
        "tag": "string",
        "tagColor": "string"
      }
    ],
    "title": "string",
    "uuid": "string"
  },
  "msg": "string",
  "status": 0
}

```