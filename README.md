
# 電梯和PTS 交握

```mermaid
sequenceDiagram

    participant PTS
    participant Elev

    note over PTS,Elev: 程式啟動跳心跳
        PTS->>Elev: 12:1
        Elev-->>PTS: 8:1
        PTS->>Elev: 12:0
        Elev-->>PTS: 8:0
        PTS->>Elev: 12:1
        Elev-->>PTS: 8:1
        PTS->>Elev: 12:0
        Elev-->>PTS: 8:0

   

```
```mermaid
sequenceDiagram

    participant PTS ELEV 心跳
    participant PTS
    participant Elev

 note over PTS,Elev: 電梯在4F,AMR 在5F 要使用電梯
        PTS->>Elev: postVehicleStatus (VEHCILE:1、Status=0...)
        Elev-->>PTS: Response 完成登錄作業
        PTS->>Elev: postVehicleStatus (VEHCILE:2、Status=4...)
        Elev-->>PTS: Response 完成登錄作業
        PTS->>Elev: postVehicleStatus (VEHCILE:3、Status=4...)
        Elev-->>PTS: Response 完成登錄作業

```





