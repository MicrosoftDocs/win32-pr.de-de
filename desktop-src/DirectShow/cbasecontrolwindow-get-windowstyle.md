---
description: Die get \_ Windows Style-Methode ruft die Standardfenster Stile ab.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: CBaseControlWindow.get_WindowStyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372707"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>Cbasecontrolwindow. get \_ WindowStyle-Methode

Die- `get_WindowStyle` Methode ruft die Standardfenster Stile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwindowstyle* 
</dt> <dd>

Zeiger auf Fenster Stile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion gibt die Standardfenster Stile zurück, wie z \_ . b. WS Child und WS \_ Visible. Die [**cbasecontrolwindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) -Member-Funktion wird aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




