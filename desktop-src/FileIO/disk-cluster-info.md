---
description: Stellt Informationen dar, die auf dem Partitions-Manager über einen Datenträger verwaltet werden, der Teil eines Clusters ist.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO-Struktur (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813792"
---
# <a name="disk_cluster_info-structure"></a>DISK \_ CLUSTER \_ INFO-Struktur

Stellt Informationen dar, die auf dem Partitions-Manager über einen Datenträger verwaltet werden, der Teil eines Clusters ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Versionsnummer. Dieser Wert muss auf die Größe dieser Struktur festgelegt werden.

</dd> <dt>

**Flags**
</dt> <dd>

Eine Kombination von Flags im Zusammenhang mit Datenträgern und Clustern.



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**DATENTRÄGER \_ \_CLUSTERFLAG \_ AKTIVIERT**</dt> <dt>1</dt> </dl>                                          | Der Datenträger wird als Teil des Clusterdiensts verwendet.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**DATENTRÄGER \_ \_CLUSTERFLAG \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Volumes auf dem Datenträger werden von CSVFS auf allen Knoten des Clusters verfügbar gemacht.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**DATENTRÄGER \_ \_CLUSTERFLAG \_ IN \_ MAINTENANCE**</dt> <dt>4</dt> </dl>                    | Die diesem Datenträger zugeordnete Clusterressource befindet sich im Wartungsmodus.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**DATENTRÄGER \_ \_CLUSTERFLAG \_ PNP \_ ARRIVAL \_ COMPLETE**</dt> <dt>8</dt> </dl> | Der Clusterdatenträgertreiber für den Kernelmodus (clusdisk) hat eine PnP-Benachrichtigung über den Eingang des Datenträgers erhalten.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Die Flags, die im **Flags-Member** geändert werden.

</dd> <dt>

**Benachrichtigen**
</dt> <dd>

**TRUE** zum Senden einer Layoutänderungsbenachrichtigung; Andernfalls **FALSE**.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Datenträgerverwaltungsstrukturen](disk-management-structures.md)
</dt> <dt>

[**IOCTL \_ DISK \_ GET \_ CLUSTER \_ INFO**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**IOCTL \_ DISK \_ SET \_ CLUSTER \_ INFO**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




