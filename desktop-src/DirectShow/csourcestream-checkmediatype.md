---
description: 'Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. Diese Methode implementiert die rein virtuelle cbasepin:: checkmediatype-Methode.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Csourcestream. checkmediatype-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355924"
---
# <a name="csourcestreamcheckmediatype-method"></a>Csourcestream. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. Diese Methode implementiert die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediatype* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                            | Beschreibung                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Diese PIN unterstützt diesen Medientyp.<br/>        |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Dieser Medientyp wird von der PIN nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Standardmäßig unterstützt die PIN einen einzelnen Medientyp. Diese Methode ruft den unterstützten Typ durch Aufrufen der Einzel Parameter Version der [**csourcestream:: getmediatype**](csourcestream-getmediatype.md) -Methode ab und vergleicht sie mit dem vorgeschlagenen Typ. Wenn Ihre PIN mehr als einen Medientyp unterstützt, überschreiben Sie diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




