---
title: Idlesettings. stoponidleend (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Stoponidleend-Eigenschaft Taskplaner
- Stoponidleend-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, stoponidleend-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858740"
---
# <a name="idlesettingsstoponidleend-property"></a>Idlesettings. stoponidleend (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**stoponidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

[**Idlesettings**](idlesettings.md)
</dt> </dl>

 

 





