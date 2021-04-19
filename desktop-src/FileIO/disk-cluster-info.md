---
description: Stellt Informationen dar, die auf dem Partitions-Manager zu einem Datenträger, der Teil eines Clusters ist, verwaltet werden.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO Struktur (ntdddisk. h)
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
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362239"
---
# <a name="disk_cluster_info-structure"></a>Datenträger \_ Cluster- \_ Informationsstruktur

Stellt Informationen dar, die auf dem Partitions-Manager zu einem Datenträger, der Teil eines Clusters ist, verwaltet werden.

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

Eine Kombination von Flags, die sich auf Datenträger und Cluster beziehen.



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> Datenträger <dt>**\_ \_Clusterflag \_ aktiviert**</dt> <dt>1</dt> </dl>                                          | Der Datenträger wird als Teil des Cluster Dienstanbieter verwendet.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> Datenträger <dt>**\_ \_Clusterflag \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Volumes auf dem Datenträger werden von csvfs auf allen Knoten des Clusters verfügbar gemacht.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> Datenträger <dt>**\_ \_Clusterflag \_ in \_ Wartung**</dt> <dt>4</dt> </dl>                    | Die dieser Festplatte zugeordnete Cluster Ressource befindet sich im Wartungsmodus.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> Datenträger <dt>**\_ \_Clusterflag \_ PnP-Ankunft bei \_ \_ Abschluss**</dt> <dt>8</dt> </dl> | Der Cluster Datenträger Treiber für den Kernel Modus (Clusdisk) hat eine PNP-Benachrichtigung über die Ankunft des Datenträgers erhalten.<br/> |



 

</dd> <dt>

**Flagsmask**
</dt> <dd>

Die Flags, die im **Flags** -Member geändert werden.

</dd> <dt>

**Benachrichtigen**
</dt> <dd>

**True** , um eine layoutänderungsbenachrichtigung zu senden. andernfalls **false**.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen der Datenträgerverwaltung](disk-management-structures.md)
</dt> <dt>

[**ioctl-Datenträger \_ \_ get \_ Cluster \_ Info**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**ioctl-Datenträger \_ \_ Satz- \_ Cluster \_ Informationen**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




