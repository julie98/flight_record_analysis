Data interpretation -- 3742 entries in total

1. Plat/ equipment/ att -- 1258 rows

   possible tasks: 

   - find out the raderID that associated with a specific platID

   - fHeight, fSpeed, fDir

```json
db.getCollection("Second").insert([ {
    _id: ObjectId("6430d9ffe96ada3d115b0a18"),
    sRID: "1_1_1",
    PlatID: NumberInt("6"),
    EquipmentName: "yanshi-red",
    EquipmentType: "plane",
    ATT: "Enum_ATT_1",
    fTime: 24,
    fLon: 117.63942,
    fLat: 23.964516,
    fHeight: 5000,
    fSpeed: 300,
    fDir: 75.85895,
    iActiveFlag: NumberInt("1"),
    nRCSNum: NumberInt("1"),
    RCSArray: [
        {
            fRCS: 5
        }
    ],
    FlyPosType: "Enum_Cruise"
} ]);
```



2. RadarID -- 2484
   - RadarID/ iTargetNum/ RadarDetectPlat -- 1242
   -  targetID/ iDetectZoneNum/ ZonePoint  -- 1242

```json
db.getCollection("Second").insert([ {
    _id: ObjectId("6430d9ffe96ada3d115b0a13"),
    sRID: "1_1_1",
    fTime: 20.8,
    RadarID: NumberInt("7"),
    iTargetNum: NumberInt("1"),
    RadarDetectPlat: [
        {
            PlatID: NumberInt("15"),
            ATT: "Enum_ATT_2",
            fLon: 118.29824,
            fLat: 24.060064,
            fHeight: 4192.3384,
            fSpeed: 233.05397,
            fDir: 299.30017,
            DetectError: 72.9096
        }
    ]
} ]);



db.getCollection("Second").insert([ {
    _id: ObjectId("6430d9ffe96ada3d115b0a15"),
    sRID: "1_1_1",
    fTime: 20.8,
    RadarID: NumberInt("7"),
    TargetID: NumberInt("6"),
    iDetectZoneNum: NumberInt("121"),
    ZonePoint: [
        {
            fLon: 117.63083,
            fLat: 23.962542
        },
        {
            fLon: 117.97182,
            fLat: 25.044592
        },
	.....


    ]
} ]);

```





课题名称：基于仿真环境下多源数据的关联性分析算法研究与应用
课题依据：随着信息技术的高速发展，社会数据化程度得到不断提升，数据源的多样化、数据量的巨大化以及数据集的关联化为信息的获取与分析提供了更为有利的条件，通过对多源数据进行组合或综合,利用**多源数据的交叉印证与关联分析**,可得到比单一数据源、更全面的信息。在当前大数据时代，针对多源数据的融合已成为大数据分析处理的关键环节。
任务要求：针对分布式虚拟飞行场景下飞行数据量大，数据维度高的问题，研究对态势转变起重要数据关联性分析算法，为目标识别、轨迹预测、意图预测算法提供数据的关联信息。该选题涉及大数据关联性分析。通过改题目的完成，可以培养学生大数据理论基础与实际动手解决复杂问题的能力，为日后相关工作打下基础。该选题需要完成一下内容：

（1）多源数据的读取与存储

（2）基于多源数据的关联性分析算法（2-3种）

（3）不同算法得出的时序信息融合