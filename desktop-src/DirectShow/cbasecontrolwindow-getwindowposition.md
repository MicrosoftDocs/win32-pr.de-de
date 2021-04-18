---
description: Die getwindowposition-Methode ruft die aktuellen Koordinaten für das Fenster ab.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Cbasecontrolwindow. getwindowposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357678"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Cbasecontrolwindow. getwindowposition-Methode

Die- `GetWindowPosition` Methode ruft die aktuellen Koordinaten für das Fenster ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pleft* 
</dt> <dd>

Zeiger auf die linke Koordinate in Bildschirm Koordinaten.

</dd> <dt>

*ptop* 
</dt> <dd>

Zeiger auf die obere Koordinate in Bildschirm Koordinaten.

</dd> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die Fensterbreite in Bildschirm Koordinaten.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die Fensterhöhe in Bildschirm Koordinaten.

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

 

 




