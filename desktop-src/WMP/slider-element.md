---
title: SLIDER-Element
description: SLIDER-Element
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Windows Media Player Skins, SLIDER-Element
- skins,SLIDER-Element
- SLIDER-Element
- Referenz für Skins, SLIDER-Element
- elements,SLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140c84f6bec826b34ff4e1c5a4a3365d44ba9aa67ca9504cea642aba25f076d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569087"
---
# <a name="slider-element"></a>SLIDER-Element

Das **SLIDER-Element** bietet eine Möglichkeit, ein einfaches horizontales oder vertikales Schieberegler-Steuerelement zu erstellen und zu bearbeiten. Sie unterstützt die folgenden Attribute und Ereignishandler. Der Einfachheit halber werden auch vordefinierte **SLIDER-Elemente** bereitgestellt.

Das **SLIDER-Element** unterstützt die folgenden Attribute.



| attribute                                                 | Beschreibung                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](slider-backgroundcolor.md)             | Gibt die Hintergrundfarbe des Schieberegler-Steuerelements an oder ruft sie ab.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Gibt die Hintergrundendfarbe des Schieberegler-Steuerelements an oder ruft sie ab.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Gibt das Hintergrundbild des Schiebereglers an, der angezeigt wird, wenn er mit der Maus darauf zeigt, oder ruft es ab.      |
| [backgroundImage](slider-backgroundimage.md)             | Gibt das Standardhintergrundbild des Schiebereglers an oder ruft es ab.                                                |
| [borderSize](slider-bordersize.md)                       | Gibt die Rahmengröße in Pixel an oder ruft sie ab.                                                                 |
| [Cursor](slider-cursor.md)                               | Gibt einen Wert an, der angibt, welcher Cursortyp angezeigt wird, wenn sich der Mauszeiger über dem Schieberegler-Steuerelement befindet, oder ruft einen Wert ab. |
| [direction](slider-direction.md)                         | Gibt die Richtung an, in der Schiebereglerbilder angeordnet werden, oder ruft diese ab.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Gibt die deaktivierte Farbe des Schieberegler-Steuerelements an oder ruft sie ab.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Gibt das Bild des Schiebereglers an, der angezeigt wird, wenn das Steuerelement deaktiviert ist, oder ruft es ab.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Gibt die Vordergrundfarbe des Schieberegler-Steuerelements an oder ruft sie ab.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Gibt die Vordergrundendefarbe des Schieberegler-Steuerelements an oder ruft sie ab.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Gibt das Vordergrundbild des Schiebereglers an, der angezeigt wird, wenn er mit der Maus darauf zeigt, oder ruft es ab.      |
| [foregroundImage](slider-foregroundimage.md)             | Gibt das Standardvordergrundbild des Schiebereglers an oder ruft es ab.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Gibt die aktuelle Position der Vordergrund-Statusleiste als Prozentsatz des Schiebereglerbereichs an oder ruft sie ab.    |
| [max](slider-max.md)                                     | Gibt den maximalen Wert des bereichs an, der vom Schieberegler-Steuerelement definiert wird, oder ruft den Wert ab.                              |
| [min](slider-min.md)                                     | Gibt den Minimalwert des bereichs an, der vom Schieberegler-Steuerelement definiert wird, oder ruft den Wert ab.                              |
| [Folie](slider-slide.md)                                 | Gibt einen Wert an, der angibt, ob das Vordergrundbild über das Hintergrundbild gleitet, oder ruft einen Wert ab.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Gibt das deaktivierte Schiebereglerbild des Schieberegler-Steuerelements an oder ruft es ab.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Gibt das Bild an, das den Abwärtszustand des Daumens darstellt, oder ruft es ab.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Gibt das Bild des Daumens an, das angezeigt wird, wenn mit der Maus darauf zeigt, oder ruft es ab.                  |
| [thumbImage](slider-thumbimage.md)                       | Gibt das Bild an, das zur Darstellung der aktuellen Position des Schiebereglers verwendet wird, oder ruft es ab.               |
| [Gekachelte](slider-tiled.md)                                 | Gibt einen Wert an, der angibt, ob die Schiebereglerbilder gekachelt werden, oder ruft einen Wert ab.                                |
| [Quickinfo](slider-tooltip.md)                             | Gibt den QuickInfo-Text für das Schieberegler-Steuerelement an oder ruft den Text ab.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Gibt die transparente Farbe der Schiebereglerbilder an oder ruft sie ab.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Gibt einen Wert an, der angibt, ob die Vordergrund-Statusanzeige verwendet wird, oder ruft einen Wert ab.                       |
| [value](slider-value.md)                                 | Gibt die aktuelle Position des Schiebereglers an und ruft sie ab.                                                       |



 

Das **SLIDER-Element** kann die folgenden Ereignishandler implementieren.



| Ereignishandler                                   | Beschreibung                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Behandelt ein Ereignis, das auftritt, wenn der Benutzer klickt und die linke Maustaste gedrückt hält und beginnt, die Maus zu ziehen. |
| [onDragEnd](slider-ondragend.md)               | Behandelt ein Ereignis, das auftritt, wenn die linke Maustaste nach einem Ziehvorgang losgelassen wird.                      |
| [onPositionChange](slider-onpositionchange.md) | Behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers ändert, wenn der Benutzer klickt oder zieht.   |



 

Das **SLIDER-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient Attributes](ambient-attributes.md) und Ambient [Event Handlers](ambient-event-handlers.md).

Vordefinierte Schieberegler sind normale **SLIDER-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Schieberegler sind verfügbar.



| Vordefinierter SLIDER                  | Beschreibung                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | Ein **SCHIEBEREGLER,** der zum Festlegen des Audioausgleichs verwendet wird.                        |
| [SEEKSLIDER](seekslider.md)       | Ein **SCHIEBEREGLER,** der verwendet wird, um eine beliebige Position innerhalb einer Mediendatei zu suchen. |
| [VOLUMESLIDER](volumeslider.md)   | Ein **SCHIEBEREGLER,** der zum Festlegen der Audiolautstärke verwendet wird.                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




