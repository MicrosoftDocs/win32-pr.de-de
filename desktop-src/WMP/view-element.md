---
title: VIEW-Element
description: VIEW-Element
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player Skins, VIEW-Element
- skins,VIEW-Element
- VIEW-Element
- Referenz für Skins, VIEW-Element
- elements,VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d2b14f75d3cf5405c1663e23ad343e3c22bb2a80f60919de4505808cdf0a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571652"
---
# <a name="view-element"></a>VIEW-Element

Das **VIEW-Element** enthält die Benutzeroberflächendetails einer Skin und verwendet die Attribute, Methoden und Ereignishandler, die in den folgenden Tabellen gezeigt werden.

Mehrere **VIEW-Elemente** können als untergeordnete Elemente des **THEME-Elements** einer Skin definiert werden, um unterschiedliche Schnittstellen für verschiedene Situationen bereitzustellen. **VIEW-Elemente** können nicht als untergeordnete Elemente eines anderen Elements angegeben werden, und sie enthalten alle anderen Skinelemente. Beachten Sie, dass jede Ansicht über einen eigenen Variablenbereich verfügt, was bedeutet, dass attributwerte nicht für andere Ansichten freigegeben werden können.

Das globale **View-Attribut** kann verwendet werden, um von überall darin auf ein bestimmtes **VIEW-Element** zu verweisen. Dies ist eine Alternative zur Verwendung des **ID-Attributs,** das innerhalb anderer **VIEW-Elemente** oder innerhalb des **THEME-Elements** verwendet werden muss.

Das **VIEW-Element** unterstützt die folgenden Attribute. Attribute, die mit einem Sternchen () gekennzeichnet \* sind, werden auch vom **SUBVIEW-Element** unterstützt.



| attribute                                                       | Beschreibung                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Gibt die Hintergrundfarbe von **VIEW** oder **SUBVIEW** an oder ruft sie ab.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Gibt das Hintergrundbild von **VIEW** oder **SUBVIEW** an oder ruft es ab.                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Gibt die Menge an, um die der Farbton des Hintergrundbilds verschoben wird, oder ruft sie ab.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Gibt den Sättigungswert des Hintergrundbilds an oder ruft den Sättigungswert ab.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Gibt einen Wert an, der angibt, ob das Hintergrundbild der **VIEW-** oder **SUBVIEW-Ansicht** gekachelt ist, oder ruft einen Wert ab.         |
| [category](view-category.md)                                   | Gibt die Kategorie an, für die die Benutzeroberfläche angezeigt wird, oder ruft sie ab.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Gibt einen Wert an, der angibt, welches Element den Tastaturfokus besitzt, oder ruft einen Wert ab.                                             |
| [Maxheight](view-maxheight.md)                                 | Gibt die maximale Höhe der **ANSICHT** beim Ändern der Größe an oder ruft sie ab.                                                |
| [maxWidth](view-maxwidth.md)                                   | Gibt die maximale Breite der **ANSICHT** beim Ändern der Größe an oder ruft sie ab.                                                 |
| [Minheight](view-minheight.md)                                 | Gibt beim Ändern der Größe die mindeste Höhe der **VIEW-Ansicht** an oder ruft sie ab.                                                |
| [Minwidth](view-minwidth.md)                                   | Gibt beim Ändern der Größe die mindeste Breite der **ANSICHT** an oder ruft sie ab.                                                 |
| [Resizable](view-resizable.md)                                 | Gibt einen Wert an, der angibt, ob die **VIEW-Größe** geändert werden kann, oder ruft einen Wert ab.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Gibt einen Wert an, der angibt, ob die Größe des Hintergrundbilds geändert werden kann, oder ruft einen Wert ab.                                  |
| [scriptFile](view-scriptfile.md)                               | Gibt die Dateinamen der zugehörigen JScript Dateien an.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Gibt das Intervall in Millisekunden an, in dem der Timer Ereignisse an den **ontimer-Ereignishandler** ausgibt, oder ruft es ab. |
| [title](view-title.md)                                         | Gibt den Titel von **VIEW** an oder ruft den Titel ab. Kann nur zur Entwurfszeit festgelegt werden.                                       |
| [Titlebar](view-titlebar.md)                                   | Gibt einen Wert an, der angibt, ob die Fenstertitelleiste angezeigt wird, oder ruft einen Wert ab.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Gibt die Transparenzfarbe des Hintergrundbilds an oder ruft sie ab.                                                  |



 

Das **VIEW-Element** unterstützt die folgenden Methoden.



| Methode                                              | Beschreibung                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Schließt **view**.                                       |
| [Maximieren](view-maximize.md)                       | Maximiert **view**.                                    |
| [Minimieren](view-minimize.md)                       | Minimiert **view**.                                    |
| [restore](view-restore.md)                         | Stellt **view** wieder her.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Gibt den Benutzer in den vollständigen Modus von Windows Media Player zurück. |
| [size](view-size.md)                               | Die Größe der **VIEW-Ansicht** an einem angegebenen Rand wird geändert.                  |



 

Das **VIEW-Element** kann die folgenden Ereignishandler implementieren.



| Ereignishandler               | Beschreibung                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [Onclose](view-onclose.md) | Behandelt ein Ereignis, das auftritt, wenn **view** gerade geschlossen wird.      |
| [Onerror](view-onerror.md) | Behandelt ein Fehlerereignis, wenn **Einstellungen.enableErrorDialogs** auf FALSE festgelegt ist. |
| [Onload](view-onload.md)   | Behandelt ein Ereignis, das auftritt, wenn die **VIEW-Ansicht** zum ersten Mal angezeigt wird.         |
| [ontimer](view-ontimer.md) | Behandelt Timerereignisse.                                                      |



 

Das **VIEW-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren, sofern nicht angegeben. Weitere Informationen finden Sie unter [Ambient Attributes](ambient-attributes.md) and Ambient [Event Handlers](ambient-event-handlers.md),

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




