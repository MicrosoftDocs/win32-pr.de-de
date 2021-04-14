---
title: Principal.ID-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner des Prinzipals ab oder legt ihn fest.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- ID-Eigenschaft Taskplaner
- ID-Eigenschaft Taskplaner, Prinzipal Objekt
- Prinzipal Objekt Taskplaner, ID-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392087"
---
# <a name="principalid-property"></a>Principal.ID-Eigenschaft

Ruft bei der Skripterstellung den Bezeichner des Prinzipals ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Principal.Id As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner des Prinzipals.

## <a name="remarks"></a>Bemerkungen

Dieser Bezeichner wird auch verwendet, wenn die Eigenschaft " [**aktioncollection. Context**](actioncollection-context.md) " angegeben wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Bezeichner des Prinzipals im ID-Attribut des [**Principal**](taskschedulerschema-principal-principaltype-element.md) -Elements des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Aktions Sammlung. Context"**](actioncollection-context.md)
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





