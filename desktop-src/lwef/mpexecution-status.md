---
title: MPEXECUTION_STATUS-Enumeration (mpclient. h)
description: Möglicher Bedrohungs Ausführungs Status.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPEXECUTION_STATUS enumerationszeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858792"
---
# <a name="mpexecution_status-enumeration"></a>Mpexecution- \_ statusenumeration

Möglicher Bedrohungs Ausführungs Status.

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

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP- \_ Ausführungs \_ Status \_ unbekannt**
</dt> <dd>

Der Ausführungs Status ist nicht bekannt.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP- \_ Ausführungs \_ Status \_ blockiert**
</dt> <dd>

Die Ausführung durch den Mini Filter wurde blockiert.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP- \_ Ausführungs \_ Status \_ zulässig**
</dt> <dd>

Die Ausführung durch den Mini Filter ist zulässig.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**Ausführungs Status von MP wird \_ \_ \_ ausgeführt**
</dt> <dd>

Die Bedrohung wird ausgeführt.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP- \_ Ausführungs \_ Status wird \_ nicht \_ ausgeführt**
</dt> <dd>

Die Bedrohung wird nicht ausgeführt und ist nur während der Wiederherstellung über die Engine verfügbar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





