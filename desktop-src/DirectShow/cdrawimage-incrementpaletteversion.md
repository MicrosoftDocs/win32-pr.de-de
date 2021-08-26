---
description: Die IncrementPaletteVersion-Methode erhöht die Palettenversion. Rufen Sie diese Methode auf, wenn sich der Medientyp in ein neues palettiertes Format ändert.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: CDrawImage.IncrementPaletteVersion-Methode (Winutil.h)
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
ms.openlocfilehash: 7884c4d552920a9e5650d2a092b7fffc43a1c67bf03916eab7bb72da3a87946a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076400"
---
# <a name="cdrawimageincrementpaletteversion-method"></a>CDrawImage.IncrementPaletteVersion-Methode

Die `IncrementPaletteVersion` -Methode erhöht die Palettenversion. Rufen Sie diese Methode auf, wenn sich der Medientyp in ein neues palettiertes Format ändert.

## <a name="syntax"></a>Syntax


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erhöht den Wert der **m PaletteVersion-Membervariablen. \_**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::GetPaletteVersion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




