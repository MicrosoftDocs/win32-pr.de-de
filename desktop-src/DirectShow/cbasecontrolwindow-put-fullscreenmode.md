---
description: Die Put \_ Fullscreenmode-Methode legt den Vollbildmodus des Renderers fest.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: CBaseControlWindow.put_FullScreenMode-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364722"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>Cbasecontrolwindow. Put \_ Fullscreenmode-Methode

Die- `put_FullScreenMode` Methode legt den Vollbildmodus des Renderers fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fullscreenmode* 
</dt> <dd>

Der anzuwendende Vollbildmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die aktuelle Implementierung gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

Ein Videorenderer, der einen Vollbildmodus implementiert, sollte diese Element Funktion überschreiben und alle unterstützten Modi implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




