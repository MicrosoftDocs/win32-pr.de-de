---
description: Mit der Put \_ Top-Methode wird die obere Fenster Koordinate festgelegt.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: CBaseControlWindow.put_Top-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdbce19c3caf4129b1f224a740b27209b855a1f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367136"
---
# <a name="cbasecontrolwindowput_top-method"></a>Cbasecontrolwindow. Put \_ Top-Methode

Die- `put_Top` Methode legt die obere Fenster Koordinate fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Top* 
</dt> <dd>

Neue obere Koordinate in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Fenster hat eine Position auf dem Desktop. Dies wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt. Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention. Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.

Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters. Ebenso wirkt sich die Festlegung von Breite und Höhe nicht auf die linke und die obere Koordinate aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




