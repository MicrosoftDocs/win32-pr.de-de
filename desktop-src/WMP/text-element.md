---
title: Text-Element (Windows Media Player SDK)
description: Text-Element
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Windows Media Player Skins, Text-Element
- Skins, Text-Element
- Text-Element
- Verweis für Skins, Text-Element
- Elemente, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acdad737fda44cc0e090eb13fb20c765b447ccbd
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313601"
---
# <a name="text-element"></a>Text-Element

Das **Text** -Element bietet eine Möglichkeit, die Darstellung von Text in einem Skin mithilfe der folgenden Attribute zu erstellen und zu steuern. Vordefinierte **Text** Elemente werden aus Gründen der leichteren Bereitstellung bereitgestellt.

Das **Text** -Element unterstützt die folgenden Attribute.



| Attribut                                                   | BESCHREIBUNG                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Background Color](text-backgroundcolor.md)                 | Gibt die Hintergrundfarbe für das Text Steuerelement an oder ruft diese ab.                                           |
| [Cursor](text-cursor.md)                                   | Gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Text Steuerelement befindet     |
| [disabledbackgroundcolor](text-disabledbackgroundcolor.md) | Gibt die für das Text Steuerelement verwendete Hintergrundfarbe an oder ruft diese ab, wenn diese deaktiviert ist.                  |
| [disabledfontstyle](text-disabledfontstyle.md)             | Gibt den Schrift Schnitt an, der für das Text Steuerelement verwendet wird, wenn er deaktiviert ist.                        |
| [disabledforegroundcolor](text-disabledforegroundcolor.md) | Gibt die Textfarbe an oder ruft Sie ab, die verwendet wird, wenn das Text Steuerelement deaktiviert ist.                               |
| [fontface](text-fontface.md)                               | Gibt die Schriftart für das Text Steuerelement an oder ruft diese ab.                                                   |
| [FontSize](text-fontsize.md)                               | Gibt den Schrift Grad für das Text Steuerelement an oder ruft ihn ab.                                                  |
| [FON-moothing](text-fontsmoothing.md)                     | Gibt einen Wert an, der angibt, ob die Schriftart Glättung aktiviert ist.                                |
| [FontStyle](text-fontstyle.md)                             | Gibt den Schrift Schnitt für das Text Steuerelement an oder ruft ihn ab.                                                 |
| [ForegroundColor](text-foregroundcolor.md)                 | Gibt die Textfarbe für das Text Steuerelement an oder ruft diese ab.                                                 |
| [hoverbackgroundcolor](text-hoverbackgroundcolor.md)       | Gibt die für das Text Steuerelement verwendete Hintergrundfarbe an oder ruft diese ab, wenn mit dem Mauszeiger darauf gezeigt wird. |
| [hoverfontstyle](text-hoverfontstyle.md)                   | Gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn mit dem Mauszeiger darauf gezeigt wird, oder ruft diesen ab.       |
| [hoverforegroundcolor](text-hoverforegroundcolor.md)       | Gibt die Textfarbe an, die für das Text Steuerelement verwendet wird, wenn der Mauszeiger darüber bewegt wird, oder ruft Sie ab.       |
| [Recht](text-justification.md)                     | Gibt die Ausrichtung des Texts im Text Steuerelement an oder ruft diese ab.                                   |
| [Scroll](text-scrolling.md)                             | Gibt einen Wert an, der angibt, ob der Text durch einen Bildlauf führt                                         |
| [scrollingamount](text-scrollingamount.md)                 | Gibt die Anzahl der Pixel an, die der Text während jeder scrollbewegung bewegt, oder ruft diese ab.             |
| [scrollingdelay](text-scrollingdelay.md)                   | Gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft diese ab.                                          |
| [scrollingdirection](text-scrollingdirection.md)           | Gibt die Richtung des scrolltexts an oder ruft diese ab.                                                 |
| [TextWidth](text-textwidth.md)                             | Ruft die Breite der Zeichenfolge in Pixel ab, die im **value** -Attribut enthalten ist.                           |
| [QuickInfo](text-tooltip.md)                                 | Gibt den QuickInfo-Text für das Text Steuerelement an oder ruft ihn ab.                                               |
| [value](text-value.md)                                     | Gibt den Text an, der im Text Steuerelement angezeigt wird, oder ruft ihn ab.                                      |
| [WordWrap](text-wordwrap.md)                               | Gibt einen Wert an, der angibt, ob das Zeilenumbruch aktiviert oder deaktiviert ist, oder ruft diesen ab.                     |



 

Das **Text** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).

Vordefinierte Textelemente sind normale **Text** Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden. Die folgenden vordefinierten Textelemente sind verfügbar.



| Vordefinierter Text                                | BESCHREIBUNG                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Currentpositiontext](currentpositiontext.md) | Ein **Text** Element mit einem integrierten Listener für **Player. Controls. currentpositionstring**. |
| [Durationtext](durationtext.md)               | Ein **Text** Element mit einem integrierten Listener für " **Player. currentMedia. durationString**".    |
| [Status Text](statustext.md)                   | Ein **Text** Element mit einem integrierten Listener für **Player. Status**.                         |
| [Tracknametext](tracknametext.md)             | Ein **Text** Element mit einem integrierten Listener für **Player.currentMedia.Name**.              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




