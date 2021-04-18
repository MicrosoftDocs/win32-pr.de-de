---
title: Trigger.ID-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner für den-Typ ab oder legt ihn fest.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- ID-Eigenschaft Taskplaner
- ID-Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, ID-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517558"
---
# <a name="triggerid-property"></a>Trigger.ID-Eigenschaft

Ruft bei der Skripterstellung den Bezeichner für den-Typ ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner für den-Auslösers. Dieser Bezeichner wird von der-Taskplaner zu Protokollierungs Zwecken verwendet.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der auslöserbezeichner im ID-Attribut der einzelnen auslöserelemente (z. b. des ID-Attributs des [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Elements) des Taskplaner Schemas angegeben.

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
</dt> </dl>

 

 





