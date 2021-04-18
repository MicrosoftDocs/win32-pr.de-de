---
title: Principal. GroupID (Eigenschaft)
description: Dient zum Abrufen oder Festlegen des Bezeichners der Benutzergruppe, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- GroupID-Eigenschaft Taskplaner
- GroupID-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, GroupID-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339995"
---
# <a name="principalgroupid-property"></a>Principal. GroupID (Eigenschaft)

Dient zum Abrufen oder Festlegen des Bezeichners der Benutzergruppe, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

## <a name="syntax"></a>Syntax


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner der Benutzergruppe, die diesem Prinzipal zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft nicht fest, wenn ein Benutzer Bezeichner in der [**UserID**](principal-userid.md) -Eigenschaft angegeben ist.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Gruppen Bezeichner für einen Prinzipal im [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UserID**](principal-userid.md)
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





