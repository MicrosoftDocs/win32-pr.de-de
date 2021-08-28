---
title: BUTTON-Element (WMP)
description: BUTTON-Element
ms.assetid: 2818ff6a-4fc5-4150-9ff9-ff143feb9204
keywords:
- Windows Media Player,BUTTON-Element
- skins,BUTTON-Element
- BUTTON-Element
- Referenz für Skins, BUTTON-Element
- elements,BUTTON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ca4e57dafdc01fc194c4cf4bc534e067297a58fcc2527939e3672f2d705628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736730"
---
# <a name="button-element"></a>BUTTON-Element

Das **BUTTON-Element** bietet eine Möglichkeit, eine Schaltfläche in einer Skin zu erstellen. Die folgenden Attribute können verwendet werden, um das Verhalten einer Schaltfläche anzupassen, oder eine vordefinierte Schaltfläche kann der Einfachheit halber verwendet werden.

Das **BUTTON-Element** unterstützt die folgenden Attribute.



| attribute                                         | Beschreibung                                                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](button-cursor.md)                       | Gibt den Cursor an, der angezeigt wird, wenn der Mauszeiger auf button zeigt, oder ruft **diesen ab.**                                                |
| [disabledImage](button-disabledimage.md)         | Gibt das Bild an, das angezeigt wird, wenn button deaktiviert ist, **oder** ruft es ab.                                                                  |
| [down](button-down.md)                           | Gibt einen Wert an oder ruft einen Wert ab, der angibt, ob **sich button** an der Position nach oben oder unten befindet.                                                  |
| [downImage](button-downimage.md)                 | Gibt das Bild an, das den Zustand "Down" der SCHALTFLÄCHE darstellt, oder ruft **es ab.**                                                                  |
| [downToolTip](button-downtooltip.md)             | Gibt den QuickInfo-Text an oder ruft diesen ab, der angezeigt wird, wenn sich der Mauszeiger über der **SCHALTFLÄCHE** befindet und sich **button** im nach unten oder unten geschwungenen Zustand befindet. |
| [hoverDownImage](button-hoverdownimage.md)       | Gibt das Bild an, das angezeigt wird, wenn sich **die SCHALTFLÄCHE** im Zustand "Down" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.          |
| [hoverImage](button-hoverimage.md)               | Gibt das Bild an, das angezeigt wird, wenn sich **die SCHALTFLÄCHE** im Auf-Zustand befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.            |
| [image](button-image.md)                         | Gibt das Standardbild von BUTTON an oder ruft **es ab.**                                                                                      |
| [Klebrig](button-sticky.md)                       | Gibt einen Wert an oder ruft einen Wert ab, der angibt, ob es sich bei **button** um eine Umschaltfläche handelt, d. b. ob es sich um eine Schaltfläche mit zwei oder einem Zustand handelt.         |
| [Gekachelte](button-tiled.md)                         | Gibt einen Wert an, der angibt, ob das **BUTTON-Bild** gekachelt wird, oder ruft einen Wert ab.                                                            |
| [transparencyColor](button-transparencycolor.md) | Gibt die Farbe an, die im BUTTON-Bild transparent ist, oder **ruft sie** ab.                                                               |
| [upToolTip](button-uptooltip.md)                 | Gibt den QuickInfo-Text an oder ruft diesen ab, der angezeigt wird, wenn sich der Mauszeiger über **button** befindet und sich **button** im Auf-Zustand befindet.                |



 

Das **BUTTON-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient Attributes (Umgebungsattribute)](ambient-attributes.md) [und Ambient Event Handlers (Umgebungsereignishandler).](ambient-event-handlers.md)

Vordefinierte Schaltflächen sind normale **BUTTON-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Schaltflächen sind verfügbar.



| Vordefinierte SCHALTFLÄCHE                    | Beschreibung                                                                        |
|--------------------------------------|------------------------------------------------------------------------------------|
| [CLOSEBUTTON](closebutton.md)       | Eine **SCHALTFLÄCHE,** die zum Schließen des Players verwendet wird.                                             |
| [FFWDBUTTON](ffwdbutton.md)         | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.fastForward,** wenn darauf geklickt wird. |
| [Imagebutton](imagebutton.md)       | Eine **SCHALTFLÄCHE,** die zum Anzeigen eines Bilds verwendet wird.                                             |
| [MINIMIZEBUTTON](minimizebutton.md) | Eine **SCHALTFLÄCHE,** die verwendet wird, um den Player zu minimieren.                                          |
| [MUTEBUTTON](mutebutton.md)         | Eine **SCHALTFLÄCHE,** die zum Stummschalten und Ent stummschalten des Audios verwendet wird.                                   |
| [NEXTBUTTON](nextbutton.md)         | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.next,** wenn darauf geklickt wird.        |
| [PAUSEBUTTON](pausebutton.md)       | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.pause,** wenn darauf geklickt wird.       |
| [Playbutton](playbutton.md)         | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.play, wenn** darauf geklickt wird.        |
| [PREVBUTTON](prevbutton.md)         | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.previous, wenn** darauf geklickt wird.    |
| [Repeatbutton](repeatbutton.md)     | Eine **SCHALTFLÄCHE,** die die Option Wiederholen umschaltet.                                       |
| [RETURNBUTTON](returnbutton.md)     | Eine **SCHALTFLÄCHE,** die Windows Media Player an das Mediencenter zurückgibt.                |
| [REWBUTTON](rewbutton.md)           | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.fastReverse, wenn** darauf geklickt wird. |
| [SHUFFLEBUTTON](shufflebutton.md)   | Eine **SCHALTFLÄCHE,** die die Option Shuffle umschaltet.                                      |
| [STOPBUTTON](stopbutton.md)         | Eine **SCHALTFLÄCHE** mit einem integrierten Aufruf von **player.controls.stop, wenn** darauf geklickt wird.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




