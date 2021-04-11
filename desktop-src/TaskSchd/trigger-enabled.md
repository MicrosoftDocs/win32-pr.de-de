---
title: Eigenschaft "Auslösung"
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Aktivierte Eigenschaften Taskplaner
- Aktivierte Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949638"
---
# <a name="triggerenabled-property"></a>Eigenschaft "Auslösung"

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn der-Wert aktiviert ist. andernfalls false. Der Standardwert ist "True".

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die aktivierte Eigenschaft mit dem [**aktivierten**](taskschedulerschema-enabled-triggerbasetype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





