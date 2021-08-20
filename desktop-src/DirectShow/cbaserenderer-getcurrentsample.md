---
description: Die GetCurrentSample-Methode ruft das aktuelle Beispiel ab.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: CBaseRenderer.GetCurrentSample-Methode (Renbase.h)
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
ms.openlocfilehash: 5ffe3cdf95d5ab248956e670c04572140fa4621fff5b0cb5183f9a7cbd9b837e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822721"
---
# <a name="cbaserenderergetcurrentsample-method"></a>CBaseRenderer.GetCurrentSample-Methode

Die `GetCurrentSample` -Methode ruft das aktuelle Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels oder **NULL** zurück, wenn kein Beispiel verfügbar ist.

## <a name="remarks"></a>Hinweise

Sofern die Methode nicht **NULL** zurückgibt, ruft die Methode **AddRef** für den [**IMediaSample-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-imediasample) auf, bevor sie sie zurückgibt. Der Aufrufer muss den Zeiger freigeben. (ImPlizierend müssen Sie den Rückgabewert einer Variablen zuweisen, damit Sie ihn später freigeben können.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




