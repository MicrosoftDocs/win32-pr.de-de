---
description: Die settimereference-Methode richtet ein Zeit Geber Ereignis mit der Referenzuhr ein.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Ccmdqueue. settimeempfehlung-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364408"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Ccmdqueue. settimeempfehlung-Methode

Die- `SetTimeAdvise` Methode richtet ein Timer-Ereignis mit der Referenzuhr ein.

## <a name="syntax"></a>Syntax


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion Ruft die [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode auf, um eine Benachrichtigung für den frühesten Zeitraum einzurichten, der in der Warteschlange erforderlich ist. Zurück gestellte Präsentationszeit Befehle sind immer aktiviert. Wenn sich das Filter Diagramm im laufenden Modus befindet, werden auch verzögerte Befehle mit streamzeit geprüft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




