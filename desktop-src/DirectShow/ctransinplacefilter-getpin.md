---
description: 'CTransInPlaceFilter.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: CTransInPlaceFilter.GetPin-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4bef01168eb7bad9a1ffc8e5e8555ecd5e8804893269723c8dba72a066b3c50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079280"
---
# <a name="ctransinplacefiltergetpin-method"></a>CTransInPlaceFilter.GetPin-Methode

Die `GetPin` -Methode ruft einen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Nummer des angegebenen Pins, indiziert von 0 (null). Bei diesem Filter ist Stecknadel 0 der Eingabepin, und Pin 1 ist der Ausgabepin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das [**CBasePin-Objekt**](cbasepin.md) zurück, das den Pin implementiert, oder **NULL,** wenn die Methode fehlschlägt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CTransformFilter::GetPin-Methode.**](ctransformfilter-getpin.md) Beim ersten Aufruf der -Methode werden beide Stecknadeln erstellt.

Diese Methode erhöht den Verweiszähler für den zurückgegebenen Pin nicht, sodass der zurückgegebene Pin keinen ausstehenden Verweiszähler aufwies. Wenn der Aufrufer einen Verweis auf den Pin beibehalten muss, sollte er die **IUnknown::AddRef-Methode** auf dem Pin aufrufen.

Wenn der Filter die [**Standard-Pins CTransInPlaceInputPin**](ctransinplaceinputpin.md) und [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) verwendet, müssen Sie diese Methode wahrscheinlich nicht überschreiben. Wenn der Filter jedoch Pins verwendet, die diese Klassen erweitern, müssen Sie diese Methode überschreiben, um Pins dieses Typs zu erstellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




