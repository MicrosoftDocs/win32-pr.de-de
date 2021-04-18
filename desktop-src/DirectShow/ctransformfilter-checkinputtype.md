---
description: Die checkinputtype-Methode überprüft, ob ein angegebener Medientyp für die Eingabe zulässig ist.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Ctransformfilter. checkinputtype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357573"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Ctransformfilter. checkinputtype-Methode

Die- `CheckInputType` Methode überprüft, ob ein angegebener Medientyp für die Eingabe zulässig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MTiN* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                | Beschreibung                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Der Medientyp ist akzeptabel.<br/>     |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Der Medientyp ist nicht zulässig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss von der abgeleiteten Klasse implementiert werden. Gibt S \_ OK zurück, wenn das vorgeschlagene Eingabeformat zulässig ist, andernfalls einen Fehlercode.

Diese Methode muss nicht überprüfen, ob das Eingabeformat mit dem Ausgabeformat (sofern vorhanden) kompatibel ist. Die Eingabe-PIN überprüft dies durch Aufrufen der [**checktransform**](ctransformfilter-checktransform.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




