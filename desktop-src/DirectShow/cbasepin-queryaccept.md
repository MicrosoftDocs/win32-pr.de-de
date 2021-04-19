---
description: 'Die queryaccept-Methode bestimmt, ob die PIN einen angegebenen Medientyp akzeptiert. Diese Methode implementiert die IPin:: queryaccept-Methode.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Cbasepin. queryaccept-Methode (amfilter. h)
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
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360446"
---
# <a name="cbasepinqueryaccept-method"></a>Cbasepin. queryaccept-Methode

Die- `QueryAccept` Methode bestimmt, ob die PIN einen angegebenen Medientyp akzeptiert. Diese Methode implementiert die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Medientyp zulässig ist. Andernfalls gibt S \_ false zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse delegiert diese Methode an die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode. Wenn **checkmediatype** fehlschlägt, `QueryAccept` gibt S \_ false zurück.

Diese Methode enthält nicht den kritischen Abschnitt der PIN ([**cbasepin:: m \_ Plock**](cbasepin-m-plock.md)). Wenn die abgeleitete Klasse den Satz zulässiger Medientypen dynamisch ändert, sollten Sie diese Methode überschreiben, um den kritischen Abschnitt zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




