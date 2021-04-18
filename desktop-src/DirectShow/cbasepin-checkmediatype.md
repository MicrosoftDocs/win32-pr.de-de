---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Cbasepin. checkmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358755"
---
# <a name="cbasepincheckmediatype-method"></a>Cbasepin. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp zulässig ist. Andernfalls gibt S \_ false oder einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Die abgeleitete Klasse muss diese reine virtuelle Methode überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




