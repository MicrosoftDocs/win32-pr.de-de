---
title: MonthlyTrigger.MonthsOfYear-Eigenschaft
description: Ruft für die Skripterstellung die Monate des Jahres ab, in denen der Task ausgeführt wird, oder legt diese fest. | MonthlyTrigger.MonthsOfYear-Eigenschaft
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- MonthsOfYear-Eigenschaft Taskplaner
- MonthsOfYear-Eigenschaft Taskplaner , MonthlyTrigger-Objekt
- MonthlyTrigger-Objekt Taskplaner , MonthsOfYear-Eigenschaft
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff6f08e257acf85a8a3f073f43c3c81e65817900f8154e1701ab73fe10c2368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253780"
---
# <a name="monthlytriggermonthsofyear-property"></a>MonthlyTrigger.MonthsOfYear-Eigenschaft

Ruft für die Skripterstellung die Monate des Jahres ab, in denen der Task ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Eigenschaftswert

Eine bitweise Maske, die die Monate des Jahres angibt, in denen der Task ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.



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



 

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe werden die Monate des Jahres mithilfe des [**Months-Elements**](taskschedulerschema-months-monthlyscheduletype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





