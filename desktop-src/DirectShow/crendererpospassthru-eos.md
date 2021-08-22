---
description: Die EOS-Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Benachrichtigung über das Ende des Streams.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: CRendererPosPassThru.EOS-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10f87fbb66f8ad1d89ff31c6653780b3fde23ecbaf55d72b6f3de2f59546b49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073414"
---
# <a name="crendererpospassthrueos-method"></a>CRendererPosPassThru.EOS-Methode

Die `EOS` -Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Benachrichtigung über das Ende des Streams.

## <a name="syntax"></a>Syntax


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                            | Beschreibung                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler. Möglicherweise wird der Filter nicht gestreamt.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Filter sollte diese Methode aufrufen, wenn er eine End-of-Stream-Benachrichtigung empfängt ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). Die -Methode legt beide zwischengespeicherten Zeitstempel auf die Stoppposition fest und stellt sicher, dass die [**IMediaSeeking:: GetCurrentPosition-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) am Ende des Streams die richtigen Werte zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




