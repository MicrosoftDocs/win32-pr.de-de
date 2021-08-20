---
description: Stellt die Attribute dar, die beim Zeichnen auf Ink angewendet werden.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: InkDrawingAttributes-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 44b3ef1115539219f7cbf6b700014117ad180d15fe8cdd6d2afe4a0f783a06df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042348"
---
# <a name="inkdrawingattributes-class"></a>InkDrawingAttributes-Klasse

Stellt die Attribute dar, die beim Zeichnen auf Ink angewendet werden.

**InkDrawingAttributes** weist diese Typen von Membern auf:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkDrawingAttributes-Klasse** definiert.



| Schnittstelle                 | Beschreibung                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Dieses Objekt implementiert die **COM-Schnittstelle IInkDrawingAttributes.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkDrawingAttributes-Klasse** verfügt über diese Methoden.



| Methode                         | Beschreibung                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Erstellt ein doppeltes [**InkDisp-,**](inkdisp-class.md) **InkDrawingAttributes-** oder [**InkRecognizerContext-Objekt.**](inkrecognizercontext-class.md)<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkDrawingAttributes-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp           | Beschreibung                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Antialiased**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob die Vordergrund- und Hintergrundfarben entlang des Rands der Ink kombiniert werden, um die Glätte eines Ink-Strichs zu erhöhen, oder legt diesen fest.<br/> |
| [**Farbe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lesen/Schreiben<br/> | Ruft die Farbe der mit diesem **InkDrawingAttributes-Objekt gezeichneten InkDrawingAttributes-Farbe** ab oder legt diese fest.<br/>                                                                                    |
| [**Extendedproperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Schreibgeschützt<br/>  | Ruft die Auflistung anwendungsdefinierter Daten ab, die im **InkDrawingAttributes-Objekt** gespeichert sind.<br/>                                                                |
| [**Fittocurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob Ink als Reihe von Kurven anstatt als Linien zwischen Stift-Beispielpunkten gerendert wird, oder legt diesen fest.<br/>                                    |
| [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lesen/Schreiben<br/> | Ruft die Höhe des Stifts beim Zeichnen von **InkDrawingAttributes-Objekten** ab oder legt diese fest.<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob gezeichnete Ink mit erhöhtem Druck der Stiftspitze auf der Tablettoberfläche automatisch breiter wird, oder legt diesen fest.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lesen/Schreiben<br/> | Ruft die Stiftspitze ab, die beim Zeichnen von **InkDrawingAttributes-Objekten** (Kugel oder Rechteck) verwendet werden soll, oder legt diese fest.<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie die Stiftfarbe mit den vorhandenen Hintergrundfarben auf der Anzeige interagiert, wenn die Farbe gezeichnet wird.<br/>                                                    |
| [**Transparenz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lesen/Schreiben<br/> | Ruft den Transparenzwert von gezeichneter Ink ab oder legt ihn fest. Die Werte reichen von 0 (vollständig deckend) bis 255 (vollständig transparent).<br/>                                               |
| [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lesen/Schreiben<br/> | Ruft die Breite des Stifts beim Zeichnen von **InkDrawingAttributes-Objekten** ab oder legt diese fest.<br/>                                                                         |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Diese Zeichnungsattribute können einem Strich oder Cursor zugeordnet werden und Einstellungen wie Farbe, Breite und Transparenz angeben.

Um die Zeichnungsattribute eines Strichs anzugeben, verwenden Sie die [**DrawingAttributes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) des [**IInkStrokeDisp-Objekts.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Um die Zeichnungsattribute aller Striche innerhalb einer Auflistung von Strichen anzugeben, rufen Sie die [**ModifyDrawingAttributes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) der [InkStrokes-Auflistung auf.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

Jedes [**InkCollector-Objekt,**](inkcollector-class.md) [**InkOverlay-Objekt**](inkoverlay-class.md) und [InkPicture-Steuerelement](inkpicture-control-reference.md) kann einen anderen Satz von Zeichnungsattributen für denselben Cursor angeben. Verwenden Sie die [**DrawingAttributes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) des [**IInkCursor-Objekts,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) um die Zeichnungsattribute eines Cursors abzurufen oder festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DrawingAttributes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes-Eigenschaft**
</dt> <dt>

**DrawingAttributes-Eigenschaft**
</dt> <dt>

[**DefaultDrawingAttributes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**DefaultDrawingAttributes-Eigenschaft**
</dt> <dt>

**DefaultDrawingAttributes-Eigenschaft**
</dt> <dt>

[**ModifyDrawingAttributes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

