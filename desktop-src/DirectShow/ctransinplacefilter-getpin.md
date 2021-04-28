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
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084768"
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

Die Nummer des angegebenen Pins, indiziert von 0 (null). Bei diesem Filter ist Pin 0 der Eingabepin und Pin 1 der Ausgabepin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das [**CBasePin-Objekt**](cbasepin.md) zurück, das den Pin implementiert, oder **NULL,** wenn die Methode fehlschlägt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CTransformFilter::GetPin-Methode.**](ctransformfilter-getpin.md) Wenn die -Methode zum ersten Mal aufgerufen wird, werden beide Pins erstellt.

Diese Methode erhöht den Verweiszähler für den zurückgegebenen Pin nicht, sodass der zurückgegebene Pin keinen ausstehenden Verweiszähler hat. Wenn der Aufrufer einen Verweis auf der Stecknadel behalten muss, sollte er die **IUnknown::AddRef-Methode** auf dem Pin aufrufen.

Wenn der Filter die Standardpins [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) und [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) verwendet, müssen Sie diese Methode wahrscheinlich nicht überschreiben. Wenn der Filter jedoch Pins verwendet, die diese Klassen erweitern, müssen Sie diese Methode überschreiben, um Pins dieses Typs zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




