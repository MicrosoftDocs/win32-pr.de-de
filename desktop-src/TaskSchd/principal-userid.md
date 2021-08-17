---
title: Principal.UserId-Eigenschaft
description: Ruft für die Skripterstellung den Benutzerbezeichner ab, der zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diesen fest.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId-Eigenschaft Taskplaner
- UserId-Eigenschaft Taskplaner , Principal-Objekt
- Prinzipalobjekt Taskplaner , UserId-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060028"
---
# <a name="principaluserid-property"></a>Principal.UserId-Eigenschaft

Ruft für die Skripterstellung den Benutzerbezeichner ab, der zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Benutzerbezeichner, der zum Ausführen der Aufgabe erforderlich ist.

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft nicht fest, wenn in der [**GroupId-Eigenschaft**](principal-groupid.md) ein Gruppenbezeichner angegeben ist.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Benutzerbezeichner für den Prinzipal mithilfe des [**UserId-Elements**](taskschedulerschema-userid-principaltype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> <dt>

[**Principal.GroupId**](principal-groupid.md)
</dt> </dl>

 

 





