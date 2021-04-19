---
description: In diesem Abschnitt wird die mehrfache Dokument Schnittstelle erläutert, bei der es sich um eine Spezifikation handelt, die eine Benutzeroberfläche für Anwendungen definiert, mit denen der Benutzer gleichzeitig mit mehr als einem Dokument arbeiten kann.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Mehrere Dokument Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1898202aad6ec8d26f859bec2457124328c3a27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360555"
---
# <a name="multiple-document-interface"></a>Mehrere Dokument Schnittstellen

\[Viele neue und fortgeschrittene Benutzer sind schwierig zu erlernen, um MDI-Anwendungen zu verwenden. Daher sollten Sie andere Modelle für Ihre Benutzeroberfläche in Erwägung gezogen. Allerdings können Sie MDI für Anwendungen verwenden, die nicht problemlos in ein vorhandenes Modell passen.\]

Die Multiple Document Interface (MDI) ist eine Spezifikation, die eine Benutzeroberfläche für Anwendungen definiert, die es dem Benutzer ermöglichen, gleichzeitig mit mehreren Dokumenten zu arbeiten.

### <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                              | BESCHREIBUNG                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informationen zur Schnittstelle für mehrere Dokumente](about-the-multiple-document-interface.md) | Beschreibt die Schnittstelle für mehrere Dokumente.<br/>                                     |
| [Verwenden der Multiple Document-Schnittstelle](using-the-multiple-document-interface.md) | Erläutert das Ausführen von Aufgaben, die mit der multidokumentschnittstelle verknüpft sind.<br/> |
| [MDI-Referenz](multiple-document-interface-reference.md)                         | Enthält die API-Referenz.<br/>                                                    |



 

### <a name="mdi-functions"></a>MDI-Funktionen



| Name                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Anatemdiwindow"**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Erstellt ein untergeordnetes MDI-Fenster. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**"Debug"**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Stellt die Standard Verarbeitung für alle Fenster Meldungen bereit, die von der Fenster Prozedur eines MDI-Rahmen Fensters nicht verarbeitet werden. Alle Fenster Meldungen, die nicht explizit von der Fenster Prozedur verarbeitet werden, müssen an die [**defframeproc**](/windows/win32/api/winuser/nf-winuser-defframeproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übermittelt werden. <br/>                              |
| [**Defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Stellt die Standard Verarbeitung für jede Fenster Meldung bereit, die von der Fenster Prozedur eines untergeordneten MDI-Fensters nicht verarbeitet wird. Eine von der Fenster Prozedur nicht verarbeitete Fenster Nachricht muss an die [**defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden. <br/>                                             |
| [**Translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Verarbeitet Zugriffstasten-Tastatureingaben für Fenstermenü Befehle der untergeordneten MDI-Fenster, die dem angegebenen MDI-Client Fenster zugeordnet sind. Die Funktion übersetzt die Nachrichten WM [**\_ KeyUp**](/windows/desktop/inputdev/wm-keyup) und [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) in [**WM \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachrichten und sendet Sie an die entsprechenden untergeordneten MDI-Fenster. <br/> |



 

### <a name="mdi-messages"></a>MDI-Meldungen



| Name                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ mdiaktivierung**](wm-mdiactivate.md)       | Wird an ein MDI-Client Fenster gesendet, um das Client Fenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM- \_ mdicascade**](wm-mdicascade.md)         | Wird an ein MDI-Client Fenster gesendet, um alle untergeordneten Fenster in einem kaskadierenden Format anzuordnen. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM- \_ mdicreate**](wm-mdicreate.md)           | Wird an ein MDI-Client Fenster gesendet, um ein untergeordnetes MDI-Fenster zu erstellen. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM- \_ mdidestroy**](wm-mdidestroy.md)         | Wird an ein MDI-Client Fenster gesendet, um ein untergeordnetes MDI-Fenster zu schließen. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM- \_ mdigetactive**](wm-mdigetactive.md)     | Wird an ein MDI-Client Fenster gesendet, um das Handle für das aktive untergeordnete MDI-Fenster abzurufen. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM- \_ mdiiconarrange**](wm-mdiiconarrange.md) | Wird an ein MDI-Client Fenster gesendet, um alle minimierten untergeordneten MDI-Fenster anzuordnen. Untergeordnete Fenster, die nicht minimiert sind, sind nicht betroffen. <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM- \_ mdimaximierung**](wm-mdimaximize.md)       | Wird an ein MDI-Client Fenster gesendet, um ein untergeordnetes MDI-Fenster zu maximieren. Das System ändert die Größe des untergeordneten Fensters, damit der Client Bereich das Client Fenster ausfüllen muss. Das System platziert das Fenstermenü Symbol des untergeordneten Fensters an der rechten Position der Menüleiste des Frame Fensters und platziert das Wiederherstellungs Symbol des untergeordneten Fensters an der äußersten linken Position. Das System fügt den Text der Titelleiste des untergeordneten Fensters auch an die des Frame Fensters an. <br/> |
| [**WM- \_ mdinext**](wm-mdinext.md)               | Wird an ein MDI-Client Fenster gesendet, um das nächste oder vorherige untergeordnete Fenster zu aktivieren. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM- \_ mumgeleitet-freshmenu**](wm-mdirefreshmenu.md) | Wird an ein MDI-Client Fenster gesendet, um das Fenstermenü des MDI-Rahmen Fensters zu aktualisieren. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM- \_ mumgeleitet-Speicher**](wm-mdirestore.md)         | Wird an ein MDI-Client Fenster gesendet, um ein untergeordnetes MDI-Fenster von maximierter oder minimierter Größe wiederherzustellen. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM- \_ mdisetmenu**](wm-mdisetmenu.md)         | Wird an ein MDI-Client Fenster gesendet, um das gesamte Menü eines MDI-Rahmen Fensters zu ersetzen, um das Fenstermenü des Rahmen Fensters zu ersetzen, oder beides. <br/>                                                                                                                                                                                                                                                                                           |
| [**WM- \_ mditile**](wm-mditile.md)               | Wird an ein MDI-Client Fenster gesendet, um alle untergeordneten MDI-Fenster in einem Kachel Format anzuordnen. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>MDI-Strukturen



| Name                                       | BESCHREIBUNG                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Enthält Informationen über die Klasse, den Titel, den Besitzer, den Speicherort und die Größe eines untergeordneten MDI-Fensters. <br/> |



 

 

