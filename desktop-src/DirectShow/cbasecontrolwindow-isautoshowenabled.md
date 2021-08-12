---
description: Die IsAutoShowEnabled-Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der Renderingfilter angehalten oder ausgeführt wird.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: CBaseControlWindow.IsAutoShowEnabled-Methode (Ctlutil.h)
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
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660229"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>CBaseControlWindow.IsAutoShowEnabled-Methode

Die `IsAutoShowEnabled` -Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der Renderingfilter angehalten oder ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das **m \_ bAutoShow-Element** auf 1 festgelegt ist, oder **FALSE,** wenn es auf 0 festgelegt ist.

## <a name="remarks"></a>Hinweise

Wenn das **m \_ bAutoShow-Element** in einem ausgeblendeten Videofenster auf 1 festgelegt ist, wird das Fenster sichtbar, wenn der Filter angehalten oder ausgeführt wird. Wenn dieser Member auf 0 festgelegt ist, wird das Fenster nur angezeigt, wenn Sie die [**Memberfunktion CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern verwenden.

Diese Memberfunktion ruft die **m \_ bAutoShow-Membereinstellung** ab und hat das gleiche Ergebnis wie die Verwendung der [**IVideoWindow::get \_ AutoShow-Methode.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




