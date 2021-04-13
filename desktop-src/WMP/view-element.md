---
title: View-Element
description: View-Element
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player Skins, Ansichts Element
- Skins, Ansichts Element
- View-Element
- Verweis für Skins, Ansichts Element
- Elemente, Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388435"
---
# <a name="view-element"></a>View-Element

Das **View** -Element enthält die Benutzeroberflächen Details eines Skin und verwendet die in den folgenden Tabellen gezeigten Attribute, Methoden und Ereignishandler.

Mehrere **Ansichts** Elemente können als untergeordnete Elemente des Design **-Elements eines** Skin definiert werden, um verschiedene Schnittstellen für verschiedene Situationen bereitzustellen. **Ansichts** Elemente können nicht als untergeordnete Elemente eines anderen Elements angegeben werden, und Sie enthalten alle anderen Skin-Elemente. Beachten Sie, dass jede Sicht einen eigenen Variablen Bereich hat, d. h., Sie kann keine Attributwerte für andere Sichten freigeben.

Das **View** Global-Attribut kann verwendet werden, um von überall darin auf ein bestimmtes **Ansichts** Element zu verweisen. Dies ist eine Alternative zur Verwendung des **ID** -Attributs, das in anderen **Ansichts** Elementen oder innerhalb des **Theme** -Elements verwendet werden muss.

Das **View** -Element unterstützt die folgenden Attribute. Attribute, die mit einem Sternchen ( \* ) gekennzeichnet sind, werden auch vom **subview** -Element unterstützt.



| Attribut                                                       | BESCHREIBUNG                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [BackgroundColor](view-backgroundcolor.md)\*                  | Gibt die Hintergrundfarbe der **Ansicht** oder **unter Ansicht** an oder ruft diese ab.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Gibt das Hintergrundbild der **Ansicht** oder **unter Ansicht** an oder ruft es ab.                                             |
| [backgroundimagehueshift](view-backgroundimagehueshift.md)     | Gibt den Betrag an, um den der Farbton des Hintergrund Bilds verschoben wird, oder ruft diesen ab.                                  |
| [backgroundimagesationations](view-backgroundimagesaturation.md) | Gibt den Sättigungswert des Hintergrund Bilds an oder ruft ihn ab.                                                    |
| [backgroundkacheln](view-backgroundtiled.md)\*                  | Gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Hintergrundbild der **Ansicht** oder der **unter Ansicht** gekachelt wird.         |
| [category](view-category.md)                                   | Gibt die Kategorie an, für die die Benutzeroberfläche angezeigt wird, oder ruft Sie ab.                                           |
| [focusobjectid](view-focusobjectid.md)                         | Gibt einen Wert an, der angibt, welches Element den Tastaturfokus besitzt, oder ruft diesen ab                                             |
| [MaxHeight](view-maxheight.md)                                 | Gibt die maximale Höhe der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.                                                |
| [maxWidth](view-maxwidth.md)                                   | Gibt die maximale Breite der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.                                                 |
| [minHeight](view-minheight.md)                                 | Gibt die Mindesthöhe der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.                                                |
| [minWidth](view-minwidth.md)                                   | Gibt die minimale Breite der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.                                                 |
| [geändert](view-resizable.md)                                 | Gibt einen Wert an, der angibt, ob die **Ansicht** geändert werden kann, oder ruft ihn ab.                                          |
| [resizebackgroundimage](view-resizebackgroundimage.md)         | Gibt einen Wert an oder ruft ihn ab, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.                                  |
| [scriptFile](view-scriptfile.md)                               | Gibt die Dateinamen der begleitenden JScript-Dateien an.                                                                 |
| [TimerInterval](view-timerinterval.md)                         | Gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse in den **OnTimer** -Ereignishandler auslöst, oder ruft es ab. |
| [title](view-title.md)                                         | Gibt den Titel der **Ansicht** an oder ruft ihn ab. Kann nur zur Entwurfszeit festgelegt werden.                                       |
| [TitleBar](view-titlebar.md)                                   | Gibt einen Wert an, der angibt, ob die Fenstertitelleiste angezeigt wird, oder ruft diesen ab.                                        |
| [transparendcolor](view-transparencycolor.md)\*              | Gibt die Transparenz Farbe des Hintergrund Bilds an oder ruft diese ab.                                                  |



 

Das **View** -Element unterstützt die folgenden Methoden.



| Methode                                              | BESCHREIBUNG                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Schließt die **Ansicht**.                                       |
| [optimieren](view-maximize.md)                       | Maximiert die **Ansicht**.                                    |
| [Verkleinern](view-minimize.md)                       | Minimiert die **Ansicht**.                                    |
| [restore](view-restore.md)                         | Stellt die **Ansicht** wieder her.                                     |
| [returntomediacenter](view-returntomediacenter.md) | Gibt den Benutzer in den vollständigen Modus von Windows-Media Player zurück. |
| [size](view-size.md)                               | Ändert die Größe der **Ansicht** an einem angegebenen Rand.                  |



 

Das **View** -Element kann die folgenden Ereignishandler implementieren.



| Ereignishandler               | BESCHREIBUNG                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [OnClose](view-onclose.md) | Behandelt ein Ereignis, das auftritt, wenn die **Ansicht** geschlossen wird.      |
| [OnError](view-onerror.md) | Behandelt ein Fehler Ereignis, wenn **Settings. enableerrordialogs** auf false festgelegt ist. |
| [OnLoad](view-onload.md)   | Behandelt ein Ereignis, das auftritt, wenn die **Ansicht** zum ersten Mal angezeigt wird.         |
| [OnTimer](view-ontimer.md) | Behandelt Timer-Ereignisse.                                                      |



 

Das **View** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren, sofern nicht angegeben. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




