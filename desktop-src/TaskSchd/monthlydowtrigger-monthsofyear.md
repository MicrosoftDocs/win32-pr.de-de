---
title: Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)
description: Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest. | Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- MONTHSOFYEAR-Eigenschaft Taskplaner
- MONTHSOFYEAR-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, MONTHSOFYEAR (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869979"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>Monthlydowauslöst. MONTHSOFYEAR (Eigenschaft)

Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Monate des Jahres angibt, in dem die Aufgabe ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.



| Monat     | Farbtonwert | Dezimalzahl |
|-----------|-----------|---------------|
| January   | 0X01      | 1             |
| Februar  | 0x02      | 2             |
| März     | 0X04      | 4             |
| April     | 0X08      | 8             |
| May       | 0X10      | 16            |
| June      | 0X20      | 32            |
| Juli      | 0x40      | 64            |
| August    | 0X80      | 128           |
| September | 0X100     | 256           |
| Oktober   | 0X200     | 512           |
| November  | 0X400     | 1024          |
| Dezember  | 0X800     | 2048          |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Monate des Jahres eines monatlichen wochentags im Taskplaner Schema durch das [**Monate**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) -Element angegeben.

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

 

 





