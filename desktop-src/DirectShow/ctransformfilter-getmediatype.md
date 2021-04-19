---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Ctransformfilter. getmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361634"
---
# <a name="ctransformfiltergetmediatype-method"></a>Ctransformfilter. getmediatype-Methode

Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPosition* 
</dt> <dd>

NULL basierter Indexwert.

</dd> <dt>

*pmediatype* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt> </dl> | Der Index liegt außerhalb des zulässigen Bereichs.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>           | Index kleiner als 0 (null).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die [**ctransformoutputpin:: getmediatype**](ctransformoutputpin-getmediatype.md) -Methode der Ausgabe-PIN ruft diese Methode auf. Diese Methode muss von der abgeleiteten Klasse implementiert werden. Weitere Informationen finden Sie unter [**cbasepin:: getmediatype**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




