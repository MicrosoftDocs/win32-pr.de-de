---
title: DailyTrigger.DaysInterval-Eigenschaft
description: Ruft für die Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt dieses fest.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- DaysInterval-Eigenschaft Taskplaner
- DaysInterval-Eigenschaft Taskplaner , DailyTrigger-Objekt
- DailyTrigger-Objekt Taskplaner , DaysInterval-Eigenschaft
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
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139493"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger.DaysInterval-Eigenschaft

Ruft für die Skripterstellung das Intervall zwischen den Tagen im Zeitplan ab oder legt dieses fest.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Eigenschaftswert

Das Intervall zwischen den Tagen im Zeitplan.

## <a name="remarks"></a>Hinweise

Ein Intervall von 1 erzeugt einen täglichen Zeitplan. Ein Intervall von 2 erzeugt einen Zeitplan für jeden zweiten Tag.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird das Intervall für einen täglichen Zeitplan mithilfe des [**DaysInterval-Elements**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) des Taskplaner Schemas angegeben.

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

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





