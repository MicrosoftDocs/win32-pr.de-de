---
description: Die getpin-Methode ruft eine PIN ab. Die cenumpins-Klasse ruft diese Methode auf, um Pins für den Filter aufzuzählen.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Cbasefilter. getpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354217"
---
# <a name="cbasefiltergetpin-method"></a>Cbasefilter. getpin-Methode

Die **getpin** -Methode ruft eine PIN ab. Die [**cenumpins**](cenumpins.md) -Klasse ruft diese Methode auf, um Pins für den Filter aufzuzählen.

## <a name="syntax"></a>Syntax


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Der null basierte Index der PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert.

## <a name="remarks"></a>Bemerkungen

Sie müssen diese rein virtuelle Methode in der abgeleiteten Klasse implementieren. Gibt einen Zeiger auf die *n*-te Pin dieses Filters zurück, indiziert von 0 (null). Sie können eine beliebige Indizierungs Reihenfolge auswählen, solange die Reihenfolge korrigiert ist. Wenn der Filter Pins hinzufügt oder löscht oder die Bestellung aus einem anderen Grund zur Laufzeit geändert wird, wird die [**cbasefilter:: incrementpinversion**](cbasefilter-incrementpinversion.md) -Methode aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




