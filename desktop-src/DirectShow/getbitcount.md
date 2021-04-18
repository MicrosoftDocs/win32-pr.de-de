---
description: Die getbitcount-Funktion gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Video Untertyp verwendet werden. Diese Funktion ist nur für nicht komprimierte RGB-Untertypen gültig.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Getbitcount-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368428"
---
# <a name="getbitcount-function"></a>Getbitcount-Funktion

Die- `GetBitCount` Funktion gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Video Untertyp verwendet werden. Diese Funktion ist nur für nicht komprimierte RGB-Untertypen gültig.

## <a name="syntax"></a>Syntax


```C++
WORD GetBitCount(
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

Gibt die Anzahl der Bits pro Pixel für diesen Untertyp oder den Wert von "-Wert für die **\_ maximal** zulässige Größe zurück, wenn der Untertyp nicht erkannt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




