---
description: Die OnSize-Methode verarbeitet \_ Nachrichten der WM-Größe.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Cbasewindow. OnSize-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365969"
---
# <a name="cbasewindowonsize-method"></a>Cbasewindow. OnSize-Methode

Die- `OnSize` Methode verarbeitet \_ Nachrichten der WM-Größe.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Width* 
</dt> <dd>

Breite des Client Bereichs in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Die Höhe des Client Bereichs in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode speichert die neue Breite und Höhe. Um diese Werte abzurufen, rufen Sie die [**cbasewindow:: getwindowheight**](cbasewindow-getwindowheight.md) -Methode und die [**cbasewindow:: getwindowwidth**](cbasewindow-getwindowwidth.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




