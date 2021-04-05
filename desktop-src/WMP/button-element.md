---
title: Button-Element (WMP)
description: Button-Element
ms.assetid: 2818ff6a-4fc5-4150-9ff9-ff143feb9204
keywords:
- Windows Media Player Skins, Button-Element
- Skins, Button-Element
- Button-Element
- Verweis für Skins, Button-Element
- Elemente, Schaltfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c069207e15be62e06b4d2b18f13c052026932dc
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2019
ms.locfileid: "103719607"
---
# <a name="button-element"></a>Button-Element

Das **Button** -Element bietet eine Möglichkeit zum Erstellen einer Schaltfläche in einem Skin. Die unten aufgeführten Attribute können verwendet werden, um das Verhalten einer Schaltfläche anzupassen, oder es kann eine vordefinierte Schaltfläche verwendet werden.

Das **Button** -Element unterstützt die folgenden Attribute.



| Attribut                                         | BESCHREIBUNG                                                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](button-cursor.md)                       | Gibt den Cursor an oder ruft ihn ab, der angezeigt wird, wenn mit dem Mauszeiger auf die **Schaltfläche** gezeigt wird.                                                |
| [disabledImage](button-disabledimage.md)         | Gibt das Bild an, das beim Deaktivieren der **Schaltfläche** angezeigt wird, oder ruft es ab.                                                                  |
| [auf](button-down.md)                           | Gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob sich die **Schaltfläche** an der nach-oben-oder                                                  |
| [Windows Mage](button-downimage.md)                 | Gibt das Bild an, das den Zustand der **Schaltfläche** nach unten darstellt, oder ruft es ab.                                                                  |
| [downtooltip](button-downtooltip.md)             | Gibt den QuickInfo-Text an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über der **Schaltfläche** befindet und sich die **Schaltfläche** im Zustand "gedrückt" |
| [hoverdownimage](button-hoverdownimage.md)       | Gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "gedrückt" befindet, und der Benutzer mit dem Mauszeiger darüber bewegt wird.          |
| [hoverimage](button-hoverimage.md)               | Gibt das Bild an, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "up" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt.            |
| [image](button-image.md)                         | Gibt das Standardbild der **Schaltfläche** an oder ruft es ab.                                                                                      |
| [Klebe](button-sticky.md)                       | Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob die **Schaltfläche** eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei oder einem Bundesstaat handelt         |
| [Ken](button-tiled.md)                         | Gibt einen Wert an, der angibt, ob das **Schalt** Flächen Bild angezeigt wird, oder ruft diesen ab.                                                            |
| [transparendcolor](button-transparencycolor.md) | Gibt die Farbe an, die im **Schalt** Flächen Bild transparent sein wird, oder ruft Sie ab.                                                               |
| [uptooltip](button-uptooltip.md)                 | Gibt den QuickInfo-Text an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über der **Schaltfläche** befindet und sich die **Schaltfläche** im Zustand "                |



 

Das **Button** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).

Vordefinierte Schaltflächen sind normale **Schalt** Flächen Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden. Die folgenden vordefinierten Schaltflächen sind verfügbar.



| Vordefinierte Schaltfläche                    | BESCHREIBUNG                                                                        |
|--------------------------------------|------------------------------------------------------------------------------------|
| [CLOSEBUTTON](closebutton.md)       | Eine **Schaltfläche** zum Schließen des Players.                                             |
| [Ffwdbutton](ffwdbutton.md)         | Eine **Schaltfläche** mit einem integrierten-Befehl für **Player. Controls. FastForward** , wenn darauf geklickt wird. |
| [Image Button](imagebutton.md)       | Eine **Schaltfläche** , mit der ein Bild angezeigt wird.                                             |
| [Minimizebutton](minimizebutton.md) | Eine **Schaltfläche** , mit der der Spieler minimiert wird.                                          |
| [MuteButton](mutebutton.md)         | Eine **Schaltfläche** , mit der die Audiodatei stumm geschaltet wird.                                   |
| [NEXTBUTTON](nextbutton.md)         | Eine **Schaltfläche** mit einem integrierten Befehl für **Player. Controls. Next** , wenn darauf geklickt wird.        |
| [Pausen Schaltfläche](pausebutton.md)       | Eine **Schaltfläche** mit einem integrierten Befehl für **Player. Controls. Pause** , wenn darauf geklickt wird.       |
| [PlayButton](playbutton.md)         | Eine **Schaltfläche** mit einem integrierten Befehl für **Player. Controls. Play** , wenn darauf geklickt wird.        |
| [Prevbutton](prevbutton.md)         | Eine **Schaltfläche** mit einem integrierten-Befehl für **Player. Controls. Previous** , wenn darauf geklickt wird.    |
| [REPEATBUTTON](repeatbutton.md)     | Eine **Schaltfläche** , die die Wiederholungs Option schaltet.                                       |
| [Returnbutton](returnbutton.md)     | Eine **Schaltfläche** , die Windows Media Player an das Mediencenter zurückgibt.                |
| [Rewbutton](rewbutton.md)           | Eine **Schaltfläche** mit einem integrierten-Befehl für **Player. Controls. fastreverse** , wenn darauf geklickt wird. |
| [Shufflebutton](shufflebutton.md)   | Eine **Schaltfläche** , die die Shuffle-Option umschaltet.                                      |
| [StopButton](stopbutton.md)         | Eine **Schaltfläche** mit einem integrierten Befehl für **Player. Controls. beenden** , wenn darauf geklickt wird.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




