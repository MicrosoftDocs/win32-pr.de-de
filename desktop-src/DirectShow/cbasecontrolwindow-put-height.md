---
description: Die Put \_ Height-Methode legt die Fensterhöhe fest.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: CBaseControlWindow.put_Height -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34774d366858e9c9bbe9ce5b02e897453bca21b9bd07d9eb11c60ac8313d33e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660037"
---
# <a name="cbasecontrolwindowput_height-method"></a>CBaseControlWindow.put \_ Height-Methode

Die `put_Height` -Methode legt die Fensterhöhe fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Height* 
</dt> <dd>

Neue Fensterhöhe in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Das Fenster hat eine Position auf dem Desktop. Dies wird in Pixel durch vier Koordinaten ausgedrückt (links, oben, rechts und unten). Schnittstellen, die von OLE automatisiert werden, drücken diese Position in der Regel über links, oben, Breite und Höhe aus. dies ist die Konvention, die in DirectShow verwendet wird. Alle Koordinaten werden in Pixel ausgedrückt, und durch das Ändern einer beliebigen Koordinate wird das Fenster sofort aktualisiert.

Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben bewegt. Diese Koordinaten haben keine Auswirkungen auf die Breite und Höhe des Fensters. Ebenso wirkt sich das Festlegen der Breite und Höhe nicht auf die linke und die obere Koordinate aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




