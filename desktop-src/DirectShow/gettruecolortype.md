---
description: Die GetTrueColorType-Funktion ruft den lesbaren Namen eines Videountertyps ab.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: GetTrueColorType-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fb25d4539d4b929362241ffacbfafd97b08844508ec2c1f38c619fe40901475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564710"
---
# <a name="gettruecolortype-function"></a>GetTrueColorType-Funktion

Die **GetTrueColorType-Funktion** ruft den lesbaren Namen eines Videountertyps ab.

## <a name="syntax"></a>Syntax


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pHeader* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) die die Bitmap definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt MEDIASUBTYPE \_ RGB555 oder MEDIASUBTYPE \_ RGB565 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




