---
description: Die getcurrentsample-Methode ruft das aktuelle Beispiel ab.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Cbaserderderer. getcurrentsample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371173"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Cbaserderderer. getcurrentsample-Methode

Die- `GetCurrentSample` Methode ruft das aktuelle Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels zurück, oder **null** , wenn keine Stichprobe verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode nicht **null** zurückgibt, ruft die Methode vor der Rückgabe die Methode " **adressf** " für den [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeiger auf. Der Aufrufer muss den Zeiger freigeben. (Implizit müssen Sie den Rückgabewert einer Variablen zuweisen, damit Sie Sie später freigeben können.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




