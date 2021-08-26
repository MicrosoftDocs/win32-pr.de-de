---
title: VIEW.timerInterval
description: Das timerInterval-Attribut gibt das Intervall in Millisekunden an, in dem der Timer Ereignisse an den ontimer-Ereignishandler ausgibt oder abruft.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW.timerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43b2b7bbd87663a35c43db733d3e11ff0dca5bc3ddfd00e57022b4df7122c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001310"
---
# <a name="viewtimerinterval"></a>VIEW.timerInterval

Das **timerInterval-Attribut** gibt das Intervall in Millisekunden an, in dem der Timer Ereignisse an den **ontimer-Ereignishandler** ausgibt oder abruft.

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibnummer **(long**) mit dem Standardwert 1000.



| Wert        | Beschreibung                    |
|--------------|--------------------------------|
| 0            | Das Timerereignis wird nicht ausgelöst. |
| 50 und höher | Das Intervall in Millisekunden.  |



 

Jeder Wert unter 50 (einschließlich negativer Zahlen, aber nicht einschließlich Null) generiert einen Fehler, und der vorherige Wert wird beibehalten.

## <a name="remarks"></a>Hinweise

Dies wird nicht automatisch ausgelöst, wenn kein **ontimer-Ereignishandler** implementiert ist. Daher gibt es keine Leistungsbeeinträchtigung, auch wenn der Standardwert ungleich 0 (null) ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> <dt>

[**VIEW.ontimer**](view-ontimer.md)
</dt> </dl>

 

 





