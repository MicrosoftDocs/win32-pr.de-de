---
description: Die get \_ Bitrate-Methode ruft eine ungefähre Bitrate für das Video ab.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: CBaseControlVideo.get_BitRate-Methode (ctlutil. h)
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
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371094"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>Cbasecontrolvideo. get- \_ Bitrate-Methode

Die- `get_BitRate` Methode ruft eine ungefähre Bitrate für das Video ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbitrate* 
</dt> <dd>

Zeiger auf die Bitrate in Bits pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ Bitrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) -Methode. Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




