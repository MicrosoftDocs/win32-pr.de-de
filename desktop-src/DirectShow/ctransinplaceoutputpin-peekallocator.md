---
description: Die Methode "Peer-ID" gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Ctransinplaceoutputpin. Peer-zuordcator-Methode (transip. h)
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
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370612"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>Ctransinplaceoutputpin. Peer-zuordcator-Methode

Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**cbaseoutputpin:: m \_ pallocator**](cbaseoutputpin-m-pallocator.md) -Member-Variable zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceoutputpin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




