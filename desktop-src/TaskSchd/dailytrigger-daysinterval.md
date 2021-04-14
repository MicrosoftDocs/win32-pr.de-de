---
title: Dailydie. daysinterval (Eigenschaft)
description: Ruft bei der Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt es fest.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Daysinterval-Eigenschaft Taskplaner
- Daysinterval-Eigenschaft Taskplaner, dailyauslöserobjekt
- Dailyauslöserobjekt Taskplaner, daysinterval-Eigenschaft
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517915"
---
# <a name="dailytriggerdaysinterval-property"></a>Dailydie. daysinterval (Eigenschaft)

Ruft bei der Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt es fest.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Eigenschaftswert

Das Intervall zwischen den Tagen im Zeitplan.

## <a name="remarks"></a>Bemerkungen

Ein Intervall von 1 erzeugt einen täglichen Zeitplan. Ein Intervall von 2 erzeugt einen Zeitplan für jeden anderen Tag.

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Intervall für einen täglichen Zeitplan mit dem [**daysinterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.

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

[**Dailylöst**](dailytrigger.md)
</dt> </dl>

 

 





