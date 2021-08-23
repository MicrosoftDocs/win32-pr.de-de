---
description: Ein Fenster oder Menü, das sich auf mehreren Monitoren befindet, führt zu visuellen Unterbrechungen für einen Viewer. Um dieses Problem zu minimieren, zeigt das System Menüs und neue und maximierte Fenster auf einem Monitor an. Die folgende Tabelle zeigt, wie der Monitor ausgewählt wird.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Positionieren von Objekten auf mehreren Anzeigemonitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6581fbed64b6a8ac83e29410e9758c6dea7b2d145958c57fa187abf34985c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602730"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Positionieren von Objekten auf mehreren Anzeigemonitoren

Ein Fenster oder Menü, das sich auf mehreren Monitoren befindet, führt zu visuellen Unterbrechungen für einen Viewer. Um dieses Problem zu minimieren, zeigt das System Menüs und neue und maximierte Fenster auf einem Monitor an. Die folgende Tabelle zeigt, wie der Monitor ausgewählt wird.



| Object         | Standort                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fenster         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(Ex) zeigt ein Fenster auf dem Monitor an, das den größten Teil des Fensters enthält. Maximiert auf dem Monitor, der den größten Teil des Fensters enthält, bevor es minimiert wurde.<br/> Die Tastenkombination ALT/TAB zeigt ein Fenster auf dem Monitor an, das über das derzeit aktive Fenster verfügt.<br/>                                                                                                                                          |
| Eigenes Fenster   | auf demselben Monitor wie der Besitzer.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Untermenü        | Wird auf dem Monitor angezeigt, der den größten Teil des entsprechenden Menüelements enthält.                                                                                                                                                                                                                                                                                                                                                                                                          |
| Kontextmenü   | Wird auf dem Monitor angezeigt, auf dem der Rechtsklick aufgetreten ist.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Dropdownliste | Wird auf dem Monitor angezeigt, der das Rechteck des Kombinationsfelds enthält.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Dialogfeld     | Wird auf dem Monitor des Fensters angezeigt, das es besitzt. Wenn sie mit dem DS \_ CENTERMOUSE-Stil definiert ist, wird sie mit der Maus auf dem Monitor angezeigt.<br/> Wenn kein Besitzer vorhanden ist und sich das aktive Fenster und das Dialogfeld in derselben Anwendung befinden, wird das Dialogfeld auf dem Monitor des derzeit aktiven Fensters angezeigt.<br/> Wenn das Dialogfeld keinen Besitzer hat und sich das aktive Fenster nicht in derselben Anwendung wie das Dialogfeld befindet, wird das Dialogfeld auf dem primären Monitor angezeigt.<br/> |
| Meldungsfeld    | Wird auf dem Monitor des Fensters angezeigt, das es besitzt.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Wenn ein Fenster zwei Monitore umspannt und einer der Monitore neu positioniert wird, positioniert das System das Fenster auf dem Monitor, der den größten Teil des ursprünglichen Fensters enthält.

Eine Anwendung muss in der Regel auch Objekte positionieren. Beispielsweise muss ein Fenster möglicherweise auf dem gleichen Monitor wie ein anderes Fenster erstellt werden.

**So positionieren Sie ein Objekt auf einem System mit mehreren Monitoren**

1.  Bestimmen Sie den geeigneten Monitor.
2.  Abrufen der Koordinaten zum Monitor.
3.  Positionieren Sie das Objekt mithilfe der Koordinaten.

In der Regel positionieren Sie ein Objekt entweder auf dem primären Monitor oder auf einem Monitor, auf dem bereits ein -Objekt vorhanden ist. Verwenden Sie [**MonitorFromPoint,**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)und [**MonitorFromWindow,**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)um den Monitor für einen bestimmten Punkt, ein bestimmtes Rechteck oder Fenster zu identifizieren.

Um die Koordinaten für den Monitor abzurufen, verwenden [**Sie GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), das sowohl den Arbeitsbereich als auch das gesamte Monitorrechteck bereitstellt. Beachten Sie, dass SM \_ CXSCREEN und SM \_ CYSCREEN immer auf den primären Monitor verweisen, nicht unbedingt auf den Monitor, auf dem Ihre Anwendung angezeigt wird. Vermeiden Sie außerdem SM \_ xxVIRTUALSCREEN, da dadurch ihr Fenster auf dem virtuellen Bildschirm und nicht auf einem Monitor zentrieren wird.

Verwenden Sie den DS CENTER-Stil, um Dialogfelder im Arbeitsbereich eines Fensters zu \_ zentriert. Verwenden [**Sie GetWindowRect,**](/windows/win32/api/winuser/nf-winuser-getwindowrect)um das Dialogfeld auf ein Anwendungsfenster zu zentrieren. Windows schränkt Menüs und Dialogfelder automatisch auf einen Monitor ein. Es kann jedoch ein Problem mit benutzerdefinierten Menüs, benutzerdefinierten Dropdownfeldern, benutzerdefinierten Toolpaletten und der gespeicherten Anwendungsposition geben.

Ein Beispiel dafür, wie Objekte ordnungsgemäß positioniert werden, finden Sie unter Positionieren von Objekten in einem Setup für [mehrere Anzeige.](positioning-objects-on-a-multiple-display-setup.md)

Die Verwendung von SM \_ CXSCREEN und SM \_ CYSCREEN zum Bestimmen des Speicherorts einer Anwendungsdesktopsymbolleiste (auch als *AppBar* bezeichnet) schränkt die Appbar auf den primären Monitor ein. Damit sich eine App-Leiste an einem beliebigen Rand eines Beliebigen Monitors aufsetzen kann, verwenden Sie die entsprechenden Systemmetriken, um die Ränder der Monitore zu berechnen. Verwenden Sie außerdem die Makros **GET \_ X \_ LPARAM** und **GET \_ Y \_ LPARAM,** um die Koordinaten zu extrahieren. Andernfalls kann das Vorzeichen der Koordinaten falsch sein. Diese Makros sind in Windowsx.h enthalten.

Die Größe eines Vollbildfensters muss sich ändern, wenn es zwischen Monitoren mit unterschiedlichen Auflösungen verschoben wird. Zu diesem Zwecke muss die Anwendung mit [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) oder [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) überprüfen, in welchem Fenster sie sich befindet, und dann [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) verwenden, um die Größe des Monitors abzurufen. Alternativ können Sie **HMONITOR** aus der DirectX **DirectDrawEnumerateEx-Funktion** verwenden. Verwenden Sie dann [**SetWindowPos,**](/windows/win32/api/winuser/nf-winuser-setwindowpos) um das Fenster so zu positionieren und zu dimensionieren, dass es den Monitor abdeckt.

Ein maximiertes Fenster deckt keine Taskleiste ab, die über die Eigenschaft "Always On Top" verfügt. Ein Vollbildfenster deckt jedoch die Taskleiste ab, z. B. in Microsoft PowerPoint Bildschirmpräsentationen und Spiele.

Verwenden Sie die Funktionen [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) und [**SetWindowPlacement,**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) um die Position eines Fensters zu speichern und später wiederherzustellen, wenn eine Anwendung beendet wird. Überprüfen Sie jedoch, ob die Position noch gültig ist, bevor Sie sie verwenden, da der Monitor möglicherweise verschoben oder aus dem System entfernt wurde. Die Anwendung zeigt das Fenster auf dem primären Monitor an, wenn **HMONITOR** eines Fensters ungültig ist.

Das System versucht, eine Anwendung auf dem Monitor zu starten, die die zugehörige Verknüpfung enthält. Eine Möglichkeit, eine Anwendung zu positionieren, besteht also darin, ihre Verknüpfung auf einem gewünschten Monitor zu verwenden.

Wenn Sie [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) verwenden, geben Sie einen *hWnd* an, damit das System alle neuen Fenster auf demselben Monitor wie die aufrufende Anwendung öffnet.

Beachten Sie, dass die Werte für die [**MINMAXINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) für ein System mit mehreren Monitoren geringfügig geändert werden.

 

 
