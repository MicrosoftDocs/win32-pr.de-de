---
description: Die CPlApplet-Rückruffunktion verarbeitet alle Nachrichten, die von Windows an ein System Steuerungselement gesendet werden. An die Funktion gesendete Nachrichten sind in einer bestimmten Reihenfolge angeordnet. Das CPL-Element erfordert, dass die Nachrichten auf eine bestimmte Weise verarbeitet werden.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Nachrichtenverarbeitung in der Systemsteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b43c6e265030279a6644547f41e3630208325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960291"
---
# <a name="control-panel-message-processing"></a>Nachrichtenverarbeitung in der Systemsteuerung

Die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Rückruffunktion verarbeitet alle Nachrichten, die von Windows an ein System Steuerungselement gesendet werden. An die Funktion gesendete Nachrichten sind in einer bestimmten Reihenfolge angeordnet. Das CPL-Element erfordert, dass die Nachrichten auf eine bestimmte Weise verarbeitet werden.

Zuerst empfängt die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion die CPL- \_ Init-Nachricht, wenn Windows das System Steuerungselement zum ersten Mal lädt. Die Funktion sollte jede Initialisierung durchführen, z. b. das belegen von Speicher und die Rückgabe ungleich 0 (null). Wenn das **CPlApplet** die Initialisierung nicht abschließen kann, muss es NULL zurückgeben und Windows zum Beenden der Kommunikation und zum Freigeben der dll weiterleiten.

Wenn die CPL- \_ Init-Nachricht erfolgreich war, sendet Windows die CPL \_ GetCount-Nachricht. Die Funktion muss dann die Anzahl der System Steuerungselemente zurückgeben, die von der DLL-Datei unterstützt werden.

Die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion empfängt dann eine CPL \_ -Anfrage Nachricht und eine CPL- \_ newinquire-Nachricht für jedes System Steuerungselement, das von der DLL-Datei unterstützt wird. Die-Funktion füllt eine [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur mit Informationen über Ihr Element aus, z. b. Name, Symbol und eine beschreibende Zeichenfolge. Die meisten Anwendungen sollten die CPL \_ -Anfrage Nachricht verarbeiten und die CPL- \_ Netzteil Nachricht ignorieren. Die CPL- \_ Anfrage Nachricht enthält Informationen in einer Form, die von Windows zwischengespeichert werden kann. Dies führt zu einer wesentlich besseren Leistung. Die CPL- \_ Netzteil Meldung wird nur verwendet, wenn Sie das Symbol des Elements ändern oder Zeichen folgen basierend auf dem Zustand des Computers anzeigen müssen. System Steuerungselemente, die CPL- \_ Netzteile verwenden, können nicht über eine **Startmenü** Suche in Windows Vista gefunden werden, da Sie auf Caching basiert.

Die Funktion [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) empfängt als nächstes eine CPL- \_ dblclk-Nachricht als Benachrichtigung, dass der Benutzer das Symbol ausgewählt hat, das das System Steuerungselement darstellt. Die Funktion kann diese Nachricht beliebig oft empfangen. Die Meldung enthält den Element Bezeichner und den **lpdata** -Zeiger, der in der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur beim [**cpl \_**](cpl-inquire.md) -oder CPL-Befehl zurückgegeben wird. [**\_**](cpl-newinquire.md) Die Funktion sollte das entsprechende Dialogfeld anzeigen und nachfolgende Benutzereingaben verarbeiten.

Zusätzlich zu cpl- \_ dblclk kann die CPL- \_ startwparser-Nachricht gesendet werden, wenn ein System Steuerungselement mit Eingabe Parametern aufgerufen wird, z. b. über eine Eingabeaufforderung oder ein anderes Programm. Die Meldung enthält den Element Bezeichner sowie die zusätzliche Parameter Zeichenfolge.

Bevor die steuernde Anwendung beendet wird, empfängt [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) die CPL-beendenden \_ Nachricht einmal für jedes System Steuerungselement, das von der DLL-Datei unterstützt wird. Die Meldung enthält den Bezeichner für das System Steuerungselement und den **lpdata** -Zeiger, der in der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur beim cpl-Anweisungs-oder CPL-Befehl zurückgegeben wird [**\_**](cpl-inquire.md) . [**\_**](cpl-newinquire.md) Die Funktion sollte jeglichen Speicher freigeben, den Sie für das angegebene Dialogfeld zugeordnet hat.

Nach der letzten cpl-Beendigungs \_ Meldung empfängt [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) eine CPL-Beendigungs \_ Nachricht. Die Funktion sollte den verbleibenden zugeordneten Arbeitsspeicher freigeben und die Registrierung aller privaten Fenster Klassen aufheben, die Sie möglicherweise registriert hat. Unmittelbar nach der Rückgabe der Funktion aus dieser Meldung gibt Windows das System Steuerungselement aus, indem die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPlApplet](using-cplapplet.md)
</dt> <dt>

[Ausführen von System Steuerungselementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von System Steuerungselementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
