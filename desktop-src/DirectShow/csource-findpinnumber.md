---
description: Die findpinnumber-Methode ruft die Nummer einer angegebenen PIN für den Filter ab.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: CSource. findpinnumber-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369380"
---
# <a name="csourcefindpinnumber-method"></a>CSource. findpinnumber-Methode

Die- `FindPinNumber` Methode ruft die Nummer einer angegebenen PIN für den Filter ab.

## <a name="syntax"></a>Syntax


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die PIN-Nummer oder 1 zurück, wenn die PIN in diesem Filter nicht gefunden wurde. Die erste PIN ist mit 0 nummeriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




