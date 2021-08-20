---
description: Die get \_ Top-Methode ruft die Koordinate des oberen Fensters ab.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: CBaseControlWindow.get_Top -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7ba60f3365ba2f1a8ea00579e8c2eb51c9d6aa32843e7603d0d26c2747c97c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017388"
---
# <a name="cbasecontrolwindowget_top-method"></a>CBaseControlWindow.get \_ Top-Methode

Die `get_Top` -Methode ruft die Koordinate des oberen Fensters ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTop* 
</dt> <dd>

Zeiger auf die obere Koordinate in Pixel.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




