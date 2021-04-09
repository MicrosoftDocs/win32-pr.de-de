---
title: MPTHREAT_DETECTION-Enumeration (mpclient. h)
description: Mögliche bekannte Typen fehlerhafter Bedrohungserkennung.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_DETECTION enumerationszeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741008"
---
# <a name="mpthreat_detection-enumeration"></a>Mpthreat- \_ Erkennungs Enumeration

Mögliche bekannte Typen fehlerhafter Bedrohungserkennung.

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

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP- \_ Bedrohungs \_ Erkennung \_ konkret**
</dt> <dd>

Die Bedrohung wurde über konkrete Signaturen erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP- \_ Bedrohungs \_ Erkennung \_ heuristic**
</dt> <dd>

Die Bedrohung wurde über eine Heuristik erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP- \_ Bedrohungs \_ Erkennung \_ generisch**
</dt> <dd>

Die Bedrohung wurde über generische Signaturen erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP- \_ Bedrohungs \_ Erkennung \_ verdächtig**
</dt> <dd>

Die Bedrohungserkennung wurde durch die Verhaltens Überwachung erkannt.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP- \_ Bedrohungs \_ Erkennung \_ FastPath**
</dt> <dd>

Die Bedrohung wurde über FastPath erkannt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





