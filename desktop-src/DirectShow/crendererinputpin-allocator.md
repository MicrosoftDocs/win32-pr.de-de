---
description: Die zuordnermethode Ruft einen Zeiger auf die Speicherzuweisung ab.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Crendererinputpin. zuordcator-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372092"
---
# <a name="crendererinputpinallocator-method"></a>Crendererinputpin. zuordcator-Methode

Die- `Allocator` Methode ruft einen Zeiger auf die Speicherzuweisung ab.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners oder **null** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die [**cbaseingeputpin:: m \_ pallocator**](cbaseinputpin-m-pallocator.md) -Member-Variable zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle. Bei dieser Methode handelt es sich um eine-Accessor-Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




