---
description: Die ResetPaletteVersion-Methode setzt die Palettenversion zurück. Rufen Sie diese Methode auf, wenn der Stecknadel des besitzenden Filters erneut eine Verbindung herstellen kann.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: CDrawImage.ResetPaletteVersion-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d367060c86c54fb9df5bd7b0f05cea1fa3d7b7f3316dce327fca7ce9985fadfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055960"
---
# <a name="cdrawimageresetpaletteversion-method"></a>CDrawImage.ResetPaletteVersion-Methode

Die `ResetPaletteVersion` -Methode setzt die Palettenversion zurück. Rufen Sie diese Methode auf, wenn der Stecknadel des besitzenden Filters erneut eine Verbindung herstellen kann.

## <a name="syntax"></a>Syntax


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt den Wert von **m \_ PaletteVersion** auf eine vordefinierte Konstante fest, **PALETTE \_ VERSION**.

## <a name="requirements"></a>Anforderungen



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

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




