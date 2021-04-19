---
description: Die getmaxidealimagesize-Methode ruft die maximale ideale Bildgröße ab.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Cbasecontrolwindow. getmaxidealimagesize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367021"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a>Cbasecontrolwindow. getmaxidealimagesize-Methode

Die- `GetMaxIdealImageSize` Methode ruft die maximale ideale Bildgröße ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die maximale ideale Breite in Pixel.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die maximale ideale Höhe in Pixel.

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

 

 




