---
title: MPTHREAT_DETECTION -Enumeration (MpClient.h)
description: Mögliche bekannte Typen der Erkennung von bedrohungsbedrohungen.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION enumeration Legacy Windows Environment Features
- PMPTHREAT_DETECTION enumeration pointer Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d362edbb7257f8be5577880a4390c5a2f5f5703504a5f7447154bebe5ada500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601180"
---
# <a name="mpthreat_detection-enumeration"></a>MPTHREAT \_ DETECTION-Enumeration

Mögliche bekannte Typen der Erkennung von bedrohungsbedrohungen.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**KONKRETE \_ \_ MP-BEDROHUNGSERKENNUNG \_**
</dt> <dd>

Bedrohungen wurden über konkrete Signaturen erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_ \_ HEURISTISCHE \_ MP-BEDROHUNGSERKENNUNG**
</dt> <dd>

Bedrohung wurde über heuristisch erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_ \_ MP-BEDROHUNGSERKENNUNG \_ GENERISCH**
</dt> <dd>

Bedrohungen wurden über generische Signaturen erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**\_ \_ MP-BEDROHUNGSERKENNUNG \_ VERDÄCHTIG**
</dt> <dd>

Bedrohungen wurden über die Verhaltensüberwachung erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ THREAT \_ DETECTION \_ FASTPATH**
</dt> <dd>

Die Bedrohung wurde über fastpath erkannt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





