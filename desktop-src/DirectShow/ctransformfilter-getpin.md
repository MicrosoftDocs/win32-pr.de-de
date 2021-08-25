---
description: 'CTransformFilter.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: CTransformFilter.GetPin-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32f9ccdd2b7d787faa6f1081c51bf107b979d26d952552651542afcb34f985ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823920"
---
# <a name="ctransformfiltergetpin-method"></a>CTransformFilter.GetPin-Methode

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

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die rein virtuelle [**CBaseFilter::GetPin-Methode.**](cbasefilter-getpin.md) Wenn die -Methode zum ersten Mal aufgerufen wird, werden beide Pins erstellt.

Diese Methode erhöht den Verweiszähler für den zurückgegebenen Pin nicht, sodass der zurückgegebene Pin keinen ausstehenden Verweiszähler hat. Wenn der Aufrufer einen Verweis auf die Stecknadel behalten muss, sollte er die **IUnknown::AddRef-Methode** auf dem Pin aufrufen.

Wenn der Filter die Standardpins [**CTransformInputPin**](ctransforminputpin.md) und [**CTransformOutputPin**](ctransformoutputpin.md) verwendet, müssen Sie diese Methode wahrscheinlich nicht überschreiben. Wenn der Filter jedoch Pins verwendet, die diese Klassen erweitern, müssen Sie diese Methode überschreiben, um Pins dieses Typs zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




