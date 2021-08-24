---
title: MonthlyDOWTrigger.DaysOfWeek (Eigenschaft)
description: Für die Skripterstellung ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek-Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner , MonthlyDOWTrigger-Objekt
- MonthlyDOWTrigger-Objekt Taskplaner , DaysOfWeek-Eigenschaft
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
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517460"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger.DaysOfWeek (Eigenschaft)

Für die Skripterstellung ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen der Task ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Zuordnung der bitweise Maske, die von dieser Eigenschaft verwendet wird.



| Tag der Woche | Hexadezimalwert | Dezimalwert |
|-------------|-----------|---------------|
| Sonntag      | 0x01      | 1             |
| Montag      | 0x02      | 2             |
| Tuesday     | 0x04      | 4             |
| Wednesday   | 0x08      | 8             |
| Thursday    | 0x10      | 16            |
| Freitag      | 0x20      | 32            |
| Samstag    | 0x40      | 64            |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen Wochentagskalenders durch das [**DaysOfWeek-Element**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





