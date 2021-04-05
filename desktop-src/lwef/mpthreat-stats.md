---
title: MPTHREAT_STATS Struktur (mpclient. h)
description: Bedrohungs bezogene Statistiken.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_STATS Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858858"
---
# <a name="mpthreat_stats-structure"></a>Mpthreat \_ Stats-Struktur

Bedrohungs bezogene Statistiken.

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

**Anzahl von Zustellungen**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Anzahl der erkannten Bedrohungen.

</dd> <dt>

**Verdächtiger Anzahl**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Anzahl der erkannten Bedrohungen bei der Verhaltens Überwachung.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **uint \[ 4 \]**

</dd> <dd>

Felder, die für die zukünftige Verwendung reserviert sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





