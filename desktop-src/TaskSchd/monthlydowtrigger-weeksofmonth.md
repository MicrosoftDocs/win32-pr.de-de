---
title: Monthlydowauslöst. weeksofmonth (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochen des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Weeksofmonth-Eigenschaft Taskplaner
- Weeksofmonth-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, weeksofmonth (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475807"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>Monthlydowauslöst. weeksofmonth (Eigenschaft)

Ruft bei der Skripterstellung die Wochen des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.



| Woche                     | Hexadezimalwert | Dezimalwert |
|--------------------------|-----------|---------------|
| Erste Woche des Monats  | 0X01      | 1             |
| Zweite Woche des Monats | 0x02      | 2             |
| Dritte Woche des Monats  | 0X04      | 4             |
| Vierte Woche des Monats | 0X08      | 8             |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen [**Wochen**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) Tags durch das Week-Element angegeben.

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

 

 





