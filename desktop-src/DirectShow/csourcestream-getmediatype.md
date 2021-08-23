---
description: Die GetMediaType-Methode ruft einen bevorzugten Medientyp ab. Diese Methode verwendet die *Parameter iPosition* und *pMediaType.*
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: CSourceStream.GetMediaType-Methode (Source.h) – iPosition- und pMediaType-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073254"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>CSourceStream.GetMediaType-Methode (Source.h) – iPosition- und pMediaType-Parameter

Die **GetMediaType-Methode** ruft einen bevorzugten Medientyp ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
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

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt> </dl> | Index liegt nicht im Bereich.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index kleiner als 0 (null).<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Unerwarteter Fehler.<br/>     |



 

## <a name="remarks"></a>Hinweise

Es gibt zwei Versionen dieser Methode. Eine Version überschreibt die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) und akzeptiert einen Indexwert als Parameter. Die andere Version ist so konzipiert, dass ein einzelner Medientyp abgerufen wird, sodass der Indexparameter fehlt.

Die Einzelparametermethode gibt E \_ UNEXPECTED zurück. Die Methode mit zwei Parametern überprüft, ob der *iPosition-Parameter* 0 (null) ist, und ruft dann die Einzelparameterversion auf. Abhängig von der Anzahl der Medientypen, die der Pin unterstützt, müssen Sie eine der folgenden Methoden überschreiben:

-   Wenn der Pin genau einen Medientyp unterstützt, überschreiben Sie die Einzelparameterversion. Geben Sie den Medientyp ein, den der Pin unterstützt.
-   Wenn der Pin mehrere Medientypen unterstützt, überschreiben Sie die Version mit zwei Parametern. Überschreiben Sie auch [**die CSourceStream::CheckMediaType-Methode.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Source.h (include Streams.h)                                                                                    |
| Bibliothek | Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




