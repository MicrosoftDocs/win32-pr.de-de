---
description: Die RemovePalette-Methode löscht die vorhandene logische Palette und ruft CBaseWindow::UnsetPalette für das CBaseWindow-Objekt auf.
ms.assetid: fab531b8-8630-43f8-bf08-cd8f24659bef
title: CImagePalette.RemovePalette-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.RemovePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b87c8f028da17e6af305900f203c5cf1143132806ca1b2ce9b0edaddebd0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916009"
---
# <a name="cimagepaletteremovepalette-method"></a>CImagePalette.RemovePalette-Methode

Die `RemovePalette` -Methode löscht die vorhandene logische Palette und ruft [**CBaseWindow::UnsetPalette**](cbasewindow-unsetpalette.md) für das **CBaseWindow-Objekt** auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemovePalette();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




