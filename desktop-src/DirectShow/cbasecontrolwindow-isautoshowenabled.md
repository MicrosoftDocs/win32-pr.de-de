---
description: Die isautoshowenabled-Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der renderingfilter anhält oder ausgeführt wird.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Cbasecontrolwindow. isautoshowenabled-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368581"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Cbasecontrolwindow. isautoshowenabled-Methode

Die- `IsAutoShowEnabled` Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der renderingfilter anhält oder ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das **m \_ bauchanshow** -Element auf 1 oder **false** festgelegt ist, wenn es auf 0 festgelegt ist.

## <a name="remarks"></a>Bemerkungen

Wenn das **m \_ baudeshow** -Element in einem ausgeblendeten Videofenster auf 1 festgelegt ist, wird das Fenster sichtbar, wenn der Filter anhält oder ausgeführt wird. Wenn dieser Member auf 0 festgelegt ist, wird das Fenster nur angezeigt, wenn Sie die Member-Funktion [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern verwenden.

Diese Member-Funktion Ruft die **m \_ baudeshow** -Element Einstellung ab und hat dasselbe Ergebnis wie die Verwendung der [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




