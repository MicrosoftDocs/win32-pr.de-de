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
ms.openlocfilehash: 2b8833780411ae126dcda20c579fc5f6a681362da3707ee68879b06800b7b032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654768"
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



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




