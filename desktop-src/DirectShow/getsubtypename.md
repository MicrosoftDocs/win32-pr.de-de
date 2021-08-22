---
description: Die GetSubtypeName-Funktion ruft den für Menschen lesbaren Namen eines Videountertyps ab.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: GetSubtypeName-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c676f3e08f55bd010e761853b777e0eb4b28933536ab7af09bd94e457032b583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564849"
---
# <a name="getsubtypename-function"></a>GetSubtypeName-Funktion

Die `GetSubtypeName` Funktion ruft den für Menschen lesbaren Namen eines Videountertyps ab.

## <a name="syntax"></a>Syntax


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSubtype* 
</dt> <dd>

Zeiger auf eine **Videountertyp-GUID.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichenfolge zurück, die den Namen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




