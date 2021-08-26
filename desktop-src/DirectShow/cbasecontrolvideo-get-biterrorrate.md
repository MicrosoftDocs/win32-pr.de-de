---
description: Die get \_ BitErrorRate-Methode ruft eine ungefähre Bitfehlerrate für das Video ab.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate -Methode (Ctlutil.h)
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
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057290"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>CBaseControlVideo.get \_ BitErrorRate-Methode

Die `get_BitErrorRate` -Methode ruft eine ungefähre Bitfehlerrate für das Video ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

Zeiger auf die Bitfehlerrate (ein Fehler für ungefähr so viele Bits).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück, wenn erfolgreich, oder E \_ OUTOFMEMORY, wenn nicht genügend Arbeitsspeicher verfügbar ist.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IBasicVideo::get \_ BitErrorRate-Methode.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) Sie ruft die rein virtuelle [**CBaseControlVideo::GetVideoFormat-Methode**](cbasecontrolvideo-getvideoformat.md) auf, um die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) aus der abgeleiteten Klasse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




