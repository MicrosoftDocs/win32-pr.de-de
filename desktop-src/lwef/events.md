---
title: Iagentnotifysink
description: Iagentnotifysink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038912"
---
# <a name="iagentnotifysink"></a>Iagentnotifysink

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Iagentnotifysink benachrichtigt Clients, wenn bestimmte Zustandsänderungen auftreten. Diese Funktionen sind auch über [iagentnotifysinkex](iagentnotifysinkex.md)verfügbar.

**Methoden in Vtable-Reihenfolge**



| Iagentnotifysink                                                      | BESCHREIBUNG                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**S**](command-method.md)                                     | Tritt auf, wenn der Server einen Client definierten Befehl verarbeitet.                               |
| [**Activatinput State**](iagentnotifysink--activateinputstate.md)    | Tritt auf, wenn ein Zeichen als Eingabe aktiv wird oder beendet wird.                            |
| [**Balloonvisiblestate**](iagentnotifysink---balloonvisiblestate.md) | Tritt ein, wenn der **sichtbare** Zustand des Zeichens geändert wird.                                   |
| [**Click-Ereignis**](click-event.md)                                    | Tritt auf, wenn auf ein Zeichen geklickt wird.                                                      |
| [**DblClick-Ereignis**](dblclick-event.md)                              | Tritt auf, wenn auf ein Zeichen Doppel geklickt wird.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Tritt auf, wenn ein Benutzer mit dem Ziehen eines Zeichens beginnt.                                          |
| [**Dragcomplete**](https://www.bing.com/search?q=**DragComplete**)                          | Tritt auf, wenn ein Benutzer das Ziehen eines Zeichens beendet.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Tritt auf, wenn der Server mit der Verarbeitung eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts beginnt.    |
| [**Requestcomplete**](iagentnotifysink--requestcomplete.md)          | Tritt auf, wenn der Server die Verarbeitung eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts abschließt. |
| [**Lesezeichen**](iagentnotifysink--bookmark.md)                        | Tritt auf, wenn der Server ein Lesezeichen verarbeitet.                                             |
| [**Idle**](iagentnotifysink--idle.md)                                | Tritt auf, wenn der Server die Leerlauf Verarbeitung startet oder beendet.                                   |
| [**Move**](iagentnotifysink--move.md)                                | Tritt auf, wenn ein Zeichen verschoben wurde.                                                  |
| [**Größe**](iagentnotifysink---size.md)                               | Tritt auf, wenn die Größe eines Zeichens geändert wurde.                                                |
| [**Balloonvisiblestate**](iagentnotifysink---balloonvisiblestate.md) | Tritt auf, wenn sich der Sichtbarkeits Zustand der Word-Sprechblase eines Zeichens ändert.                  |



 

Die iagentnotifysink:: Restart-und iagentnotifysink:: Shutdown-Ereignisse, die in früheren Versionen des Microsoft-Agents unterstützt wurden, sind mittlerweile veraltet. Der Server sendet diese Ereignisse nicht mehr, obwohl er aus Gründen der Abwärtskompatibilität unterstützt wird.

 

 