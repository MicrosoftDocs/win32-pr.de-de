---
description: Mit der Put \_ WindowState-Methode wird der Fenster Zustand festgelegt.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: CBaseControlWindow.put_WindowState-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358141"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>Cbasecontrolwindow. Put \_ WindowState-Methode

Die- `put_WindowState` Methode legt den Fenster Zustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*WindowState* 
</dt> <dd>

Neuer Fenster Zustand.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion nimmt dieselben Parameter wie die Microsoft Win32 **ShowWindow** -Funktion (z. b. WS \_ shownormal, WS \_ showminnoaktivierungs und WS \_ showmaximized).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




