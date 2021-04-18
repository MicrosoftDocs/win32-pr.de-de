---
description: Die expertstatusenumeration-Enumeration enthält Statuswerte. Sie wird vom Status-Member der Expertenstatus-Struktur und vom Status-Parameter in "Expertenstatus" verwendet.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Expertstatus usenumeration-Enumeration (Netmon. h)
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
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345004"
---
# <a name="expertstatusenumeration-enumeration"></a>Expertstatus usenumeration-Enumeration

Die **expertstatusenumeration** -Enumeration enthält Statuswerte. Sie wird vom **Status** -Member der [Expertenstatus](expertstatus.md) -Struktur und vom *Status* - [Parameter in "Expertenstatus"](expertindicatestatus.md)verwendet.

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

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**Profil Status \_ inaktiv**
</dt> <dd>

Der Experte wurde nie gestartet.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**Profil Status wird \_ gestartet**
</dt> <dd>

Der Experte wird gestartet.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**Profil Status wird \_ ausgeführt**
</dt> <dd>

Der Experte wird normal ausgeführt.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**expertstatus- \_ Problem**
</dt> <dd>

Der Experte hat ein im *unter Status* angegebenes Problem beendet.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**der Expertenstatus wurde \_ abgebrochen.**
</dt> <dd>

Netzwerkmonitor den Experten beendet.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**Profil Status \_ abgeschlossen**
</dt> <dd>

Der Experte wurde erfolgreich beendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




