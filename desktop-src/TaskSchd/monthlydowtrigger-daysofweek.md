---
title: Monthlydowauslöst. DaysOfWeek (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochentage ab, an denen die Aufgabe ausgeführt wird, oder legt diese fest.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek-Eigenschaft Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, DaysOfWeek (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478417"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>Monthlydowauslöst. DaysOfWeek (Eigenschaft)

Ruft bei der Skripterstellung die Wochentage ab, an denen die Aufgabe ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.



| Tag der Woche | Hexadezimalwert | Dezimalwert |
|-------------|-----------|---------------|
| Sonntag      | 0x01      | 1             |
| Montag      | 0x02      | 2             |
| Tuesday     | 0x04      | 4             |
| Wednesday   | 0x08      | 8             |
| Thursday    | 0x10      | 16            |
| Freitag      | 0x20      | 32            |
| Samstag    | 0x40      | 64            |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen wochentags mit dem [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) -Element angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Monthlydowlöst**](monthlydowtrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





