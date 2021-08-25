---
title: MPEXECUTION_STATUS -Enumeration (MpClient.h)
description: Möglicher Status der Bedrohungsausführung.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS enumeration Legacy Windows Environment Features
- PMPEXECUTION_STATUS enumeration pointer Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943910"
---
# <a name="mpexecution_status-enumeration"></a>MPEXECUTION \_ STATUS-Enumeration

Möglicher Status der Bedrohungsausführung.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**\_ \_ MP-AUSFÜHRUNGSSTATUS \_ UNBEKANNT**
</dt> <dd>

Der Ausführungsstatus ist nicht bekannt.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**\_ \_ MP-AUSFÜHRUNGSSTATUS \_ BLOCKIERT**
</dt> <dd>

Ausführung durch Minifilter blockiert.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_ \_ MP-AUSFÜHRUNGSSTATUS \_ ZULÄSSIG**
</dt> <dd>

Die Ausführung per Minifilter ist zulässig.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_ \_ AUSFÜHRUNGSSTATUS DES MP \_**
</dt> <dd>

Die Bedrohung wird ausgeführt.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**\_ \_ MP-AUSFÜHRUNGSSTATUS \_ \_ WIRD NICHT AUSGEFÜHRT**
</dt> <dd>

Die Bedrohung wird nicht ausgeführt und ist nur während der Behebung über die Engine verfügbar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





