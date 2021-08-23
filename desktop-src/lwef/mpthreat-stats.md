---
title: MPTHREAT_STATS-Struktur (MpClient.h)
description: Bedrohungsbezogene Statistiken.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPTHREAT_STATS Strukturzeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975940"
---
# <a name="mpthreat_stats-structure"></a>\_MPTHREAT-STATS-Struktur

Bedrohungsbezogene Statistiken.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Member

<dl> <dt>

**ThreatCount**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Anzahl der erkannten Bedrohungen.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Anzahl der bei der Verhaltensüberwachung erkannten Bedrohungen.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **UINT \[ 4 \]**

</dd> <dd>

Felder, die für die zukünftige Verwendung reserviert sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





