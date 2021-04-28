---
description: 'CTransInPlaceOutputPin.PeekAllocator-Methode: Die PeekAllocator-Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.'
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: CTransInPlaceOutputPin.PeekAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084598"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>CTransInPlaceOutputPin.PeekAllocator-Methode

Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBaseOutputPin::m \_ pAllocator-Membervariable**](cbaseoutputpin-m-pallocator.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




