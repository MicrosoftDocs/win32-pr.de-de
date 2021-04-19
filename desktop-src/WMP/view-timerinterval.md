---
title: View. TimerInterval
description: Das TimerInterval-Attribut gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse für den OnTimer-Ereignishandler auslöst, oder ruft es ab.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- Ansicht. TimerInterval-Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352860"
---
# <a name="viewtimerinterval"></a>View. TimerInterval

Das **TimerInterval** -Attribut gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse für den **OnTimer** -Ereignishandler auslöst, oder ruft es ab.

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 1000. 



| Wert        | BESCHREIBUNG                    |
|--------------|--------------------------------|
| 0            | Das Timer-Ereignis wird nicht ausgelöst. |
| 50 und höher | Das Intervall in Millisekunden.  |



 

Jeder Wert unter 50 (einschließlich negativer Zahlen, aber nicht einschließlich 0) generiert einen Fehler, und der vorherige Wert wird beibehalten.

## <a name="remarks"></a>Bemerkungen

Dies wird nicht automatisch ausgelöst, wenn kein **OnTimer** -Ereignishandler implementiert ist. Folglich gibt es keine Leistungsminderung, obwohl der Standardwert ungleich 0 (null) ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> <dt>

[**View. OnTimer**](view-ontimer.md)
</dt> </dl>

 

 





