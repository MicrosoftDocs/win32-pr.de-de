---
description: 'CTransInPlaceInputPin.PeekAllocator-Methode: Die PeekAllocator-Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.'
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: CTransInPlaceInputPin.PeekAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084668"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a>CTransInPlaceInputPin.PeekAllocator-Methode

Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBaseInputPin::m \_ pAllocator-Membervariable**](cbaseinputpin-m-pallocator.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceInputPin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




