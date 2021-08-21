---
description: Stellt die Verwaltung von Zuordnungen von Ink zum Anzeigefenster dar. Verwenden Sie das InkRenderer-Objekt, um Ink in einem Fenster anzuzeigen. Sie können ihn auch verwenden, um Striche neu zu positionieren und deren Größe zu ändern.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: InkRenderer-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: f03b65a1ce009313b996fc7bede03f8c7425ff589fd29506c243f3161a851583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938720"
---
# <a name="inkrenderer-class"></a>InkRenderer-Klasse

Stellt die Verwaltung von Zuordnungen von Ink zum Anzeigefenster dar. Verwenden Sie das **InkRenderer-Objekt,** um Ink in einem Fenster anzuzeigen. Sie können ihn auch verwenden, um Striche neu zu positionieren und deren Größe zu ändern.

**InkRenderer** verfügt über diese Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkRenderer-Klasse** definiert.



| Schnittstelle        | BESCHREIBUNG                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Dieses Objekt implementiert die **IInkRenderer-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkRenderer-Klasse** verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Zeichnet Striche in einem Gerätekontext.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Zeichnet einen Strich im angegebenen Windows-Gerätekontext.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Ruft die Objekttransformation ab, die zum Rendern von Ink verwendet wurde.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Ruft die Ansichtstransformation ab, die zum Rendern von Ink verwendet wird.<br/>                                                                                      |
| [**Inkspacetopixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Konvertiert eine Position in Freihandraumkoordinaten in einen Pixelraum.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Konvertiert ein Array von Punkten in Freihandraumkoordinaten in Pixelraum.<br/>                                                                          |
| [**"Measure"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Berechnet das Rechteck im Gerätekontext, das eine Auflistung von Strichen enthalten würde, wenn sie mit dem **InkRenderer-Objekt** gezeichnet würden.<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Berechnet das Rechteck im Gerätekontext, das einen Strich enthalten würde, wenn sie mit dem **InkRenderer-Objekt** gezeichnet würden.<br/>                |
| [**Move**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Wendet eine Übersetzung auf die Ansichtstransformation in Freihandraumkoordinaten an.<br/>                                                                         |
| [**Pixeltoinkspace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Konvertiert eine Position in Pixelkoordinaten in Freihandraum.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Konvertiert ein Array von Punkten in Pixelraumkoordinaten in Freihandraum.<br/>                                                                          |
| [**Drehen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Wendet eine Drehung auf die Ansichtstransformation an.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Skaliert die Ansichtstransformation in der X- und Y-Dimension.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Legt die Objekttransformation fest, die zum Rendern von Ink verwendet wird.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Legt die Ansichtstransformation fest, die zum Rendern von Ink verwendet wird.<br/>                                                                                           |



 

## <a name="remarks"></a>Hinweise

Das Drucken erfolgt auch über das **InkRenderer-Objekt.**

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Renderereigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**InkDrawingAttributes-Klasse**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

