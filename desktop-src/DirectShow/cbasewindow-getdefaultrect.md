---
description: Die getdefaultrect-Methode ruft die Standardgröße des Client Bereichs ab.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Cbasewindow. getdefaultrect-Methode (winutil. h)
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
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370684"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Cbasewindow. getdefaultrect-Methode

Die- `GetDefaultRect` Methode ruft die Standardgröße des Client Bereichs ab.

## <a name="syntax"></a>Syntax


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Standard Rechteck zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Fenster aktiviert ist, ruft das-Objekt diese Methode auf, um zu bestimmen, wie groß es den Client Bereich des Fensters machen soll. In der Basisklasse gibt diese Methode ein Rechteck zurück, dessen Höhe und Breite die definierten Konstanten "defheight" und "defwidth" sind. Eine abgeleitete Klasse sollte diese Methode überschreiben. Bei einem Videorenderer gibt die abgeleitete Klasse in der Regel die Größe des systemeigenen Video Bilds zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




