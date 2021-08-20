---
description: Konstruktormethode. Der Konstruktor sperrt das angegebene kritische Abschnittsobjekt.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: CAutoLock.CAutoLock-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: 11267b444df319e339bcf13b30f200868a0f62d67712ed147513c2f8bc7d000c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017568"
---
# <a name="cautolockcautolock-constructor"></a>CAutoLock.CAutoLock-Konstruktor

Konstruktormethode. Der Konstruktor sperrt das angegebene kritische Abschnittsobjekt.

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

Zeiger auf ein [**CCritSec-Objekt,**](ccritsec.md) das ein kritisches Abschnittsobjekt enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAutoLock-Klasse**](cautolock.md)
</dt> </dl>

 

 




