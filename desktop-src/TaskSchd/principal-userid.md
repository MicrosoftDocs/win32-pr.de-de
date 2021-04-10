---
title: Principal. UserId-Eigenschaft
description: Ruft bei der Skripterstellung die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserID-Eigenschaft Taskplaner
- UserID-Eigenschaft Taskplaner, Prinzipal Objekt
- Prinzipal Objekt Taskplaner, UserID-Eigenschaft
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
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104355"
---
# <a name="principaluserid-property"></a>Principal. UserId-Eigenschaft

Ruft bei der Skripterstellung die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Benutzer Bezeichner, der zum Ausführen der Aufgabe erforderlich ist.

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft nicht fest, wenn ein Gruppen Bezeichner in der [**GroupID**](principal-groupid.md) -Eigenschaft angegeben ist.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Benutzer-ID für den Prinzipal mit dem [**UserID**](taskschedulerschema-userid-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> <dt>

[**Principal. groupID**](principal-groupid.md)
</dt> </dl>

 

 





