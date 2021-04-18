---
description: Die incrementpaletteversion-Methode erhöht die palettenversion. Ruft diese Methode auf, wenn der Medientyp in ein neues Format geändert wird.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Cdrawimage. incrementpaletteversion-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372234"
---
# <a name="cdrawimageincrementpaletteversion-method"></a>Cdrawimage. incrementpaletteversion-Methode

Die- `IncrementPaletteVersion` Methode erhöht die palettenversion. Ruft diese Methode auf, wenn der Medientyp in ein neues Format geändert wird.

## <a name="syntax"></a>Syntax


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht den Wert der **m \_ paletteversion** -Member-Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage:: getpaletteversion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**Cdrawimage:: resetpaletteversion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




