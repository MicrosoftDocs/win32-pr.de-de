---
description: Die get \_ biterrorrate-Methode ruft eine ungefähre Bitfehlerrate für das Video ab.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356456"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Cbasecontrolvideo. get \_ biterrorrate-Methode

Die- `get_BitErrorRate` Methode ruft eine ungefähre Bitfehlerrate für das Video ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbiterrorrate* 
</dt> <dd>

Zeiger auf die Bitfehlerrate (ein Fehler für ungefähr diese viele Bits).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ biterrorrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) -Methode. Sie ruft die rein virtuelle [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) -Methode auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




