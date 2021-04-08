---
title: Tasksettings. Hidden (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe in der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Taskplaner für verborgene Eigenschaften
- Ausgeblendete Eigenschaften Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Hidden-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742737"
---
# <a name="tasksettingshidden-property"></a>Tasksettings. Hidden (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe in der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest. Administratoren können diese Einstellung jedoch überschreiben, indem Sie einen "Master Switch" verwenden, der alle Aufgaben in der Benutzeroberfläche sichtbar macht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert **true** ist, gibt der Wert an, dass die Aufgabe nicht in der Benutzeroberfläche sichtbar ist. Wenn der Wert **false** ist, wird die Aufgabe in der Benutzeroberfläche angezeigt. Der Standardwert ist **False**.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Hidden-Element [**(settingstype)**](taskschedulerschema-hidden-settingstype-element.md) des Taskplaner-Schemas angegeben.

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

 

 





