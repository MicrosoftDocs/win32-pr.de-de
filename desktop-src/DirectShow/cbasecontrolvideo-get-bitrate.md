---
description: Die get \_ BitRate-Methode ruft eine ungefähre Bitrate für das Video ab.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: CBaseControlVideo.get_BitRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b33e3584bb0460b798101d8062c3647b983841c77653adcffd18580eade25c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057270"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>\_CBaseControlVideo.get-BitRate-Methode

Die `get_BitRate` -Methode ruft eine ungefähre Bitrate für das Video ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBitRate* 
</dt> <dd>

Zeiger auf die Bitrate in Bits pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück, wenn erfolgreich, oder E \_ OUTOFMEMORY, wenn nicht genügend Arbeitsspeicher verfügbar ist.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IBasicVideo::get \_ BitRate-Methode.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) Sie ruft das rein virtuelle [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




