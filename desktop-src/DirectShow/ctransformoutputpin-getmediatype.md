---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Ctransformoutputpin. getmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365557"
---
# <a name="ctransformoutputpingetmediatype-method"></a>Ctransformoutputpin. getmediatype-Methode

Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp nach Indexwert ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
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



| Rückgabecode                                                                                            | Beschreibung                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg<br/>            |
| <dl> <dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt> </dl> | Index außerhalb des gültigen Bereichs<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode. Wenn die Eingabe-PIN des Filters nicht verbunden ist, gibt die Methode VFW \_ s \_ keine \_ weiteren \_ Elemente zurück. Andernfalls wird die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode des Filters aufgerufen, um den Medientyp abzurufen. Die **ctransformfilter:: getmediatype** -Methode ist rein virtuell. die von der abgeleitete Klasse des Filters muss Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




