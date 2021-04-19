---
description: Die getsubtypame-Funktion Ruft den lesbaren Namen eines Video Untertyps ab.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Getsubtypame-Funktion (wxutil. h)
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
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358678"
---
# <a name="getsubtypename-function"></a>Getsubtypame-Funktion

Die `GetSubtypeName` -Funktion Ruft den lesbaren Namen eines Video Untertyps ab.

## <a name="syntax"></a>Syntax


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psubtype* 
</dt> <dd>

Zeiger auf einen Video Untertyp- **GUID**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichenfolge zurück, die den Namen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




