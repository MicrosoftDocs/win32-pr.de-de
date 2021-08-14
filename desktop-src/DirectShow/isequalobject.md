---
description: Die IsEqualObject-Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: IsEqualObject-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817451"
---
# <a name="isequalobject-function"></a>IsEqualObject-Funktion

Die `IsEqualObject` Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFirst* 
</dt> <dd>

Zeiger auf eine Schnittstelle.

</dd> <dt>

*pSecond* 
</dt> <dd>

Zeiger auf die andere Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn sich beide Schnittstellen im selben Objekt befinden, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verschiedene Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




