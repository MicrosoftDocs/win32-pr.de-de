---
description: Die get \_ videoheight-Methode ruft die Höhe des nativen Videos ab.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight-Methode (ctlutil. h)
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
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366051"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Cbasecontrolvideo. get \_ videoheight-Methode

Die- `get_VideoHeight` Methode ruft die Höhe des nativen Videos ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideoheight* 
</dt> <dd>

Zeiger auf die Höhe des nativen Videos in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ videoheight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) -Methode. Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




