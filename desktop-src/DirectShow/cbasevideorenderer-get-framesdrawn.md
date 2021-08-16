---
description: Die get \_ FramesDrawn-Methode ruft die m \_ cFramesDrawn-Membervariable ab und gibt die Anzahl der Frames an, die seit dem Streaming gezeichnet wurden.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get_FramesDrawn-Methode (Renbase.h)
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
ms.openlocfilehash: 65a7c698d129a3606f6ba75f856289ca2b4e15c438d3890eb0a97e4a198ee808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822583"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>CBaseVideoRenderer.get \_ FramesDrawn-Methode

Die `get_FramesDrawn` -Methode ruft die **m \_ cFramesDrawn-Membervariable ab** und gibt die Anzahl der Frames an, die seit dem Streaming gezeichnet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcFramesDrawn* 
</dt> <dd>

Zeiger auf die Anzahl der gezeichneten Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IQualProp::get \_ FramesDrawn-Methode.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




