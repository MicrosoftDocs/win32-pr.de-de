---
description: Die get \_ videowidth-Methode ruft die Breite des systemeigenen Videos ab.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: CBaseControlVideo.get_VideoWidth-Methode (ctlutil. h)
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
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365850"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>Cbasecontrolvideo. get \_ videowidth-Methode

Die- `get_VideoWidth` Methode ruft die Breite des systemeigenen Videos ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideowidth* 
</dt> <dd>

Zeiger auf die Breite des nativen Videos in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ videowidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) -Methode. Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




