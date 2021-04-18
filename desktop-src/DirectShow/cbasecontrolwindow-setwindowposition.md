---
description: Die SetWindowPosition-Methode legt die Fensterposition auf dem Desktop fest.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Cbasecontrolwindow. SetWindowPosition-Methode (ctlutil. h)
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
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368619"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Cbasecontrolwindow. SetWindowPosition-Methode

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

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




