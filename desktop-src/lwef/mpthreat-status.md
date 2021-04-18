---
title: MPTHREAT_STATUS-Enumeration (mpclient. h)
description: Möglicher Bedrohungs Status.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_STATUS enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339954"
---
# <a name="mpthreat_status-enumeration"></a>Mpthreat- \_ statusenumeration

Möglicher Bedrohungs Status.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP- \_ Bedrohungs \_ Status \_ unbekannt**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP- \_ Bedrohungs \_ Status \_ erkannt**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**Management Pack- \_ Bedrohungs \_ Status \_ bereinigt**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP- \_ Bedrohungs \_ Status unter \_ Quarantäne**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP- \_ Bedrohungs \_ Status \_ entfernt**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP- \_ Bedrohungs \_ Status \_ zulässig**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP- \_ Bedrohungs \_ Status \_ blockiert**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**Fehler \_ beim \_ \_ Bereinigen des Management Packs. \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**Fehler bei MP- \_ Bedrohungs \_ Status \_ \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**Fehler \_ beim \_ \_ Entfernen \_ des Management Packs.**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**Fehler bei MP- \_ Bedrohungs \_ Status \_ \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP- \_ Bedrohungs \_ Status \_ abgebrochen**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**Fehler beim MP- \_ Bedrohungs \_ Status. \_ \_**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





