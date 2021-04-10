---
title: Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)
description: Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest. | Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- MONTHSOFYEAR-Eigenschaft Taskplaner
- MONTHSOFYEAR-Eigenschaft Taskplaner, Monthly-Auslöserobjekt
- Monthly-Auslöserobjekt Taskplaner, MONTHSOFYEAR (Eigenschaft)
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
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869879"
---
# <a name="monthlytriggermonthsofyear-property"></a>Monthly-Eigenschaft. MONTHSOFYEAR (Eigenschaft)

Ruft bei der Skripterstellung die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.MonthsOfYear As short
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



 

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden die Monate des Jahres mit dem Element [**Monate**](taskschedulerschema-months-monthlyscheduletype-element.md) des Taskplaner Schemas angegeben.

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
</dt> <dt>

[**Monthly-auslöst**](monthlytrigger.md)
</dt> </dl>

 

 





