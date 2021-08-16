---
description: Die AbortPlayback-Methode wird verwendet, um einen Streamingfehler zu signalisieren. Es sendet ein EC \_ ERRORABORT-Ereignis an den Filter-Graph-Manager und sendet eine End-of-Stream-Benachrichtigung nachgeschaltet.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: CVideoTransformFilter.AbortPlayback-Methode (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821935"
---
# <a name="cvideotransformfilterabortplayback-method"></a>CVideoTransformFilter.AbortPlayback-Methode

Die `AbortPlayback` -Methode wird verwendet, um einen Streamingfehler zu signalisieren. Es sendet ein [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) an den Filter Graph Manager und sendet eine End-of-Stream-Benachrichtigung nachgeschaltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Std.* 
</dt> <dd>

**HRESULT-Wert** des fehlgeschlagenen Vorgangs. Dieser Wert wird als erster Ereignisparameter für das EC \_ ERRORABORT-Ereignis verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des *hr-Parameters* zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (einschließlich Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




