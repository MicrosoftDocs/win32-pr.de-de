---
description: Die resetpaletteversion-Methode setzt die palettenversion zurück. Ruft diese Methode auf, wenn die PIN des besitzenden Filters erneut eine Verbindung herstellt.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Cdrawimage. resetpaletteversion-Methode (winutil. h)
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
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358028"
---
# <a name="cdrawimageresetpaletteversion-method"></a>Cdrawimage. resetpaletteversion-Methode

Die- `ResetPaletteVersion` Methode setzt die palettenversion zurück. Ruft diese Methode auf, wenn die PIN des besitzenden Filters erneut eine Verbindung herstellt.

## <a name="syntax"></a>Syntax


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt den Wert von **m \_ paletteversion** auf eine vordefinierte Konstante **, \_ palettenversion**, fest.

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

[**Cdrawimage:: incrementpaletteversion**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




