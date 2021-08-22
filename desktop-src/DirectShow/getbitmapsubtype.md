---
description: Die GetBitmapSubtype-Funktion gibt die Medienuntertyp-GUID für die angegebene Bitmap zurück.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: GetBitmapSubtype-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8903e4a404367327b677a239b8ab28e3cb47e5679203857154f453a5cc01e25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536680"
---
# <a name="getbitmapsubtype-function"></a>GetBitmapSubtype-Funktion

Die `GetBitmapSubtype` Funktion gibt die **Medienuntertyp-GUID** für die angegebene Bitmap zurück.

## <a name="syntax"></a>Syntax


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pHeader* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die **Medienuntertyp-GUID zurück.**

## <a name="remarks"></a>Hinweise

Bei nicht komprimierten RGB-Typen ordnet diese Funktion das **Feld biBitCount** dem Untertyp zu. Für komprimierte Videotypen verwendet diese Funktion die [**FOURCCMap-Klasse,**](fourccmap.md) um das **Feld biCompression** dem Untertyp zuzuordnen.

Wenn die Funktion das Format nicht mit einem Untertyp abgleichen kann, ist der Rückgabewert GUID \_ NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




