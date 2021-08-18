---
description: Die \_ put WindowState-Methode legt den Fensterzustand fest.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: CBaseControlWindow.put_WindowState-Methode (Ctlutil.h)
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
ms.openlocfilehash: 4769aff01c251017734fd7152fa703cd51064db11fb91851fd0b8fed76fc3d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635700"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>CBaseControlWindow.put \_ WindowState-Methode

Die `put_WindowState` -Methode legt den Fensterzustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Windowstate* 
</dt> <dd>

Neuer Fensterzustand.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion verwendet die gleichen Parameter wie die Microsoft Win32 **ShowWindow-Funktion** (z. B. WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE und WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




