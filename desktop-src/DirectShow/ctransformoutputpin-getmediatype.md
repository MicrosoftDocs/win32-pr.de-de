---
description: 'CTransformOutputPin.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: CTransformOutputPin.GetMediaType-Methode (Transfrm.h)
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
ms.openlocfilehash: ddd064934eea6ef2c88a4304466b15811910e8e352041e7242c75650dd54b2a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812780"
---
# <a name="ctransformoutputpingetmediatype-method"></a>CTransformOutputPin.GetMediaType-Methode

Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp nach Indexwert ab.

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

Nullbasierter Indexwert.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                            | Beschreibung                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg<br/>            |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Index außerhalb des Bereichs<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::GetMediaType-Methode.**](cbasepin-getmediatype.md) Wenn der Eingabepin des Filters nicht verbunden ist, gibt die Methode VFW \_ S NO MORE ITEMS \_ \_ \_ zurück. Andernfalls wird die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) des Filters aufgerufen, um den Medientyp abzurufen. Die **CTransformFilter::GetMediaType-Methode** ist rein virtuell. Die abgeleitete Klasse des Filters muss sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




