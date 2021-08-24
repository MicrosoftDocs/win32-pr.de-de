---
description: Die GetPaletteVersion-Methode ruft die aktuelle Palettenversion ab.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: CDrawImage.GetPaletteVersion-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14cc4df95507a0c28bd61ec6db405f01353f9228419d0da84c4fc9fc35ca6b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537290"
---
# <a name="cdrawimagegetpaletteversion-method"></a>CDrawImage.GetPaletteVersion-Methode

Die `GetPaletteVersion` -Methode ruft die aktuelle Palettenversion ab.

## <a name="syntax"></a>Syntax


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert der **m \_ PaletteVersion-Membervariablen** zurück.

## <a name="remarks"></a>Hinweise

Der von dieser Methode zurückgegebene Wert gilt nur, wenn die Zuweisung ein [**CImageAllocator-Objekt**](cimageallocator.md) ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




