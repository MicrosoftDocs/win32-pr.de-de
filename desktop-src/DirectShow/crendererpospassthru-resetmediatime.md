---
description: Die ResetMediaTime-Methode setzt die zwischengespeicherten Zeitstempel auf null zurück.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: CRendererPosPassThru.ResetMediaTime-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1babc39ad3329ec18be663ffcc6eb882933bead0be5f631ef82ce363391f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953813"
---
# <a name="crendererpospassthruresetmediatime-method"></a>CRendererPosPassThru.ResetMediaTime-Methode

Die `ResetMediaTime` -Methode setzt die zwischengespeicherten Zeitstempel auf 0 zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der Filter sollte diese Methode aufrufen, wenn die von der [**CRendererPosPassThru::RegisterMediaTime-Methode**](crendererpospassthru-registermediatime.md) zwischengespeicherten Zeitstempel ungültig werden. Insbesondere sollte diese Methode als Antwort auf die [**Methoden IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) und [**IMediaFilter::Stop aufgerufen**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) werden.

Nachdem diese Methode aufgerufen wurde, gibt die [**CRendererPosPassThru::GetMediaTime-Methode**](crendererpospassthru-getmediatime.md) 0 (null) für die Start- und Endzeiten zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




