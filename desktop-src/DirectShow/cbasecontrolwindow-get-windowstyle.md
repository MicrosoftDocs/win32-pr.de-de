---
description: Die \_ Methode "WindowStyle abrufen" ruft die Standardfensterstile ab.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: CBaseControlWindow.get_WindowStyle-Methode (Ctlutil.h)
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
ms.openlocfilehash: e9356b449adbb4ee760ec70990c4db0b6703c16e9d0970f2756bac23907b1bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660259"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>CBaseControlWindow.get \_ WindowStyle-Methode

Die `get_WindowStyle` -Methode ruft die Standardfensterstile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWindowStyle* 
</dt> <dd>

Zeiger auf Fensterstile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion gibt die Standardfensterstile zurück, z. B. WS \_ CHILD und WS \_ VISIBLE. Sie ruft die [**Memberfunktion CBaseControlWindow::D oGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




