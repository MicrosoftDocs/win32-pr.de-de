---
description: 'CTransformFilter.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: CTransformFilter.GetMediaType-Methode (Transfrm.h)
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
ms.openlocfilehash: 9b471ac42ceb44f5e65a2ac08365bf97ab0e3157816b772b331cde0fa0b13bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907530"
---
# <a name="ctransformfiltergetmediatype-method"></a>CTransformFilter.GetMediaType-Methode

Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.

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

Nullbasierter Indexwert.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt> </dl> | Index liegt nicht im Bereich.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index kleiner als 0 (null).<br/> |



 

## <a name="remarks"></a>Hinweise

Die [**CTransformOutputPin::GetMediaType-Methode**](ctransformoutputpin-getmediatype.md) des Ausgabepins ruft diese Methode auf. Die abgeleitete Klasse muss diese Methode implementieren. Weitere Informationen finden Sie unter [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




