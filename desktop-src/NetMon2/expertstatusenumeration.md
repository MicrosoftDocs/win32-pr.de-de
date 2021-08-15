---
description: Die EXPERTSTATUSENUMERATION-Enumeration enthält Statuswerte. Sie wird vom Status-Member der EXPERTSTATUS-Struktur und dem Status-Parameter in ExpertIndicateStatus verwendet.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: EXPERTSTATUSENUMERATION-Enumeration (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ee0729deab566717457f03af27a7e31de8cdf8f1b78f9a5f97b3c3ff406641fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795793"
---
# <a name="expertstatusenumeration-enumeration"></a>EXPERTSTATUSENUMERATION-Enumeration

Die **EXPERTSTATUSENUMERATION-Enumeration** enthält Statuswerte. Sie wird vom **Status-Member** der [EXPERTSTATUS-Struktur](expertstatus.md) und dem *Status-Parameter* in [ExpertIndicateStatus](expertindicatestatus.md)verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INACTIVE**
</dt> <dd>

Der Experte hat nie begonnen.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS \_ STARTING**
</dt> <dd>

Der Experte beginnt.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ WIRD AUSGEFÜHRT**
</dt> <dd>

Der Experte wird normal ausgeführt.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_EXPERTSTATUS-PROBLEM**
</dt> <dd>

Ein in *SubStatus* angegebenes Problem hat den Experten beendet.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ ABGEBROCHEN**
</dt> <dd>

Netzwerkmonitor hat den Experten beendet.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ DONE**
</dt> <dd>

Der Experte wurde erfolgreich abgeschlossen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




