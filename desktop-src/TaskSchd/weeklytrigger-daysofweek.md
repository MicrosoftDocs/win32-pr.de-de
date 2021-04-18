---
title: Weeklyauslöst. DaysOfWeek (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek-Eigenschaft Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner, weeklyauslöserobjekt
- Weeklyauslöserobjekt Taskplaner, DaysOfWeek (Eigenschaft)
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519255"
---
# <a name="weeklytriggerdaysofweek-property"></a>Weeklyauslöst. DaysOfWeek (Eigenschaft)

Ruft bei der Skripterstellung die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.



| Monat     | Farbtonwert | Dezimalzahl |
|-----------|-----------|---------------|
| Sonntag    | 0X01      | 1             |
| Montag    | 0x02      | 2             |
| Tuesday   | 0X04      | 4             |
| Wednesday | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| Freitag    | 0x20      | 32            |
| Samstag  | 0X40      | 64            |



 

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden die Wochentage mit dem [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





