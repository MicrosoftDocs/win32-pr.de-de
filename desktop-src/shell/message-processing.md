---
description: Die CPlApplet-Rückruffunktion verarbeitet alle Nachrichten, die an ein Systemsteuerung-Element gesendet werden, Windows. Nachrichten, die an die Funktion gesendet werden, befinden sich in einer bestimmten Reihenfolge. Mit demselben Token erfordert das .cpl, dass die Nachrichten auf eine bestimmte Weise verarbeitet werden.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Systemsteuerung Nachrichtenverarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e697c603b69790d17c4d6771666a1111fa6f968eb97a30256696921f133530d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719951"
---
# <a name="control-panel-message-processing"></a>Systemsteuerung Nachrichtenverarbeitung

Die [**CPlApplet-Rückruffunktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) verarbeitet alle Nachrichten, die an ein Systemsteuerung-Element gesendet werden, Windows. Nachrichten, die an die Funktion gesendet werden, befinden sich in einer bestimmten Reihenfolge. Mit demselben Token erfordert das .cpl, dass die Nachrichten auf eine bestimmte Weise verarbeitet werden.

Zunächst empfängt die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) die CPL-INIT-Nachricht, wenn Windows zum ersten Mal das Systemsteuerung \_ lädt. Die Funktion sollte alle Initialisierungen durchführen, z. B. das Zuweisen von Arbeitsspeicher, und einen Nicht-Null-Rückgabe ungleich 0 (null) zurückgeben. Wenn **CPlApplet** die Initialisierung nicht abschließen kann, muss es 0 (null) zurückgeben, Windows die Kommunikation zu beenden und die DLL frei zu geben.

Wenn die CPL-INIT-Nachricht erfolgreich war, sendet Windows \_ CPL \_ GETCOUNT-Nachricht. Die Funktion muss dann die Anzahl der Systemsteuerung elemente zurückgeben, die von der .dll werden.

Die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) empfängt dann eine CPL-NACHRICHT UND eine \_ CPL NEWINQUIRE-Nachricht für jedes Systemsteuerung-Element, das von der .dll \_ wird. Die Funktion füllt eine [**CPLINFO-**](/windows/win32/api/cpl/ns-cpl-cplinfo) oder [**NEWCPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) mit Informationen zu Ihrem Element auf, z. B. name, icon und eine beschreibende Zeichenfolge. Die meisten Anwendungen sollten die \_ CPL-Nachricht ZU 100000000000 CPL \_ NEWINQUIRE-Nachrichten verarbeiten und ignorieren. Die CPL-NACHRICHT FÜR DIE 1000-Nachricht stellt Informationen in einer Form zur Verfügung, Windows zwischengespeichert werden kann, was zu einer \_ deutlich besseren Leistung führt. Die CPL NEWINQUIRE-Nachricht wird nur verwendet, wenn Sie das Symbol Ihres Elements oder die Anzeigezeichenfolgen basierend auf dem Zustand des \_ Computers ändern müssen. Systemsteuerung Elemente, die CPL NEWINQUIRE verwenden, kann die Suche im Startmenü in Windows Vista nicht gefunden werden, da sie auf der \_ Zwischenspeicherung  basiert.

Die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) empfängt als Nächstes eine CPL-DBLCLK-Nachricht als Benachrichtigung, dass der Benutzer das Symbol ausgewählt hat, das das Systemsteuerung \_ darstellt. Die Funktion kann diese Nachricht mehrmals empfangen. Die Nachricht enthält den Elementbezeichner und den **lpData-Zeiger,** die in der [**CPLINFO-**](/windows/win32/api/cpl/ns-cpl-cplinfo) oder [**NEWCPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) im Aufruf von [**CPL \_ BZW.**](cpl-inquire.md) [**\_ NEWINQUIRE**](cpl-newinquire.md)zurückgegeben werden. Die Funktion sollte das entsprechende Dialogfeld anzeigen und nachfolgende Benutzereingaben verarbeiten.

Neben CPL DBLCLK kann die \_ CPL STARTWPARMS-Nachricht gesendet werden, wenn ein Systemsteuerung-Element mit Eingabeparametern aufgerufen wird, z. B. über eine Eingabeaufforderung oder ein anderes \_ Programm. Die Meldung enthält den Elementbezeichner zusammen mit der zusätzlichen Parameterzeichenfolge.

Bevor die steuernde Anwendung beendet wird, empfängt [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) die CPL STOP-Nachricht einmal für jedes Systemsteuerung element, das von der .dll \_ wird. Die Nachricht enthält den Bezeichner für das Systemsteuerung-Element und den **lpData-Zeiger,** der in der [**CPLINFO-**](/windows/win32/api/cpl/ns-cpl-cplinfo) oder [**NEWCPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) im Aufruf von [**CPL \_ BZW.**](cpl-inquire.md) [**\_ NEWINQUIRE**](cpl-newinquire.md)zurückgegeben wird. Die Funktion sollte jeglichen Arbeitsspeicher, den sie dem angegebenen Dialogfeld zugeordnet hat, frei geben.

Nach der letzten CPL \_ STOP-Nachricht [**empfängt CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) eine CPL \_ EXIT-Nachricht. Die Funktion sollte den verbleibenden zugeordneten Arbeitsspeicher frei geben und die Registrierung aller privaten Fensterklassen aufheben, die sie möglicherweise registriert hat. Unmittelbar nachdem die Funktion von dieser Nachricht zurückgegeben wurde, gibt Windows das Systemsteuerung durch Aufrufen der [**FreeLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Elemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Ausführen Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
