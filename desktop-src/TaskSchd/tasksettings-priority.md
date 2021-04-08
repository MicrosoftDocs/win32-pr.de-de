---
title: Tasksettings. Priority (Eigenschaft)
description: Ruft bei der Skripterstellung die Prioritätsstufe der Aufgabe ab oder legt diese fest.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Prioritäts Eigenschaft Taskplaner
- Prioritäts Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Priority-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949513"
---
# <a name="tasksettingspriority-property"></a>Tasksettings. Priority (Eigenschaft)

Ruft bei der Skripterstellung die Prioritätsstufe der Aufgabe ab oder legt diese fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Prioritäts Ebene (0-10) der Aufgabe. Der Standard ist 7.

## <a name="remarks"></a>Bemerkungen

Prioritätsstufe 0 ist die höchste Priorität, und Prioritätsstufe 10 ist die niedrigste Priorität. Der Standardwert ist 7. Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben verwendet, und die Prioritätsstufen 4, 5 und 6 werden für interaktive Aufgaben verwendet.

Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Prioritäts Klassen Wert basiert. Ein Wert für die Prioritätsstufe (Thread Priorität) wird für com-Handler-, Meldungs-und e-Mail-Aufgaben Aktionen verwendet. Weitere Informationen zu den Werten für die Prioritäts Klasse und Prioritätsstufen finden Sie unter [Planungs Prioritäten](/windows/desktop/ProcThread/scheduling-priorities). In der folgenden Tabelle sind die möglichen Werte für den *Prioritäts* Parameter sowie die entsprechenden Werte für die Prioritäts Klasse und die Prioritäts Ebene aufgeführt.



| Aufgaben *Priorität* | Prioritäts Klasse                 | Prioritätsstufe                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | Realtime \_ priority- \_ Klasse      | Thread \_ Prioritäts \_ Zeit \_ kritisch |
| 1               | Klasse mit hoher \_ Priorität \_          | Thread \_ Priorität \_ höchste        |
| 2               | oberhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ oberhalb des \_ normalen  |
| 3               | oberhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ oberhalb des \_ normalen  |
| 4               | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 5               | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 6               | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 7               | unterhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ unterhalb von \_ Normal  |
| 8               | unterhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ unterhalb von \_ Normal  |
| 9               | inaktive \_ Prioritäts \_ Klasse          | Thread \_ Priorität \_ niedrigste         |
| 10              | inaktive \_ Prioritäts \_ Klasse          | Thread \_ Priorität im \_ Leerlauf           |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Priority-Element [**(settingstype)**](taskschedulerschema-priority-settingstype-element.md) des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tasksettings**](tasksettings.md)
</dt> </dl>

 

