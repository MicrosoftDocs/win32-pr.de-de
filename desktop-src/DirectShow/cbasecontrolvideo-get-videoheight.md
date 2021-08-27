---
description: Die get \_ VideoHeight-Methode ruft die Höhe des nativen Videos ab.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057080"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>CBaseControlVideo.get \_ VideoHeight-Methode

Die `get_VideoHeight` -Methode ruft die Höhe des nativen Videos ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

Zeiger auf die Höhe des nativen Videos in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück, wenn erfolgreich, oder E \_ OUTOFMEMORY, wenn nicht genügend Arbeitsspeicher verfügbar ist.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IBasicVideo::get \_ VideoHeight-Methode.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) Sie ruft das rein virtuelle [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




