---
description: Die methode get \_ Width ruft die aktuelle Fensterbreite ab.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: CBaseControlWindow.get_Width -Methode (Ctlutil.h)
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
ms.openlocfilehash: 3dff6e2a0929963f06c14aa8899b2a1d6a268db8f87b5067d2ed65f90964c803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768240"
---
# <a name="cbasecontrolwindowget_width-method"></a>CBaseControlWindow.get \_ Width-Methode

Die `get_Width` -Methode ruft die aktuelle Fensterbreite ab.

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

 

 




