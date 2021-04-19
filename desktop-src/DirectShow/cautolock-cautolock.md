---
description: Konstruktormethode. Der Konstruktor sperrt das angegebene kritische Abschnitts Objekt.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Cautolock. cautolock-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366687"
---
# <a name="cautolockcautolock-constructor"></a>Cautolock. cautolock-Konstruktor

Konstruktormethode. Der Konstruktor sperrt das angegebene kritische Abschnitts Objekt.

## <a name="syntax"></a>Syntax


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plock* 
</dt> <dd>

Zeiger auf ein [**ccritsec**](ccritsec.md) -Objekt, das ein kritisches Abschnitts Objekt enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cautolock-Klasse**](cautolock.md)
</dt> </dl>

 

 




