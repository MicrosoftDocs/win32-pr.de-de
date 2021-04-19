---
description: In diesem Abschnitt werden Fenster Prozeduren erläutert. Jedes Fenster verfügt über eine zugeordnete Fenster Prozedur, die alle Nachrichten verarbeitet, die gesendet oder an alle Fenster der Klasse gesendet werden.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Fenster Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349663"
---
# <a name="window-procedures"></a>Fenster Prozeduren

Jedes Fenster verfügt über eine zugeordnete Fenster Prozedur – eine Funktion, die alle Nachrichten verarbeitet, die gesendet oder an alle Fenster der Klasse gesendet werden. Alle Aspekte der Darstellung und des Verhaltens eines Fensters hängen von der Reaktion der Fenster Prozedur auf diese Nachrichten ab.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                         | BESCHREIBUNG                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Fenster Verfahren](about-window-procedures.md)       | Erläutert Fenster Prozeduren. Jedes Fenster ist ein Member einer bestimmten Fenster Klasse. Die Fenster Klasse bestimmt die Standardfenster Prozedur, die von einem einzelnen Fenster zum Verarbeiten der Nachrichten verwendet wird.<br/> |
| [Verwenden von Window](using-window-procedures.md)       | Erläutert, wie die folgenden Aufgaben ausgeführt werden, die Fenster Prozeduren zugeordnet sind.<br/>                                                                                                                        |
| [Fenster Prozedur Referenz](window-procedure-reference.md) | Enthält die API-Referenz.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Functions



| Name                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Übergibt Nachrichten Informationen an die angegebene Fenster Prozedur. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Ruft die Standardfenster Prozedur auf, um die Standard Verarbeitung für alle Fenster Meldungen bereitzustellen, die von einer Anwendung nicht verarbeitet werden. Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird. [**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) wird mit denselben Parametern aufgerufen, die von der Fenster Prozedur empfangen werden. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Eine Anwendungs definierte Funktion, die an ein Fenster gesendete Nachrichten verarbeitet. Der **WndProc** -Typ definiert einen Zeiger auf diese Rückruffunktion. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/>                                                            |



 

 

 
