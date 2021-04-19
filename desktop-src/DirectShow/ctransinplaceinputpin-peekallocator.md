---
description: Die Methode "Peer-ID" gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Ctransinplaceinputpin. Peer-zuordcator-Methode (transip. h)
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
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366945"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a>Ctransinplaceinputpin. Peer-zuordcator-Methode

Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**cbaseingeputpin:: m \_ pallocator**](cbaseinputpin-m-pallocator.md) -Member-Variable zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceinputpin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




