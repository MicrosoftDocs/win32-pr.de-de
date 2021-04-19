---
description: Die getBorderColor-Methode ruft die aktuelle Fensterrahmen Farbe (m \_ BorderColor) ab.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Cbasecontrolwindow. getBorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367083"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Cbasecontrolwindow. getBorderColor-Methode

Die- `GetBorderColour` Methode ruft die aktuelle Fensterrahmen Farbe ( **m \_ BorderColor**) ab.

## <a name="syntax"></a>Syntax


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Farbe des Rahmens zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann ein Ziel Rechteck festlegen, um das Video anzuzeigen. Dieses Rechteck sollte relativ zum Client Bereich des Fensters sein. Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Bereich, in dem das Video umgeben ist. Das heißt, der Rahmen. Die Rahmenfarbe kann über die Funktion " [**cbasecontrolwindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) Member" festgelegt werden. Diese Eigenschaft wirkt sich auf die Rahmenfarbe aus. Verwenden Sie diese Member-Funktion anstelle von [**cbasecontrolwindow:: get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), es sei denn, Sie rufen dies extern über die [**IVideoWindow:: get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




