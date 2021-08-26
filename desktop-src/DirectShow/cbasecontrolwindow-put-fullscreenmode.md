---
description: Die put \_ FullScreenMode-Methode legt den Vollbildmodus des Renderers fest.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: CBaseControlWindow.put_FullScreenMode -Methode (Ctlutil.h)
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
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983680"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow.put \_ FullScreenMode-Methode

Die `put_FullScreenMode` -Methode legt den Vollbildmodus des Renderers fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Vollbildmodus, der angewendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die aktuelle Implementierung gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Ein Videorenderer, der einen Vollbildmodus implementiert, sollte diese Memberfunktion überschreiben und die unterstützten Modi implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




