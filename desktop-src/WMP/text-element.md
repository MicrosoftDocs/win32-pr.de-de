---
title: TEXT-Element (Windows Media Player SDK)
description: TEXT-Element
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Windows Media Player Skins, TEXT-Element
- skins,TEXT-Element
- TEXT-Element
- Referenz für Skins, TEXT-Element
- elements,TEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c0d30393ef4fdeb62061ee58b0c7bd2f3f58bd685945e62c0e8062f22d881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122850"
---
# <a name="text-element"></a>TEXT-Element

Das **TEXT-Element** bietet eine Möglichkeit, die Darstellung von Text innerhalb einer Skin mithilfe der folgenden Attribute zu erstellen und zu steuern. Der Einfachheit halber werden auch vordefinierte **TEXT-Elemente** bereitgestellt.

Das **TEXT-Element** unterstützt die folgenden Attribute.



| attribute                                                   | Beschreibung                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](text-backgroundcolor.md)                 | Gibt die Hintergrundfarbe für das Text-Steuerelement an oder ruft sie ab.                                           |
| [Cursor](text-cursor.md)                                   | Gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Text-Steuerelement befindet, oder ruft einen Wert ab.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Gibt die Hintergrundfarbe an, die für das Text-Steuerelement verwendet wird, wenn es deaktiviert ist, oder ruft sie ab.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Gibt den Schriftschnitt an, der für das Text-Steuerelement verwendet wird, wenn es deaktiviert ist, oder ruft ihn ab.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Gibt die Textfarbe an, die verwendet wird, wenn das Text-Steuerelement deaktiviert ist, oder ruft sie ab.                               |
| [fontFace](text-fontface.md)                               | Gibt die Schriftart für das Text-Steuerelement an oder ruft sie ab.                                                   |
| [Fontsize](text-fontsize.md)                               | Gibt den Schriftgrad für das Text-Steuerelement an oder ruft den Schriftgrad ab.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Gibt einen Wert an, der angibt, ob die Schriftartglättung aktiviert ist, oder ruft einen Wert ab.                                |
| [Fontstyle](text-fontstyle.md)                             | Gibt den Schriftschnitt für das Text-Steuerelement an oder ruft den Schriftschnitt ab.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Gibt die Textfarbe für das Text-Steuerelement an oder ruft sie ab.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Gibt die Hintergrundfarbe an, die für das Text-Steuerelement verwendet wird, wenn der Mauszeiger darauf zeigt, oder ruft sie ab. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Gibt den Schriftschnitt an, der für das Text-Steuerelement verwendet wird, wenn der Mauszeiger darauf zeigt, oder ruft ihn ab.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Gibt die Textfarbe an, die für das Text-Steuerelement verwendet wird, wenn der Mauszeiger darauf zeigt, oder ruft sie ab.       |
| [Rechtfertigung](text-justification.md)                     | Gibt die Ausrichtung des Texts im Text-Steuerelement an oder ruft diese ab.                                   |
| [Scrollen](text-scrolling.md)                             | Gibt einen Wert an, der angibt, ob der Text scrollt, oder ruft einen Wert ab.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Gibt die Anzahl der Pixel an, die der Text während jeder Bildlaufbewegung verschoben wird, oder ruft sie ab.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft sie ab.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Gibt die Richtung des Bildlauftexts an oder ruft diese ab.                                                 |
| [Textwidth](text-textwidth.md)                             | Ruft die Breite der im **Value-Attribut** enthaltenen Zeichenfolge in Pixel ab.                           |
| [Quickinfo](text-tooltip.md)                                 | Gibt den QuickInfo-Text für das Textsteuerelement an oder ruft den Text ab.                                               |
| [value](text-value.md)                                     | Gibt den Text an, der im Text-Steuerelement angezeigt wird, oder ruft diesen ab.                                      |
| [Wordwrap](text-wordwrap.md)                               | Gibt einen Wert an, der angibt, ob Zeilenumbruch aktiviert oder deaktiviert ist, oder ruft einen Wert ab.                     |



 

Das **TEXT-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient Attributes](ambient-attributes.md) und Ambient [Event Handlers](ambient-event-handlers.md).

Vordefinierte Textelemente sind normale **TEXT-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Textelemente sind verfügbar.



| Vordefinierter TEXT                                | Beschreibung                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Ein **TEXT-Element** mit einem integrierten Listener für **player.controls.currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Ein **TEXT-Element** mit einem integrierten Listener für **player.currentMedia.DurationString**.    |
| [Statustext](statustext.md)                   | Ein **TEXT-Element** mit einem integrierten Listener für **player.status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Ein **TEXT-Element** mit einem integrierten Listener für **player.currentMedia.name**.              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




