---
description: Mit der get \_ avgtimeperframe-Methode wird die durchschnittliche Zeit pro Frame abgerufen.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: CBaseControlVideo.get_AvgTimePerFrame-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368410"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>Cbasecontrolvideo. get \_ avgtimeperframe-Methode

Die- `get_AvgTimePerFrame` Methode ruft die durchschnittliche Zeit pro Frame ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pavgtimeperframe* 
</dt> <dd>

Zeiger auf die durchschnittliche Zeit pro Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ avgtimeperframe**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) -Methode. Er ruft die reine virtuelle [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) -Member-Funktion auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




