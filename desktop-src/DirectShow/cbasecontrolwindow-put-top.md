---
description: Die put \_ Top-Methode legt die Oberfensterkoordinate fest.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: CBaseControlWindow.put_Top -Methode (Ctlutil.h)
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
ms.openlocfilehash: d3332bcf90ac5e2ee776fe7110c958e50b838bcbdbc6bb4abb23850ced12cc28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635830"
---
# <a name="cbasecontrolwindowput_top-method"></a>CBaseControlWindow.put \_ Top-Methode

Die `put_Top` -Methode legt die Oberfensterkoordinate fest.

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

 

 




