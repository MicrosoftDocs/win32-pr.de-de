---
description: Vor Windows Vista haben Sie ein System Steuerungselement erstellt, indem Sie eine DLL-Datei erstellen und diese mit der Erweiterung. cpl benennen.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Verwenden von CPlApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979480"
---
# <a name="using-cplapplet"></a>Verwenden von CPlApplet

Vor Windows Vista haben Sie ein System Steuerungselement erstellt, indem Sie eine DLL-Datei erstellen und diese mit der Erweiterung. cpl benennen. Diese Datei hat die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion exportiert. Dieses Schema wird weiterhin in Windows Vista und höheren Versionen unterstützt und wird in diesem Thema erläutert. Die Richtlinien für neue System Steuerungselemente empfehlen jedoch einen einfacheren Ansatz mit dem System Steuerungselement, das als exe-Datei erstellt wurde, die ein Layout für den Aufgaben Fluss verwendet.

Wenn die Systemsteuerung eine DLL-Datei (oder. cpl) lädt, ruft Sie die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion auf, um Informationen wie die Anzahl der System Steuerungselemente, die die Datei hostet, sowie Informationen zu den einzelnen Elementen zu erhalten. Die Systemsteuerung ruft auch die-Funktion auf, wenn das Element Fenster initialisiert, geöffnet oder geschlossen wird.

Wenn Windows das System Steuerungselement zum ersten Mal lädt, ruft es die Adresse der [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion ab und verwendet diese Adresse anschließend zum Abrufen der Funktion und zum Übergeben von Nachrichten. Möglicherweise werden die folgenden Nachrichten gesendet.



| `Message`                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPL- \_ dblclk**](cpl-dblclk.md)           | Wird gesendet, um [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten System Steuerungselement zugeordnet ist. **CPlApplet** sollte das Dialogfeld für das angegebene Element anzeigen und alle benutzerdefinierten Tasks ausführen. Der **CPlApplet** *lParam1* -Parameter ist eine ganze Zahl, die den NULL basierten Index des System Steuerungs Elements darstellt. Der *lParam2* -Parameter ist der **lpdata** -Zeiger, der in der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur in der [**cpl \_**](cpl-inquire.md) -oder der [**cpl- \_ newinquire**](cpl-newinquire.md) -Nachricht zurückgegeben wird. Der Rückgabewert wird ignoriert.                                                                |
| [**CPL- \_ Exit**](cpl-exit.md)               | Wird nach der letzten cpl \_ -Stoppnachricht gesendet, und unmittelbar bevor Windows die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion verwendet, um die dll freizugeben, die das System Steuerungselement enthält. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) muss den verbleibenden Arbeitsspeicher freigeben und die Schließung vorbereiten. Der Rückgabewert wird ignoriert.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL- \_ GetCount**](cpl-getcount.md)       | Wird nach der CPL- \_ Init-Nachricht gesendet, um [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) aufzufordern, eine Zahl zurückzugeben, die angibt, wie viele Unterprogramme unterstützt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**CPL- \_ Init**](cpl-init.md)               | Wird unmittelbar nach dem Laden der dll, die das System Steuerungselement enthält, gesendet. In der Meldung wird [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) aufgefordert, Initialisierungs Prozeduren auszuführen, einschließlich der Speicher Belegung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CPL- \_ Anfrage**](cpl-inquire.md)         | Wird nach der CPL- \_ GetCount-Nachricht gesendet, um [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) aufzufordern, Informationen zu einem angegebenen untergeordneten Programm bereitzustellen. Der *lParam1* -Wert ist eine ganze Zahl, die den NULL basierten Index des Unterprogramms darstellt, über das Informationen angefordert werden. Der *lParam2* -Parameter von **CPlApplet** verweist auf eine [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur. Der Rückgabewert wird ignoriert.                                                                                                                                                                                                                                                                                                    |
| [**CPL- \_ Netzdatei**](cpl-newinquire.md)   | Wird nach der CPL- \_ GetCount-Nachricht gesendet, um [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) aufzufordern, Informationen zu einem angegebenen System Steuerungselement bereitzustellen. Der *lParam1* -Wert ist eine ganze Zahl, die den NULL basierten Index des Unterprogramms darstellt, über das Informationen angefordert werden. Der *lParam2* -Parameter ist ein Zeiger auf eine [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur. CPL- \_ netwinquire sollte normalerweise ignoriert werden. In Ihrer Anwendung sollten nur cpl- \_ Anfragen auf Windows 95, Microsoft Windows NT 4,0 und höher verarbeitet werden, da die System Steuerungs Leistung bei Verwendung von cpl- \_ netzwinquire beeinträchtigt ist. Dies liegt daran, dass die zurückgegebenen Zeichen folgen und Symbole nicht zwischengespeichert werden können. Der Rückgabewert wird ignoriert. |
| [**CPL- \_ Auswahl**](cpl-select.md)           | Veraltet. Diese Meldung wird von den aktuellen Versionen von Windows nicht gesendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ startwparamems**](cpl-startwparms.md) | Wird gesendet, um das [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. **CPlApplet** sollte das entsprechende Dialogfeld anzeigen und alle benutzerdefinierten Tasks ausführen. Diese Meldung ähnelt cpl \_ dblclk, es gibt jedoch möglicherweise weitere Informationen. Der *lParam1* -Parameter ist die System Steuerungselement-Nummer, und *lParam2* ist ein **LPCTSTR** zu allen zusätzlichen Richtungen, die ggf. erforderlich sind. Gibt **true** zurück, wenn diese Nachricht verarbeitet wird. andernfalls **false**. Diese Nachricht ist für die [Version 5,00](versions.md) und höher von Shell32.dll gültig.                                                                                         |
| [**CPL- \_ Beendigung**](cpl-stop.md)               | Wird einmal für jedes System Steuerungselement in der CPL-Datei gesendet, bevor Windows die System Steuerungs Erweiterung entlädt. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) sollte jeden Arbeitsspeicher freigeben, der der in *lParam1* angegebenen Element Nummer zugeordnet ist. Der *lParam2* -Parameter ist ein **lpdata** -Zeiger, der in der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur in der [**cpl \_**](cpl-inquire.md) -oder der [**cpl- \_ newinferenzierung**](cpl-newinquire.md) zurückgegeben wird. Der Rückgabewert wird ignoriert.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Nachrichtenverarbeitung in der Systemsteuerung](message-processing.md)
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

 

 
