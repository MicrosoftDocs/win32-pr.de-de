---
description: Ein Fenster oder ein Menü, das sich auf mehr als einem Monitor befindet, bewirkt eine visuelle Unterbrechung für einen Viewer. Um dieses Problem zu minimieren, zeigt das Systemmenüs und neue und maximierte Fenster auf einem Monitor an. In der folgenden Tabelle wird gezeigt, wie der Monitor ausgewählt wird.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Positionieren von Objekten auf mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77149291737482fa0f3e7fe19ee4f350ee6521d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978392"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Positionieren von Objekten auf mehreren Anzeige Monitoren

Ein Fenster oder ein Menü, das sich auf mehr als einem Monitor befindet, bewirkt eine visuelle Unterbrechung für einen Viewer. Um dieses Problem zu minimieren, zeigt das Systemmenüs und neue und maximierte Fenster auf einem Monitor an. In der folgenden Tabelle wird gezeigt, wie der Monitor ausgewählt wird.



| Object         | Standort                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fenster         | In " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(ex)" wird ein Fenster auf dem Monitor angezeigt, das den größten Teil des Fensters enthält. Maximiert auf dem Monitor, der den größten Teil des Fensters enthält, bevor er minimiert wurde.<br/> Die Tastenkombination Alt + Tab zeigt ein Fenster auf dem Monitor an, das über das derzeit aktive Fenster verfügt.<br/>                                                                                                                                          |
| eigenes Fenster   | auf demselben Monitor wie der Besitzer.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Untermenü        | Wird auf dem Monitor angezeigt, der den größten Teil des entsprechenden Menü Elements enthält.                                                                                                                                                                                                                                                                                                                                                                                                          |
| Kontextmenü   | Wird auf dem Monitor angezeigt, auf dem der Rechte Klick aufgetreten ist.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Dropdownliste | Wird auf dem Monitor angezeigt, der das Rechteck des Kombinations Felds enthält.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Dialogfeld     | Wird auf dem Monitor des Fensters angezeigt, in dem es enthalten ist. Wenn er mit dem DS- \_ centermouse-Stil definiert ist, wird er mit der Maus auf dem Monitor angezeigt.<br/> Wenn Sie über keinen Besitzer und das aktive Fenster und das Dialogfeld in derselben Anwendung vorhanden sind, wird das Dialogfeld auf dem Monitor des derzeit aktiven Fensters angezeigt.<br/> Wenn das Dialogfeld keinen Besitzer hat und sich das aktive Fenster nicht in derselben Anwendung wie das Dialogfeld befindet, wird das Dialogfeld auf dem primären Monitor angezeigt.<br/> |
| Meldungs Feld    | Wird auf dem Monitor des Fensters angezeigt, in dem es enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Wenn ein Fenster zwei Monitore überschreitet und einer der Monitore neu positioniert wird, positioniert das System das Fenster auf dem Monitor, das den größten Teil des ursprünglichen Fensters enthält.

Eine Anwendung muss in der Regel auch-Objekte positionieren. Beispielsweise muss ein Fenster möglicherweise auf demselben Monitor wie ein anderes Fenster erstellt werden.

**So positionieren Sie ein Objekt auf einem System mit mehreren Monitoren**

1.  Bestimmen Sie den entsprechenden Monitor.
2.  Hiermit werden die Koordinaten für den Monitor angezeigt.
3.  Positionieren Sie das Objekt mit den Koordinaten.

In der Regel positionieren Sie ein Objekt entweder auf dem primären Monitor oder auf einem Monitor, auf dem bereits ein Objekt vorhanden ist. Verwenden Sie zum Identifizieren des Monitors für einen bestimmten Punkt, ein bestimmtes Rechteck oder ein bestimmtes Fenster [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**monitorfromrect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)und [**monitorfromwindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Um die Koordinaten für den Monitor zu erhalten, verwenden Sie [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), das sowohl den Arbeitsbereich als auch das gesamte Monitor Rechteck bereitstellt. Beachten Sie, dass SM \_ cxscreen und SM \_ cyscreen immer auf den primären Monitor verweisen, nicht notwendigerweise auf den Monitor, mit dem die Anwendung angezeigt wird. Vermeiden Sie außerdem SM \_ xxvirtualscreen, da dadurch das Fenster auf dem virtuellen Bildschirm, nicht auf einem Monitor zentriert wird.

Um die Dialogfelder im Arbeitsbereich eines Fensters zu zentrieren, verwenden Sie den DS \_ Center-Stil. Um das Dialogfeld mit einem Anwendungsfenster zu zentrieren, verwenden Sie [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Menüs und Dialogfelder werden von Windows automatisch auf einen Monitor beschränkt. Es kann jedoch ein Problem mit benutzerdefinierten Menüs, benutzerdefinierten Dropdown Feldern, benutzerdefinierten Tool Paletten und der gespeicherten Anwendungs Position auftreten.

Ein Beispiel zum ordnungsgemäßen Positionieren von Objekten finden Sie unter [Positionieren von Objekten in einer mehrfach Anzeige Einrichtung](positioning-objects-on-a-multiple-display-setup.md).

Wenn Sie \_ \_ den Speicherort einer Anwendungs Desktop-Symbolleiste (auch *appbar* genannt) mithilfe von SM cxscreen und SM cyscreen ermitteln, wird die appbar auf den primären Monitor beschränkt. Damit eine appbar an einem beliebigen Rand eines beliebigen Monitors angezeigt werden kann, verwenden Sie die geeigneten Systemmetriken, um die Ränder der Monitore zu berechnen. Verwenden Sie außerdem die **get \_ X \_ LPARAM** -und **get \_ Y \_ LPARAM** -Makros, um die Koordinaten zu extrahieren. andernfalls ist das Vorzeichen der Koordinaten möglicherweise falsch. Diese Makros sind in WINDOWSX. h enthalten.

Die Größe eines voll Bildfensters muss geändert werden, wenn es sich zwischen Monitoren mit unterschiedlichen Auflösungen bewegt. Zu diesem Zweck muss die Anwendung das Fenster, auf dem Sie sich befindet, mithilfe von " [**monitorfromwindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) " oder " [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) " überprüfen und dann " [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) " verwenden, um die Größe des Monitors zu erhalten. Als Alternative können Sie den **Hmonitor** aus der DirectX-Funktion **directdrawenenerateex** verwenden. Verwenden Sie dann [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) , um das Fenster zu positionieren und die Größe des Monitors abzudecken.

Ein maximiertes Fenster deckt nicht eine Taskleiste mit der Eigenschaft "Always on-Top" ab. Allerdings deckt ein voll Bildfenster die Taskleiste ab, z. b. in Microsoft PowerPoint-Folien anzeigen und-spielen.

Um die Position eines Fensters zu speichern und später wiederherzustellen, verwenden Sie die Funktionen [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) und [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) , wenn eine Anwendung beendet wird. Überprüfen Sie jedoch, ob die Position noch gültig ist, bevor Sie Sie verwenden, da der Monitor möglicherweise verschoben oder aus dem System entfernt wurde. Die Anwendung zeigt das Fenster auf dem primären Monitor an, wenn der **Hmonitor** eines Fensters ungültig ist.

Das System versucht, eine Anwendung auf dem Monitor zu starten, die seine Verknüpfung enthält. Eine Möglichkeit, eine Anwendung zu positionieren, besteht darin, die Verknüpfung auf einem gewünschten Monitor zu haben.

Wenn Sie [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) verwenden, geben Sie ein *HWND* an, damit das System alle neuen Fenster auf demselben Monitor wie die aufrufende Anwendung öffnet.

Beachten Sie, dass die Werte für die [**minmaxinfo**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) -Struktur für ein System mit mehreren Monitoren leicht geändert werden.

 

 
