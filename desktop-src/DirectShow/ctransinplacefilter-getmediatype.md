---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Ctransinplacefilter. getmediatype-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365998"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Ctransinplacefilter. getmediatype-Methode

Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.

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

Gibt "E unerwartete" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode. In der **ctransinplacefilter** -Klasse ruft jede PIN die entgegengesetzte verbundene PIN auf, um bevorzugte Medientypen aufzuzählen. Die Eingabe-PIN Ruft die Eingabe-PIN des downstreamfilters auf, und die Ausgabe-PIN Ruft die Ausgabepin des Upstream-Filters auf. Daher wird die-Methode des Filters `GetMediaType` nie aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




