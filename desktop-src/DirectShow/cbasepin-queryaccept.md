---
description: Die QueryAccept-Methode bestimmt, ob der Pin einen angegebenen Medientyp akzeptiert. Diese Methode implementiert die IPin::QueryAccept-Methode.
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: CBasePin.QueryAccept-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74a179fd1a7f59dcf4e4d22eadf509db9b00cbe482d55e6a6755d7207de8079d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689000"
---
# <a name="cbasepinqueryaccept-method"></a>CBasePin.QueryAccept-Methode

Die `QueryAccept` -Methode bestimmt, ob der Pin einen angegebenen Medientyp akzeptiert. Diese Methode implementiert die [**IPin::QueryAccept-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Medientyp akzeptabel ist. Andernfalls wird S \_ FALSE zurückgegeben.

## <a name="remarks"></a>Hinweise

In der Basisklasse delegiert diese Methode an die [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md) Wenn **CheckMediaType fehlschlägt,** `QueryAccept` gibt S FALSE \_ zurück.

Diese Methode enthält nicht den kritischen Abschnitt des Pins ([**CBasePin::m \_ pLock**](cbasepin-m-plock.md)). Wenn die abgeleitete Klasse den Satz zulässiger Medientypen dynamisch ändert, sollten Sie diese Methode überschreiben, um den kritischen Abschnitt zu enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




