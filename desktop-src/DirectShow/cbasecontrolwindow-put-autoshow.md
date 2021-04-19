---
description: Die Put \_ AutoShow-Methode legt das Autoshow State-Flag fest.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow-Methode (ctlutil. h)
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
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359332"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>Cbasecontrolwindow. Put \_ AutoShow-Methode

Die- `put_AutoShow` Methode legt das Autoshow State-Flag fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Automatisch anzeigen* 
</dt> <dd>

Boolesches Automatisierungs Flag (0 ist off, 1 ist on).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft vereinfacht den Fenster Anzeige Zugriff für-Anwendungen. Wenn dieser Wert auf 1 (on) festgelegt ist, wird das Fenster, das in der Regel ausgeblendet wird, nachdem der Filter verbunden ist, automatisch angezeigt, wenn der Filter anhält oder ausgeführt wird. Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter angehalten wird. Wenn dieser Wert auf 0 (Off) festgelegt ist, wird das Fenster nur dann sichtbar, wenn die Anwendung [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




