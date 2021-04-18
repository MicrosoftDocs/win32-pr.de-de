---
description: Die getpaletteversion-Methode ruft die aktuelle palettenversion ab.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Cdrawimage. getpaletteversion-Methode (winutil. h)
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
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371527"
---
# <a name="cdrawimagegetpaletteversion-method"></a>Cdrawimage. getpaletteversion-Methode

Die- `GetPaletteVersion` Methode ruft die aktuelle palettenversion ab.

## <a name="syntax"></a>Syntax


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert der **m \_ paletteversion** -Member-Variable zurück.

## <a name="remarks"></a>Bemerkungen

Der von dieser Methode zurückgegebene Wert gilt nur, wenn die Zuweisung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage:: incrementpaletteversion**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**Cdrawimage:: resetpaletteversion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




