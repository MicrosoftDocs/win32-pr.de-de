---
description: Die IsEndOfStreamDelivered-Methode fragt ab, ob das \_ EC COMPLETE-Ereignis an den Filterdiagramm-Manager übermittelt wurde.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: CBaseRenderer.IsEndOfStreamDelivered-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f15c2bca14e6c0f55f46441bbb4de362e6375d0b67f3012a4ad234a9366b188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954879"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>CBaseRenderer.IsEndOfStreamDelivered-Methode

Die `IsEndOfStreamDelivered` -Methode fragt ab, ob das EC \_ COMPLETE-Ereignis an den Filterdiagramm-Manager übermittelt wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das [**Flag CBaseRenderer::m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




