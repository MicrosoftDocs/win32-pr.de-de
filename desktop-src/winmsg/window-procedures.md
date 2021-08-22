---
description: In diesem Abschnitt werden Fensterverfahren erläutert. Jedem Fenster ist eine Fensterprozedur zugeordnet, die alle Nachrichten verarbeitet, die an alle Fenster der -Klasse gesendet oder gesendet werden.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Fenster-Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7892c1547d7f5ed1bf5d70a9242e3bb5bc6a3c8e93121470d27ecbd64fb912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548460"
---
# <a name="window-procedures"></a>Fenster-Prozeduren

Jedem Fenster ist eine Fensterprozedur zugeordnet– eine Funktion, die alle Nachrichten verarbeitet, die an alle Fenster der -Klasse gesendet oder gesendet werden. Alle Aspekte der Darstellung und des Verhaltens eines Fensters hängen von der Antwort der Fensterprozedur auf diese Meldungen ab.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                         | Beschreibung                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Fensterverfahren](about-window-procedures.md)       | Erläutert Fensterverfahren. Jedes Fenster ist ein Member einer bestimmten Fensterklasse. Die Window-Klasse bestimmt die Standardfensterprozedur, die ein einzelnes Fenster zum Verarbeiten seiner Meldungen verwendet.<br/> |
| [Verwenden von Fenster-Prozeduren](using-window-procedures.md)       | Hier erfahren Sie, wie Sie die folgenden Aufgaben ausführen, die fenster-Prozeduren zugeordnet sind.<br/>                                                                                                                        |
| [Referenz zu Fensterprozeduren](window-procedure-reference.md) | Enthält die API-Referenz.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Functions



| Name                                     | Beschreibung                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Übergibt Nachrichteninformationen an die angegebene Fensterprozedur. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Ruft die Standardfensterprozedur auf, um die Standardverarbeitung für alle Fenstermeldungen zu ermöglichen, die von einer Anwendung nicht verarbeitet werden. Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) wird mit den gleichen Parametern aufgerufen, die von der Fensterprozedur empfangen werden. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Eine anwendungsdefinierte Funktion, die Nachrichten verarbeitet, die an ein Fenster gesendet werden. Der **WNDPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*WindowProc ist*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/>                                                            |



 

 

 
