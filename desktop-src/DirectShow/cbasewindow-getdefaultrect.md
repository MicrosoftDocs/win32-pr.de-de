---
description: Die GetDefaultRect-Methode ruft die Standardgröße des Clientbereichs ab.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: CBaseWindow.GetDefaultRect-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074614"
---
# <a name="cbasewindowgetdefaultrect-method"></a>CBaseWindow.GetDefaultRect-Methode

Die `GetDefaultRect` -Methode ruft die Standardgröße des Clientbereichs ab.

## <a name="syntax"></a>Syntax


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Standardrechteck zurück.

## <a name="remarks"></a>Hinweise

Wenn das Fenster aktiviert ist, ruft das -Objekt diese Methode auf, um zu bestimmen, wie groß der Clientbereich des Fensters sein soll. In der Basisklasse gibt diese Methode ein Rechteck zurück, dessen Höhe und Breite die definierten Konstanten DEFHEIGHT und DEFWIDTH sind. Eine abgeleitete Klasse sollte diese Methode überschreiben. Bei einem Videorenderer gibt die abgeleitete Klasse in der Regel die Größe des nativen Videobilds zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




