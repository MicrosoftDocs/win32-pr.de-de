---
description: Die getbitmapsubtype-Funktion gibt die untergeordnete GUID des Mediums für die angegebene Bitmap zurück.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Getbitmapsubtype-Funktion (wxutil. h)
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
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364718"
---
# <a name="getbitmapsubtype-function"></a>Getbitmapsubtype-Funktion

Die- `GetBitmapSubtype` Funktion gibt die **GUID** für den Medien Untertyp für die angegebene Bitmap zurück.

## <a name="syntax"></a>Syntax


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pheader* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die **GUID** des Medien Untertyps zurück.

## <a name="remarks"></a>Bemerkungen

Bei nicht komprimierten RGB-Typen ordnet diese Funktion dem Untertyp das **biBitCount** -Feld zu. Für komprimierte Video Typen verwendet diese Funktion die [**fourccmap**](fourccmap.md) -Klasse, um das **bicompression** -Feld dem Untertyp zuzuordnen.

Wenn die Funktion dem Format nicht mit einem Untertyp entsprechen kann, ist der Rückgabewert GUID \_ NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




