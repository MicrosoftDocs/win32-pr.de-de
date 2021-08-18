---
description: Die UsingDifferentAllocators-Methode bestimmt, ob die Eingabe- und Ausgabepins unterschiedliche Zuweisungen verwenden.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: CTransInPlaceFilter.UsingDifferentAllocators-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0033c0f5ded1fe741d27397078367049d72061c40a993833f714686d9f8a96fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953419"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>CTransInPlaceFilter.UsingDifferentAllocators-Methode

Die `UsingDifferentAllocators` -Methode bestimmt, ob die Eingabe- und Ausgabepins unterschiedliche Zuweisungen verwenden.

## <a name="syntax"></a>Syntax


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Eingabe- und Ausgabepins unterschiedliche Zuweisungen verwenden, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




