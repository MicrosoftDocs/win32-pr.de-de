---
description: Die isequalobject-Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Isequalobject-Funktion (wxutil. h)
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
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370018"
---
# <a name="isequalobject-function"></a>Isequalobject-Funktion

Die- `IsEqualObject` Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfirst* 
</dt> <dd>

Zeiger auf eine-Schnittstelle.

</dd> <dt>

*psecond* 
</dt> <dd>

Zeiger auf die andere-Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn sich die Schnittstellen im selben Objekt befinden, andernfalls " **false** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Diverse Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




