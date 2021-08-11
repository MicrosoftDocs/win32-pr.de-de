---
title: MPTHREAT_ACTION-Enumeration (MpClient.h)
description: Mögliche Bedrohungsaktionen.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION enumeration Legacy Windows Environment Features
- PMPTHREAT_ACTION-Enumerationszeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a3cd46583b9736ad8304c16e3b12d4f0157edcdb319fd0923a0fe737d504415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247264"
---
# <a name="mpthreat_action-enumeration"></a>MPTHREAT \_ ACTION-Enumeration

Mögliche Bedrohungsaktionen.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP \_ THREAT \_ ACTION \_ UNKNOWN**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP \_ THREAT \_ ACTION \_ CLEAN**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP \_ THREAT \_ ACTION \_ QUARANTINE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP \_ THREAT \_ ACTION \_ REMOVE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP \_ THREAT \_ ACTION \_ ALLOW**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP \_ THREAT \_ ACTION \_ USERDEFINED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP \_ THREAT \_ ACTION \_ NOACTION**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP \_ THREAT \_ ACTION \_ BLOCK**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_MAX. WERT DER \_ MP-BEDROHUNGSAKTION \_ \_**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





