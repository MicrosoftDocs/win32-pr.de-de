---
description: Die SetTimeAdvise-Methode richtet ein Timerereignis mit der Referenzuhr ein.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: CCmdQueue.SetTimeAdvise-Methode (Winutil.h)
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
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757130"
---
# <a name="ccmdqueuesettimeadvise-method"></a>CCmdQueue.SetTimeAdvise-Methode

Die `SetTimeAdvise` -Methode richtet ein Timerereignis mit der Referenzuhr ein.

## <a name="syntax"></a>Syntax


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft die [**IReferenceClock::AdviseTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) auf, um eine Benachrichtigung so früh wie möglich in der Warteschlange einrichten zu können. Verzögerte Präsentationszeitbefehle werden immer überprüft. Wenn sich das Filterdiagramm im Ausführungsmodus befindet, werden auch verzögerte Befehle mit Streamzeit überprüft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




