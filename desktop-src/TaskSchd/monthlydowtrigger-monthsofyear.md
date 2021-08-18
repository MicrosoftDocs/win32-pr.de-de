---
title: MonthlyDOWTrigger.MonthsOfYear -Eigenschaft
description: Für die Skripterstellung ruft die Monate des Jahres ab, in denen der Task ausgeführt wird, oder legt diese fest. | MonthlyDOWTrigger.MonthsOfYear -Eigenschaft
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- MonthsOfYear-Taskplaner
- MonthsOfYear-Eigenschaft Taskplaner , MonthlyDOWTrigger-Objekt
- MonthlyDOWTrigger-Objekt Taskplaner , MonthsOfYear-Eigenschaft
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
ms.openlocfilehash: 7f8dc9752cf241218a95a9816824bc6ccf560f47c3445df9e5f40406381de3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253820"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>MonthlyDOWTrigger.MonthsOfYear -Eigenschaft

Für die Skripterstellung ruft die Monate des Jahres ab, in denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Monate des Jahres angibt, in denen der Task ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Zuordnung der bitweise Maske, die von dieser Eigenschaft verwendet wird.



| Month (Monat)     | Farbtonwert | Dezimalzahl |
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



 

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Monate des Jahres eines monatlichen Wochentagskalenders durch das [**Months-Element**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





