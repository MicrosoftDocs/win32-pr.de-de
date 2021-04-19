---
description: Die getownerwindow-Methode ruft das besitzende Fenster Handle "m \_ hwndOwner" ab.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Cbasecontrolwindow. getownerwindow-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369702"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Cbasecontrolwindow. getownerwindow-Methode

Die- `GetOwnerWindow` Methode ruft das besitzende Fenster Handle " **m \_ hwndOwner**" ab.

## <a name="syntax"></a>Syntax


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Besitzer Fenster zurück.

## <a name="remarks"></a>Bemerkungen

Ruft das besitzende Fenster ohne Aufrufen der Schnittstellen Methode ab. Verwenden Sie diese Member-Funktion anstelle von " [**cbasecontrolwindow:: get \_ Owner**](cbasecontrolwindow-get-owner.md)", es sei denn, Sie rufen dies extern über die [**IVideoWindow:: get- \_ Besitzer**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




