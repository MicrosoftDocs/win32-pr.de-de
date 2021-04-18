---
description: Mit der Put \_ windowstyleex-Methode werden die erweiterten Fenster Stile festgelegt.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: CBaseControlWindow.put_WindowStyleEx-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364482"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>Cbasecontrolwindow. Put \_ windowstyleex-Methode

Die- `put_WindowStyleEx` Methode legt die erweiterten Fenster Stile fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Windowstyleex* \[ in\]
</dt> <dd>

Ein-Wert, der den Stil des Steuerelement Fensters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt noError zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode verwendet erweiterte Fenster Stile. Eine umfassende Liste der erweiterten Fenster Stile finden Sie in der **Microsoft Win32-** Funktion "Microsoft-Win32-Funktion". Um den Fenster Stil zu ändern, rufen Sie den aktuellen Fenster Stil ab, und fügen Sie dann die erforderlichen Bitfelder hinzu, oder entfernen Sie Sie.

Verwenden Sie die folgenden Fenster Stile nicht, da Sie nicht überprüft werden.

-   WS \_ deaktiviert
-   WS \_ HScroll
-   WS \_ -Symbol
-   WS- \_ Maximierung
-   WS- \_ Minimierung
-   WS- \_ VScroll

Mit einigen Ausnahmen (Beachten Sie hier) sind die zulässigen Flags identisch mit denen, die von der Win32-Funktion "up **Window** " zugelassen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




