---
description: Die GetWindowPosition-Methode ruft die aktuellen Koordinaten für das Fenster ab.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: CBaseControlWindow.GetWindowPosition-Methode (Ctlutil.h)
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
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966730"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>CBaseControlWindow.GetWindowPosition-Methode

Die `GetWindowPosition` -Methode ruft die aktuellen Koordinaten für das Fenster ab.

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

*pLeft* 
</dt> <dd>

Zeiger auf die linke Koordinate in Bildschirmkoordinaten.

</dd> <dt>

*pTop* 
</dt> <dd>

Zeiger auf die obere Koordinate in Bildschirmkoordinaten.

</dd> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die Fensterbreite in Bildschirmkoordinaten.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die Fensterhöhe in Bildschirmkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




