---
description: Stellt die Verwaltung von Zuordnungen von frei Hand Eingaben zum Anzeige Fenster dar. Verwenden Sie das inkrenderer-Objekt, um frei Hand Eingaben in einem Fenster anzuzeigen. Sie können es auch zum Neupositionieren und Ändern der Größe des Strichs verwenden.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Inkrenderer-Klasse (msink AUT. h)
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
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218577"
---
# <a name="inkrenderer-class"></a>Inkrenderer-Klasse

Stellt die Verwaltung von Zuordnungen von frei Hand Eingaben zum Anzeige Fenster dar. Verwenden Sie das **inkrenderer** -Objekt, um frei Hand Eingaben in einem Fenster anzuzeigen. Sie können es auch zum Neupositionieren und Ändern der Größe des Strichs verwenden.

Der **inkrenderer** verfügt über folgende Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **inkrenderer** -Klasse definiert.



| Schnittstelle        | BESCHREIBUNG                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **Iinkrenderer** | Dieses Objekt implementiert die **iinkrenderer** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **inkrenderer** -Klasse verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Zeichnet Striche in einem Gerätekontext.<br/>                                                                                                            |
| [**Drawstroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Zeichnet einen Strich im angegebenen Windows-Gerätekontext.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Ruft die Objekt Transformation ab, die zum RenderInk verwendet wurde.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Ruft die Ansichts Transformation ab, die zum RenderInk verwendet wird.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Konvertiert einen Speicherort in frei Hand Raumkoordinaten in Pixel Raum.<br/>                                                                            |
| [**Inkspacetopixelfrompoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Konvertiert ein Array von Punkten in frei Hand Raumkoordinaten in den Pixel Raum.<br/>                                                                          |
| [**Measure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Berechnet das Rechteck im Gerätekontext, das eine Auflistung von Strichen enthalten würde, wenn Sie mit dem **inkrenderer** -Objekt gezeichnet wurden.<br/> |
| [**Messrestroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Berechnet das Rechteck im Gerätekontext, das einen Strich enthalten würde, wenn Sie mit dem **inkrenderer** -Objekt gezeichnet wurden.<br/>                |
| [**Move**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Wendet eine Übersetzung auf die Ansichts Transformation in Freihand Raumkoordinaten an.<br/>                                                                         |
| [**Pixelesinkspace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Konvertiert einen Speicherort in Pixelkoordinaten in den frei Handbereich.<br/>                                                                                  |
| [**Pixelroinkspacefrompoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Konvertiert ein Array von Punkten in Pixel Raumkoordinaten in frei Hand Raum.<br/>                                                                          |
| [**Drehen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Wendet eine Drehung auf die Ansichts Transformation an.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Skaliert die Ansichts Transformation in der X-und Y-Dimension.<br/>                                                                                           |
| [**"Stobjecttransform"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Legt die Objekt Transformation fest, die zum RenderInk verwendet wird.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Legt die Ansichts Transformation fest, die zum RenderInk verwendet wird.<br/>                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Der Druckvorgang wird auch über das **inkrenderer** -Objekt durchgeführt.

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Renderer (Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Inkdrawingattributes-Klasse**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

