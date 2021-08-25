---
description: Die PaintWindow-Methode bewirkt, dass das Fenster neu gepaint wird.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: CBaseWindow.PaintWindow-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cc998f270947890327fb3cbacce4a29183604047824b05b8a66538c163bdc08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635120"
---
# <a name="cbasewindowpaintwindow-method"></a>CBaseWindow.PaintWindow-Methode

Die `PaintWindow` -Methode bewirkt, dass das Fenster neu gepaint wird.

## <a name="syntax"></a>Syntax


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bErase* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Hintergrund gelöscht wird. Wenn der Wert **TRUE ist,** wird der Hintergrund gelöscht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode generiert eine WM \_ PAINT-Nachricht, indem der gesamte Clientbereich des Fensters ungültig wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




