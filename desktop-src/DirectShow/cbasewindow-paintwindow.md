---
description: Die paintwindow-Methode bewirkt, dass das Fenster neu gezeichnet wird.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Cbasewindow. paintwindow-Methode (winutil. h)
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
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358754"
---
# <a name="cbasewindowpaintwindow-method"></a>Cbasewindow. paintwindow-Methode

Die- `PaintWindow` Methode bewirkt, dass das Fenster neu gezeichnet wird.

## <a name="syntax"></a>Syntax


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*berase* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Hintergrund gelöscht wird. Wenn der Wert **true** ist, wird der Hintergrund gelöscht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert eine WM \_ -Zeichnungs Nachricht, indem der gesamte Client Bereich des Fensters ungültig wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




