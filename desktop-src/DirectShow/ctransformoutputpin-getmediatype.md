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
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094898"
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

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                            | Beschreibung                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg<br/>            |
| <dl> <dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt> </dl> | Index liegt nicht im Bereich<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::GetMediaType-Methode.**](cbasepin-getmediatype.md) Wenn der Eingabepin des Filters nicht verbunden ist, gibt die Methode VFW \_ S NO MORE ITEMS \_ \_ \_ zurück. Andernfalls wird die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) des Filters aufgerufen, um den Medientyp abzurufen. Die **CTransformFilter::GetMediaType-Methode** ist rein virtuell. Die abgeleitete Klasse des Filters muss sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




