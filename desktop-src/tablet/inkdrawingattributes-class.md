---
description: Stellt die Attribute dar, die beim Zeichnen auf frei Hand Eingaben angewendet werden.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Inkdrawingattributes-Klasse (msink AUT. h)
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
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347908"
---
# <a name="inkdrawingattributes-class"></a>Inkdrawingattributes-Klasse

Stellt die Attribute dar, die beim Zeichnen auf frei Hand Eingaben angewendet werden.

**Inkdrawingattributes** verfügt über diese Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **inkdrawingattributes** -Klasse definiert.



| Schnittstelle                 | BESCHREIBUNG                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **Iinkdrawingattributes** | Dieses Objekt implementiert die **iinkdrawingattributes** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **inkdrawingattributes** -Klasse verfügt über diese Methoden.



| Methode                         | BESCHREIBUNG                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Erstellt ein doppeltes [**InkDisp**](inkdisp-class.md)-, **inkdrawingattributes**-oder [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **inkdrawingattributes** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Geglättet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lesen/Schreiben<br/> | Ruft den-Wert ab, der angibt, ob die Vordergrund-und Hintergrundfarben entlang der Kante des frei Hand Zeigern gemischt werden, um die Glätte eines frei Hand Strichs zu vergrößern.<br/> |
| [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lesen/Schreiben<br/> | Ruft die Farbe der mit diesem **inkdrawingattributes** -Objekt gezeichneten frei Handschrift ab oder legt diese fest.<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Schreibgeschützt<br/>  | Ruft die Auflistung von Anwendungs definierten Daten ab, die im **inkdrawingattributes** -Objekt gespeichert sind.<br/>                                                                |
| [**Fitum Curve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lesen/Schreiben<br/> | Ruft den-Wert ab, der angibt, ob frei Hand Eingaben als eine Reihe von Kurven anstelle von Linien zwischen Stift-Stichprobenpunkten gerendert werden.<br/>                                    |
| [**Höhe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lesen/Schreiben<br/> | Ruft die Höhe des Stifts beim Zeichnen von frei Hand Eingaben mit diesem **inkdrawingattributes** -Objekt ab oder legt diese fest.<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lesen/Schreiben<br/> | Ruft den Wert ab oder legt ihn fest, der angibt, ob das Zeichnen von frei Hand Eingaben mit erhöhtem Druck der Stift Spitze auf der Tablet-Oberfläche breiter wird.<br/>                     |
| [**Trinkgeld**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lesen/Schreiben<br/> | Ruft den zu verwendenden Stift Tipp (Ball oder Rechteck) beim Zeichnen von frei Hand Eingaben mit diesem **inkdrawingattributes** -Objekt ab oder legt diesen fest.<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie die Stift Farbe mit den vorhandenen Hintergrundfarben auf der Anzeige interagiert, wenn die frei Hand Eingaben gezeichnet werden.<br/>                                                    |
| [**Transparenz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lesen/Schreiben<br/> | Ruft den Transparenz Wert der gezeichneten frei Hand Eingabe ab oder legt ihn fest Die Werte reichen von 0 (null) bis 255 (vollständig transparent).<br/>                                               |
| [**Breite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lesen/Schreiben<br/> | Ruft die Breite des Stifts beim Zeichnen von Ink mit diesem **inkdrawingattributes** -Objekt ab oder legt diese fest.<br/>                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Diese Zeichnungs Attribute können einem Strich oder Cursor zugeordnet werden und legen Einstellungen wie Farbe, Breite und Transparenz fest.

Um die Zeichnungs Attribute eines Strichs anzugeben, verwenden Sie die [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) -Eigenschaft des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts. Um die Zeichnungs Attribute aller Striche innerhalb einer Auflistung von Strichen anzugeben, nennen Sie die [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) -Methode der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung.

Jedes [**InkCollector**](inkcollector-class.md) -Objekt, [**InkOverlay**](inkoverlay-class.md) -Objekt und [InkPicture](inkpicture-control-reference.md) -Steuerelement können einen anderen Satz von Zeichnungs Attributen für denselben Cursor angeben. Verwenden Sie die [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) -Eigenschaft des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts, um die Zeichnungs Attribute eines Cursors zu erhalten oder festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DrawingAttributes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes-Eigenschaft**
</dt> <dt>

**DrawingAttributes-Eigenschaft**
</dt> <dt>

[**DefaultDrawingAttributes (Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**DefaultDrawingAttributes (Eigenschaft)**
</dt> <dt>

**DefaultDrawingAttributes (Eigenschaft)**
</dt> <dt>

[**ModifyDrawingAttributes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

