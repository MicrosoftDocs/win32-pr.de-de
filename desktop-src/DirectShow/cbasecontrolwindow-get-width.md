---
description: Die get \_ Width-Methode ruft die aktuelle Fensterbreite ab.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: CBaseControlWindow.get_Width-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361463"
---
# <a name="cbasecontrolwindowget_width-method"></a>Cbasecontrolwindow. get \_ Width-Methode

Die- `get_Width` Methode ruft die aktuelle Fensterbreite ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die Fensterbreite in Pixel.

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

 

 




