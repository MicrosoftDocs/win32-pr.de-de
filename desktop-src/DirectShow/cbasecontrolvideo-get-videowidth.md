---
description: Die get \_ VideoWidth-Methode ruft die Breite des nativen Videos ab.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: CBaseControlVideo.get_VideoWidth-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268316dd9b7f37894f60ed45878c7de9bbc8d379301daa7bbefedcadd0b8e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661377"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>CBaseControlVideo.get \_ VideoWidth-Methode

Die `get_VideoWidth` -Methode ruft die Breite des nativen Videos ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoWidth* 
</dt> <dd>

Zeiger auf die Breite des nativen Videos in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück, wenn erfolgreich, oder E \_ OUTOFMEMORY, wenn nicht genügend Arbeitsspeicher verfügbar ist.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IBasicVideo::get \_ VideoWidth-Methode.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) Sie ruft das rein virtuelle [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




