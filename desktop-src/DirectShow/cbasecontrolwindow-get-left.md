---
description: Die get \_ Left-Methode ruft die aktuelle linke Fenster Koordinate ab.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: CBaseControlWindow.get_Left-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362052"
---
# <a name="cbasecontrolwindowget_left-method"></a>Cbasecontrolwindow. get \_ Left-Methode

Die- `get_Left` Methode ruft die aktuelle linke Fenster Koordinate ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pleft* 
</dt> <dd>

Zeiger auf die linke Koordinate in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Fenster hat eine Position auf dem Desktop. Diese Position wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt. Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention. Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.

Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links und nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters. Ebenso hat das Festlegen von Breite und Höhe keine Auswirkung auf die linke und die obere Koordinate.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




