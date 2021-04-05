---
title: Cursor
description: In diesem Abschnitt werden Cursor erläutert, bei denen es sich um kleine Bilder handelt, deren Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. Maus, Stift oder Trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- Ressourcen, Cursor
- Cursor, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037043"
---
# <a name="cursors"></a>Cursor

Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. mit einer Maus, einem Stift oder einem Trackball. Im restlichen Teil dieser Übersicht bezieht sich der Begriff Maus auf jedes Zeigegerät.

Wenn der Benutzer die Maus bewegt, verschiebt das System den Cursor entsprechend. Die Cursor Funktionen ermöglichen Anwendungen das Erstellen, laden, anzeigen, animieren, verschieben, einschränken und zerstören von Cursorn.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                     | BESCHREIBUNG                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Informationen über Cursor](about-cursors.md)       | Erläutert die standardcursorn.<br/>                    |
| [Verwenden von Cursors](using-cursors.md)       | Erläutert das Ausführen von Aufgaben im Zusammenhang mit Cursorn.<br/> |
| [Cursor Verweis](cursor-reference.md) | Enthält die API-Referenz.<br/>                        |



 

### <a name="cursor-functions"></a>Cursorfunktionen



| Name                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clipcursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Schränkt den Cursor auf einen rechteckigen Bereich auf dem Bildschirm ein. Wenn sich eine nachfolgende Cursorposition (die durch die [**setcursorpos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) -Funktion oder die Maus festgelegt ist) außerhalb des Rechtecks befindet, passt das System automatisch die Position an, um den Cursor innerhalb des rechteckigen Bereichs zu halten. <br/> |
| [**Copycursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Kopiert den angegebenen Cursor. <br/>                                                                                                                                                                                                                                                               |
| [**"Kreatecursor"**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Erstellt einen Cursor mit der angegebenen Größe, den angegebenen Bitmustern und dem angegebenen Hotspot. <br/>                                                                                                                                                                                                                    |
| [**Destroycursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Zerstört einen Cursor und gibt den vom Cursor belegten Arbeitsspeicher frei. Verwenden Sie diese Funktion nicht zum Zerstören eines freigegebenen Cursors.<br/>                                                                                                                                                                            |
| [**Getclipcursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Ruft die Bildschirm Koordinaten des rechteckigen Bereichs ab, in den sich der Cursor befindet. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Ruft ein Handle für den aktuellen Cursor ab. <br/>                                                                                                                                                                                                                                                  |
| [**Getcurrsorinfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Ruft Informationen zum globalen Cursor ab.<br/>                                                                                                                                                                                                                                              |
| [**Getcurrsorpos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Ruft die Position des Cursors in Bildschirm Koordinaten ab.<br/>                                                                                                                                                                                                                                     |
| [**Getphysicalcurrsorpos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Ruft die Position des Cursors in physischen Koordinaten ab.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Lädt die angegebene Cursor Ressource aus der ausführbaren Datei (. EXE-Datei, die einer Anwendungs Instanz zugeordnet ist.<br/>                                                                                                                                                                                |
| [**LoadCursor FromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Erstellt einen Cursor auf der Grundlage von Daten, die in einer Datei enthalten sind. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Legt die Cursor Form fest. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Verschiebt den Cursor an die angegebenen Bildschirm Koordinaten. Wenn sich die neuen Koordinaten nicht innerhalb des durch den letzten [**clipcursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) -Funktions Aufrufes festgelegten Bildschirm Rechtecks befinden, passt das System die Koordinaten automatisch so an, dass der Cursor innerhalb des Rechtecks bleibt. <br/>    |
| [**Setphysicalcurrsorpos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Legt die Position des Cursors in physischen Koordinaten fest.<br/>                                                                                                                                                                                                                                    |
| [**Setsystemcursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Ermöglicht einer Anwendung das Anpassen der systemcursorn. Er ersetzt den Inhalt des vom *ID* -Parameter angegebenen System Cursors mit dem Inhalt des durch den *hcur* -Parameter angegebenen Cursors und zerstört dann *hcur*. <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Zeigt den Cursor an oder blendet ihn aus. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Cursor Benachrichtigungen



| Name                                  | BESCHREIBUNG                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ SetCursor**](wm-setcursor.md) | Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Maus Eingaben nicht aufgezeichnet werden. <br/> |



 

### <a name="cursor-structures"></a>Cursor Strukturen



| Name                             | BESCHREIBUNG                                    |
|----------------------------------|------------------------------------------------|
| [**Cursor Info**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Enthält globale Cursor Informationen.<br/> |



 

 

 





