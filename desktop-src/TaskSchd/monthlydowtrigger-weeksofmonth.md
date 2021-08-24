---
title: MonthlyDOWTrigger.WeeksOfMonth (Eigenschaft)
description: Für die Skripterstellung ruft die Wochen des Monats ab, in denen der Task ausgeführt wird, oder legt diese fest.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- WeeksOfMonth-Taskplaner
- WeeksOfMonth-Eigenschaft Taskplaner , MonthlyDOWTrigger-Objekt
- MonthlyDOWTrigger-Objekt Taskplaner , WeeksOfMonth-Eigenschaft
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
ms.openlocfilehash: 323ee8b93411d7ef176fa9dc2ffb3a4acfd1f902c0dc481fe48e07b82821227b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517440"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>MonthlyDOWTrigger.WeeksOfMonth (Eigenschaft)

Für die Skripterstellung ruft die Wochen des Monats ab, in denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Wochentage angibt, an denen der Task ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Zuordnung der bitweise Maske, die von dieser Eigenschaft verwendet wird.



| Woche                     | Hexadezimalwert | Dezimalwert |
|--------------------------|-----------|---------------|
| Erste Woche des Monats  | 0X01      | 1             |
| Zweite Woche des Monats | 0x02      | 2             |
| Dritte Woche des Monats  | 0X04      | 4             |
| Vierte Woche des Monats | 0X08      | 8             |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen Wochentagskalenders durch das [**Weeks-Element**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) angegeben.

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

 

 





