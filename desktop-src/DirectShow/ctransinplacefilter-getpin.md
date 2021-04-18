---
description: Die getpin-Methode ruft eine PIN ab.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Ctransinplacefilter. getpin-Methode (transip. h)
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
ms.openlocfilehash: ae93b663af5427bc61367ae03a3abd6790b8634a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354708"
---
# <a name="ctransinplacefiltergetpin-method"></a>Ctransinplacefilter. getpin-Methode

Die- `GetPin` Methode ruft eine PIN ab.

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

Nummer der angegebenen PIN, indiziert von 0 (null). Bei diesem Filter ist Pin 0 die Eingabe-PIN, und Pin 1 ist die Ausgabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert, oder **null** , wenn die Methode fehlschlägt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode. Wenn die-Methode zum ersten Mal aufgerufen wird, werden beide Pins erstellt.

Diese Methode erhöht nicht den Verweis Zähler für die zurückgegebene PIN, sodass die zurückgegebene Pin keinen ausstehenden Verweis Zähler enthält. Wenn der Aufrufer einen Verweis auf die PIN aufbewahren muss, sollte die **IUnknown:: adressf** -Methode für die PIN aufgerufen werden.

Wenn der Filter die standardmäßigen [**ctransinplaceinputpin**](ctransinplaceinputpin.md) -und [**ctransinplaceoutputpin**](ctransinplaceoutputpin.md) -Pins verwendet, muss diese Methode wahrscheinlich nicht außer Kraft gesetzt werden. Wenn der Filter Pins verwendet, mit denen diese Klassen erweitert werden, müssen Sie diese Methode jedoch außer Kraft setzen, um Pins dieses Typs zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




