---
description: Die GetMediaType-Methode ruft einen bevorzugten Medientyp ab.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: CSourceStream.GetMediaType-Methode (Source.h) – pMediaType-Parameter
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
ms.openlocfilehash: 2850d08726337f1ff43ad09319aea8b0af95d107ad9dad9c0f89ce94474c7261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073194"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>CSourceStream.GetMediaType-Methode (Source.h)

Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Index außerhalb des Bereichs.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index kleiner als 0 (null).<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Unerwarteter Fehler.<br/>     |



 

## <a name="remarks"></a>Hinweise

Es gibt zwei Versionen dieser Methode. Eine Version überschreibt die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) und verwendet einen Indexwert als Parameter. Die andere Version ist so konzipiert, dass ein einzelner Medientyp abgerufen wird, sodass der Indexparameter fehlt.

Die Einzelparametermethode gibt E \_ UNEXPECTED zurück. Die Methode mit zwei Parametern überprüft, ob der *iPosition-Parameter* 0 (null) ist, und ruft dann die Einzelparameterversion auf. Abhängig von der Anzahl von Medientypen, die der Pin unterstützt, müssen Sie eine der folgenden Methoden überschreiben:

-   Wenn der Pin genau einen Medientyp unterstützt, überschreiben Sie die Einzelparameterversion. Geben Sie den Medientyp ein, den der Pin unterstützt.
-   Wenn der Pin mehrere Medientypen unterstützt, überschreiben Sie die Zwei-Parameter-Version. Überschreiben Sie auch die [**CSourceStream::CheckMediaType-Methode.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




