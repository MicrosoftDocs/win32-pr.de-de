---
description: Die SetWindowPosition-Methode legt die Fensterposition auf dem Desktop fest.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: CBaseControlWindow.SetWindowPosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2734c93d1a3d3d3ea29e037d1bf85baacd5358a69f08d1517012c3eb250ab8ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635459"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>CBaseControlWindow.SetWindowPosition-Methode

Die `SetWindowPosition` -Methode legt die Fensterposition auf dem Desktop fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Left* 
</dt> <dd>

Neue linke Koordinate.

</dd> <dt>

*Top* 
</dt> <dd>

Neue obere Koordinate.

</dd> <dt>

*Width* 
</dt> <dd>

Breite des Fensters.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Fensters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




