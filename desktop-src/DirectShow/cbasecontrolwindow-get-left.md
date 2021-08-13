---
description: Die methode get \_ Left ruft die aktuelle linke Fensterkoordinate ab.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: CBaseControlWindow.get_Left -Methode (Ctlutil.h)
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
ms.openlocfilehash: 9317c1c061fe8528903bdd2e7129d0cfdc9e6dd67b9722841360d131e15cfb10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660523"
---
# <a name="cbasecontrolwindowget_left-method"></a>CBaseControlWindow.get \_ Left-Methode

Die `get_Left` -Methode ruft die aktuelle linke Fensterkoordinate ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pLeft* 
</dt> <dd>

Zeiger auf die linke Koordinate in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Das Fenster hat eine Position auf dem Desktop. Diese Position wird in Pixel durch vier Koordinaten ausgedrückt (links, oben, rechts und unten). Schnittstellen, die von OLE automatisiert werden, drücken diese Position in der Regel über links, oben, Breite und Höhe aus. dies ist die Konvention, die in DirectShow verwendet wird. Alle Koordinaten werden in Pixel ausgedrückt, und durch das Ändern einer beliebigen Koordinate wird das Fenster sofort aktualisiert.

Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben bewegt. Diese Koordinaten haben keine Auswirkungen auf die Breite und Höhe des Fensters. Ebenso hat das Festlegen der Breite und Höhe keine Auswirkungen auf die linke und die obere Koordinate.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




