---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43a092ddd9c50ff7aacb0254c4773a43005759ab23b6682aaf6484d5aef4839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725780"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

IAgentNotifySink benachrichtigt Clients, wenn bestimmte Zustandsänderungen auftreten. Diese Funktionen sind auch über [IAgentNotifySinkEx verfügbar.](iagentnotifysinkex.md)

**Methoden in Vtable-Reihenfolge**



| IAgentNotifySink                                                      | Beschreibung                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Befehl**](command-method.md)                                     | Tritt auf, wenn der Server einen clientdefinierten Befehl verarbeitet.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Tritt ein, wenn ein Zeichen eingabeaktiv wird oder nicht mehr aktiv ist.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Tritt ein, wenn sich der **Visible-Zustand des** Zeichens ändert.                                   |
| [**Click-Ereignis**](click-event.md)                                    | Tritt ein, wenn auf ein Zeichen geklickt wird.                                                      |
| [**DblClick-Ereignis**](dblclick-event.md)                              | Tritt ein, wenn auf ein Zeichen doppelt geklickt wird.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Tritt ein, wenn ein Benutzer mit dem Ziehen eines Zeichens beginnt.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Tritt ein, wenn ein Benutzer das Ziehen eines Zeichens beendet.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Tritt ein, wenn der Server mit der Verarbeitung eines [**Request-Objekts**](/windows/desktop/lwef/the-request-object) beginnt.    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Tritt ein, wenn der Server die Verarbeitung eines [**Request-Objekts**](/windows/desktop/lwef/the-request-object) abgeschlossen hat. |
| [**Lesezeichen**](iagentnotifysink--bookmark.md)                        | Tritt auf, wenn der Server ein Lesezeichen verarbeitet.                                             |
| [**Idle**](iagentnotifysink--idle.md)                                | Tritt ein, wenn der Server die Verarbeitung im Leerlauf startet oder beendet.                                   |
| [**Move**](iagentnotifysink--move.md)                                | Tritt ein, wenn ein Zeichen verschoben wurde.                                                  |
| [**Größe**](iagentnotifysink---size.md)                               | Tritt ein, wenn die Größe eines Zeichens geändert wurde.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Tritt ein, wenn sich der Sichtbarkeitszustand des Wortsprechblasens eines Zeichens ändert.                  |



 

Die Ereignisse IAgentNotifySink::Restart und IAgentNotifySink::Shutdown, die in früheren Versionen von Microsoft Agent unterstützt wurden, sind jetzt veraltet. Der Server wird zwar aus Gründen der Abwärtskompatibilität unterstützt, sendet diese Ereignisse jedoch nicht mehr.

 

 