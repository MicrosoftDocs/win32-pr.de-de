---
title: Cursor
description: In diesem Abschnitt werden Cursor erläutert, bei denen es sich um kleine Bilder handelt, deren Position auf dem Bildschirm durch ein zeigendes Gerät gesteuert wird, z. B. eine Maus, ein Stift oder ein Trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- resources,cursors
- cursors,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7be5b8e213dd1911d2227a3dce4b61078ab1a22711d4e765525c7fbd5bd08d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712610"
---
# <a name="cursors"></a>Cursor

Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm durch ein zeigendes Gerät gesteuert wird, z. B. eine Maus, ein Stift oder ein Trackball. Im weiteren Verlauf dieser Übersicht bezieht sich der Begriff Maus auf ein beliebiges zeigendes Gerät.

Wenn der Benutzer die Maus bewegt, verschiebt das System den Cursor entsprechend. Mit den Cursorfunktionen können Anwendungen Cursor erstellen, laden, anzeigen, animieren, verschieben, beschränken und zerstören.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                     | Beschreibung                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Informationen zu Cursorn](about-cursors.md)       | Erläutert die Standardcursor.<br/>                    |
| [Verwenden von Cursors](using-cursors.md)       | Erläutert, wie Aufgaben im Zusammenhang mit Cursorn ausgeführt werden.<br/> |
| [Cursorverweis](cursor-reference.md) | Enthält den API-Verweis.<br/>                        |



 

### <a name="cursor-functions"></a>Cursorfunktionen



| Name                                                 | Beschreibung                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Beschränkt den Cursor auf einen rechteckigen Bereich auf dem Bildschirm. Wenn sich eine nachfolgende Cursorposition (festgelegt durch die [**SetCursorPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) oder die Maus) außerhalb des Rechtecks befindet, passt das System die Position automatisch an, um den Cursor im rechteckigen Bereich zu halten. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Kopiert den angegebenen Cursor. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Erstellt einen Cursor mit der angegebenen Größe, den angegebenen Bitmustern und dem angegebenen Hotspots. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Zerstört einen Cursor und gibt den vom Cursor belegten Arbeitsspeicher frei. Verwenden Sie diese Funktion nicht, um einen freigegebenen Cursor zu zerstören.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Ruft die Bildschirmkoordinaten des rechteckigen Bereichs ab, auf den der Cursor beschränkt ist. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Ruft ein Handle für den aktuellen Cursor ab. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Ruft Informationen zum globalen Cursor ab.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Ruft die Position des Cursors in Bildschirmkoordinaten ab.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Ruft die Position des Cursors in physischen Koordinaten ab.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Lädt die angegebene Cursorressource aus der ausführbaren Datei (.EXE), die einer Anwendungsinstanz zugeordnet ist.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Erstellt einen Cursor auf Der Grundlage von Daten, die in einer Datei enthalten sind. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Legt die Cursorform fest. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Verschiebt den Cursor zu den angegebenen Bildschirmkoordinaten. Wenn sich die neuen Koordinaten nicht innerhalb des Bildschirmrechtecks befinden, das durch den letzten [**ClipCursor-Funktionsaufruf**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) festgelegt wurde, passt das System die Koordinaten automatisch an, sodass der Cursor innerhalb des Rechtecks bleibt. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Legt die Position des Cursors in physischen Koordinaten fest.<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Ermöglicht einer Anwendung das Anpassen der Systemcursor. Er ersetzt den Inhalt des vom *id-Parameter* angegebenen Systemcursors durch den Inhalt des Cursors, der durch den *hcur-Parameter* angegeben wird, und zerstört dann *hcur.* <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Zeigt den Cursor an oder blendet den Cursor aus. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Cursorbenachrichtigungen



| Name                                  | Beschreibung                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ SETCURSOR**](wm-setcursor.md) | Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Mauseingabe nicht erfasst wird. <br/> |



 

### <a name="cursor-structures"></a>Cursorstrukturen



| Name                             | Beschreibung                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Enthält globale Cursorinformationen.<br/> |



 

 

 





