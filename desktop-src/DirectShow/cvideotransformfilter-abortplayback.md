---
description: Die abortplayback-Methode wird verwendet, um einen Streamingfehler zu signalisieren. Es sendet ein EC \_ errorabort-Ereignis an den Filter Graph-Manager und sendet eine downstreambenachrichtigung.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Cvideotransformfilter. abortplayback-Methode (vtrans. h)
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
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353794"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Cvideotransformfilter. abortplayback-Methode

Die- `AbortPlayback` Methode wird verwendet, um einen Streamingfehler zu signalisieren. Es sendet ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an den Filter Graph-Manager und sendet eine downstreambenachrichtigung.

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

**HRESULT** -Wert des Vorgangs, bei dem ein Fehler aufgetreten ist. Dieser Wert wird als erster Ereignis Parameter für das EC \_ errorabort-Ereignis verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des *HR* -Parameters zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




