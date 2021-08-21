---
title: WeeklyTrigger.DaysOfWeek (Eigenschaft)
description: Für Die Skripterstellung ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek-Taskplaner
- DaysOfWeek-Eigenschaft Taskplaner , WeeklyTrigger-Objekt
- WeeklyTrigger-Objekt Taskplaner , DaysOfWeek-Eigenschaft
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
ms.openlocfilehash: 7298982dcd10078d9e8460459d38cfa77140d15607341460f0e0edec998306f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001793"
---
# <a name="weeklytriggerdaysofweek-property"></a>WeeklyTrigger.DaysOfWeek (Eigenschaft)

Für Die Skripterstellung ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen der Task ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Zuordnung der bitweise Maske, die von dieser Eigenschaft verwendet wird.



| Month (Monat)     | Farbtonwert | Dezimalzahl |
|-----------|-----------|---------------|
| Sonntag    | 0X01      | 1             |
| Montag    | 0x02      | 2             |
| Tuesday   | 0X04      | 4             |
| Wednesday | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| Freitag    | 0x20      | 32            |
| Samstag  | 0X40      | 64            |



 

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe werden die Wochentage mithilfe des [**DaysOfWeek-Elements**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





