---
description: Die getminidealimagesize-Methode ruft die minimale ideale Bildgröße ab.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Cbasecontrolwindow. getminidealimagesize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352989"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>Cbasecontrolwindow. getminidealimagesize-Methode

Die- `GetMinIdealImageSize` Methode ruft die minimale ideale Bildgröße ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die minimale ideale Breite in Pixel.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die minimale ideale Höhe in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verschiedene Renderer haben Leistungsbeschränkungen hinsichtlich der Größe von Bildern, die Sie anzeigen können. Obwohl Sie weiterhin ordnungsgemäß funktionieren, wenn Sie aufgefordert werden, Bilder anzuzeigen, die über dem angegebenen Maximum liegen, können Renderer die minimalen und maximalen idealen Größen über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle nominieren. Diese Schnittstelle kann nur aufgerufen werden, wenn das Filter Diagramm angehalten oder ausgeführt wird, da es nicht bis zu dem Zeitpunkt ist, zu dem Ressourcen zugewiesen werden, und der Renderer seine Einschränkungen erkennen kann. Wenn keine Einschränkungen vorhanden sind, füllt der Renderer die *pWidth* -und *pHeight* -Parameter mit den nativen Video Dimensionen aus und gibt den Wert \_ false zurück. Wenn Einschränkungen vorhanden sind, werden die eingeschränkte Breite und Höhe eingegeben, und die Member-Funktion gibt "S OK" zurück \_ .

Die Dimensionen gelten für die Größe des Zielvideos und nicht für die gesamte Fenstergröße. Wenn Sie also die Größe des festzulegenden Fensters berechnen, berücksichtigen Sie die aktuellen Fenster Stile (z \_ . b. WS-Beschriftung und WS-Rahmen \_ ).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




