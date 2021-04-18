---
description: Die get \_ framesgezeichnet-Methode ruft die m \_ cframesdrawn-Element Variable ab und gibt so die Anzahl der Rahmen an, die seit dem Start des Streaming gezeichnet wurden.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get_FramesDrawn-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371035"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>Cbasevideorenderer. get \_ framesgezeichnet-Methode

Die- `get_FramesDrawn` Methode ruft die **m \_ cframesdrawn** -Element Variable ab und gibt die Anzahl der Rahmen an, die seit dem Start des Streamings gezeichnet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcframesdrawn* 
</dt> <dd>

Ein Zeiger auf die Anzahl der gezeichneten Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualprop:: get \_ framesgezeichnet**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




