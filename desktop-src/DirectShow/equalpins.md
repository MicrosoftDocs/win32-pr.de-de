---
description: Die equalpins-Funktion überprüft, ob sich zwei Pins auf demselben Objekt befinden.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Equalpins-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357950"
---
# <a name="equalpins-function"></a>Equalpins-Funktion

Die equalpins-Funktion überprüft, ob sich zwei Pins auf demselben Objekt befinden.

## <a name="syntax"></a>Syntax


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin1* 
</dt> <dd>

Zeiger auf eine PIN.

</dd> <dt>

*pPin2* 
</dt> <dd>

Zeiger auf die andere PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn sich beide Pins auf demselben Objekt befinden, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Diverse Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




