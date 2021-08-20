---
description: Die put \_ AutoShow-Methode legt das AutoShow-Statusflag fest.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017278"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>AutoShow-Methode "CBaseControlWindow.put" \_

Die `put_AutoShow` -Methode legt das AutoShow-Statusflag fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Autoshow* 
</dt> <dd>

Boolean-Flag für Automation (0 ist deaktiviert, 1 ist aktiviert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft vereinfacht den Fensteranzeigezugriff für Anwendungen. Wenn diese Einstellung auf 1 (ein) festgelegt ist, wird das Fenster, das in der Regel ausgeblendet wird, nachdem der Filter verbunden wurde, automatisch angezeigt, wenn der Filter angehalten oder ausgeführt wird. Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter beendet wird. Wenn diese Einstellung auf 0 (deaktiviert) festgelegt ist, wird das Fenster nur sichtbar gemacht, wenn die Anwendung [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




