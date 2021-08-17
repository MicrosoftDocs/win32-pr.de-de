---
description: In diesem Abschnitt wird die Schnittstelle für mehrere Dokumente erläutert. Dabei handelt es sich um eine Spezifikation, die eine Benutzeroberfläche für Anwendungen definiert, die es dem Benutzer ermöglichen, gleichzeitig mit mehreren Dokumenten zu arbeiten.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Mehrere Dokumentschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d579d1075f85fae7cd2d4ca6e63e1b8196c6d2118e33102cd511a1e468a18ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705359"
---
# <a name="multiple-document-interface"></a>Mehrere Dokumentschnittstellen

\[Viele neue und fortgeschrittene Benutzer finden es schwierig, die Verwendung von MDI-Anwendungen zu erlernen. Daher sollten Sie andere Modelle für Ihre Benutzeroberfläche in Betracht ziehen. Sie können MDI jedoch für Anwendungen verwenden, die nicht einfach in ein vorhandenes Modell passen.\]

Die MDI (Multiple Document Interface) ist eine Spezifikation, die eine Benutzeroberfläche für Anwendungen definiert, die es dem Benutzer ermöglichen, gleichzeitig mit mehreren Dokumenten zu arbeiten.

### <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                              | BESCHREIBUNG                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informationen zur Schnittstelle für mehrere Dokumente](about-the-multiple-document-interface.md) | Beschreibt die Schnittstelle für mehrere Dokumente.<br/>                                     |
| [Verwenden der Schnittstelle für mehrere Dokumente](using-the-multiple-document-interface.md) | Erläutert das Ausführen von Aufgaben, die der Schnittstelle für mehrere Dokumente zugeordnet sind.<br/> |
| [MDI-Referenz](multiple-document-interface-reference.md)                         | Enthält die API-Referenz.<br/>                                                    |



 

### <a name="mdi-functions"></a>MDI-Funktionen



| Name                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Erstellt ein untergeordnetes MDI-Fenster. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Stellt Die Standardverarbeitung für alle Fenstermeldungen, die von der Fensterprozedur eines MDI-Rahmenfensters nicht verarbeitet werden, sicher. Alle Fenstermeldungen, die nicht explizit von der Fensterprozedur verarbeitet werden, müssen an die [**DefFrameProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defframeproca) übergeben werden, nicht an die [**DefWindowProc-Funktion.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Stellt die Standardverarbeitung für alle Fensternachrichten zur Sicher, die die Fensterprozedur eines untergeordneten MDI-Fensters nicht verarbeitet. Eine Fenstermeldung, die nicht von der Fensterprozedur verarbeitet wird, muss an die [**DefMDIChildProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) und nicht an die [**DefWindowProc-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) werden. <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Verarbeitet Tastenkombinationen für Fenstermenübefehle der untergeordneten MDI-Fenster, die dem angegebenen MDI-Clientfenster zugeordnet sind. Die Funktion übersetzt [**WM \_ KEYUP-**](/windows/desktop/inputdev/wm-keyup) und [**WM \_ KEYDOWN-Nachrichten**](/windows/desktop/inputdev/wm-keydown) in [**WM \_ SYSCOMMAND-Nachrichten**](/windows/desktop/menurc/wm-syscommand) und sendet sie an die entsprechenden untergeordneten MDI-Fenster. <br/> |



 

### <a name="mdi-messages"></a>MDI-Nachrichten



| Name                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ MDIACTIVATE**](wm-mdiactivate.md)       | Wird an ein MDI-Clientfenster gesendet, um das Clientfenster anweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ MDICASCADE**](wm-mdicascade.md)         | Wird an ein MDI-Clientfenster gesendet, um alle untergeordneten Fenster in einem kaskadierten Format zu anordnen. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ MDICREATE**](wm-mdicreate.md)           | Wird an ein MDI-Clientfenster gesendet, um ein untergeordnetes MDI-Fenster zu erstellen. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIDESTROY**](wm-mdidestroy.md)         | Wird an ein MDI-Clientfenster gesendet, um ein untergeordnetes MDI-Fenster zu schließen. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)     | Wird an ein MDI-Clientfenster gesendet, um das Handle für das aktive untergeordnete MDI-Fenster abzurufen. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) | Wird an ein MDI-Clientfenster gesendet, um alle minimierten untergeordneten MDI-Fenster zu anordnen. Dies wirkt sich nicht auf untergeordnete Fenster aus, die nicht minimiert werden. <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)       | Wird an ein MDI-Clientfenster gesendet, um ein untergeordnetes MDI-Fenster zu maximieren. Das System wird die Größe des untergeordneten Fensters so geändert, dass sein Clientbereich das Clientfenster ausfüllt. Das System platziert das Fenstermenüsymbol des untergeordneten Fensters an der rechten Position der Menüleiste des Rahmenfensters und platziert das Wiederherstellungssymbol des untergeordneten Fensters ganz links. Das System fügt auch den Titelleistentext des untergeordneten Fensters an den Text des Rahmenfensters an. <br/> |
| [**WM \_ MDINEXT**](wm-mdinext.md)               | Wird an ein MDI-Clientfenster gesendet, um das nächste oder vorherige untergeordnete Fenster zu aktivieren. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDSTELLUNGFRESHMENU**](wm-mdirefreshmenu.md) | Wird an ein MDI-Clientfenster gesendet, um das Fenstermenü des MDI-Rahmenfensters zu aktualisieren. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ MDUNGSTORE**](wm-mdirestore.md)         | Wird an ein MDI-Clientfenster gesendet, um ein untergeordnetes MDI-Fenster aus maximierten oder minimierten Größen wiederherzustellen. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ MDISETMENU**](wm-mdisetmenu.md)         | Wird an ein MDI-Clientfenster gesendet, um das gesamte Menü eines MDI-Rahmenfensters zu ersetzen, um das Fenstermenü des Rahmenfensters oder beides zu ersetzen. <br/>                                                                                                                                                                                                                                                                                           |
| [**WM \_ MDITILE**](wm-mditile.md)               | Wird an ein MDI-Clientfenster gesendet, um alle untergeordneten MDI-Fenster in einem Kachelformat zu anordnen. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>MDI-Strukturen



| Name                                       | BESCHREIBUNG                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Enthält Informationen zu Klasse, Titel, Besitzer, Speicherort und Größe eines untergeordneten MDI-Fensters. <br/> |



 

 

