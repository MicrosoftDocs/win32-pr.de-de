---
title: MPTHREAT_STATUS-Enumeration (MpClient.h)
description: Möglicher Bedrohungsstatus.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS enumeration Legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPTHREAT_STATUS enumeration pointer Legacy Windows Environment Features (Legacy Windows-Umgebungsfeatures)
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
ms.openlocfilehash: 92d800cbfb0adbeb994586a69e38ac4a1ad2a8957091508b147bd582fef5233e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476262"
---
# <a name="mpthreat_status-enumeration"></a>MPTHREAT \_ STATUS-Enumeration

Möglicher Bedrohungsstatus.

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

<span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP \_ THREAT \_ STATUS \_ UNKNOWN**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**\_ \_ MP-BEDROHUNGSSTATUS \_ ERKANNT**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_ \_ MP-BEDROHUNGSSTATUS \_ BEREINIGT**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**\_MP-BEDROHUNGSSTATUS \_ \_ UNTER QUARANTÄNE GESTELLT**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_ \_ MP-BEDROHUNGSSTATUS \_ ENTFERNT**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_ \_ MP-BEDROHUNGSSTATUS \_ ZULÄSSIG**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**\_MP-BEDROHUNGSSTATUS \_ \_ BLOCKIERT**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_FEHLER \_ BEIM \_ BEREINIGEN DES MP-BEDROHUNGSSTATUS \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**\_FEHLER \_ BEI \_ MP-BEDROHUNGSSTATUSQUARANTÄNE \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP \_ THREAT \_ STATUS \_ REMOVE \_ FAILED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP \_ THREAT \_ STATUS \_ ALLOW \_ FAILED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**\_ \_ MP-BEDROHUNGSSTATUS \_ ABGEBROCHEN**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_FEHLER \_ BEIM \_ MP-BEDROHUNGSSTATUSBLOCK \_**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





