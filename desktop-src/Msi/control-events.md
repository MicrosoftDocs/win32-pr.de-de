---
description: Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm ausgeführt werden soll, oder eine Änderung der Attribute eines oder mehrerer Steuerelemente in einem Dialogfeld. Weitere Informationen zu ControlEvents finden Sie unter ControlEvent Overview.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Steuerelement Ereignisse (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e8d9e6a8cea9a02b303040d06da346800912e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363542"
---
# <a name="control-events-windows-installer"></a>Steuerelement Ereignisse (Windows Installer)

Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm ausgeführt werden soll, oder eine Änderung der Attribute eines oder mehrerer Steuerelemente in einem Dialogfeld. Weitere Informationen zu ControlEvents finden Sie unter [ControlEvent Overview](controlevent-overview.md).

In der folgenden Tabelle finden Sie Links zu weiteren Informationen zu bestimmten ControlEvents.



| Steuerungs Ereignis                                                       | Kurze Beschreibung von ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Veröffentlicht Daten für die letzte Aktion.                                                                                                                                                                          |
| [Action Text](actiontext-controlevent.md)                           | Veröffentlicht den Namen der aktuellen Aktion.                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | Benachrichtigt den Installer, dass Features lokal ausgeführt werden.                                                                                                                                                               |
| [Addsource](addsource-controlevent.md)                             | Benachrichtigt den Installer, Features aus seiner Quelle auszuführen.                                                                                                                                                     |
| [Checkexistingtargetpath](checkexistingtargetpath-controlevent.md) | Benachrichtigt das Installationsprogramm, ob der Pfad geschrieben werden kann.                                                                                                                                                |
| [Checktargetpath](checktargetpath-controlevent.md)                 | Benachrichtigt das Installationsprogramm, ob der Pfad gültig ist.                                                                                                                                                      |
| [Directoriylistnew](directorylistnew-controlevent.md)               | Benachrichtigt das directorylist-Steuerelement, einen neuen Ordner zu erstellen.                                                                                                                                                    |
| [Directoriylistopen](directorylistopen-controlevent.md)             | Wählt das Verzeichnis im Director List-Steuerelement aus.                                                                                                                                                           |
| [Directoren](directorylistup-controlevent.md)                 | Benachrichtigt das Director List-Steuerelement, das übergeordnete Element des aktuellen Verzeichnisses auszuwählen.                                                                                                                             |
| [DoAction](doaction-controlevent.md)                               | Das-Dialog Feld benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen.                                                                                                                                                 |
| [Enablerollback](enablerollback-controlevent.md)                   | Dient zum Aktivieren und Deaktivieren von Rollback-Funktionen.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen.                                                                                                                                                          |
| [Ignorechange](ignorechange-controlevent.md)                       | Wird vom directorylist-Steuerelement veröffentlicht, wenn ein Ordner hervorgehoben, aber nicht geöffnet wird.                                                                                                                           |
| [Msilaunchapp](msilaunchapp-controlevent.md)                       | Dieses Steuerungs Ereignis führt eine angegebene Datei aus. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                                                       |
| [Msiprint](msiprint-controlevent.md)                               | Ermöglicht dem Benutzer das Drucken des Inhalts des [scrollabletext-Steuer](scrollabletext-control.md)Elements. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/> |
| [Newdialog](newdialog-controlevent.md)                             | Benachrichtigt das Installationsprogramm, ein modales Dialogfeld in ein anderes Dialogfeld zu ändern.                                                                                                                                  |
| [Neuinstallation](reinstall-controlevent.md)                             | Initiiert eine erneute Installation von-Funktionen.                                                                                                                                                                       |
| [Rein Stall Mode](reinstallmode-controlevent.md)                     | Gibt den Validierungs Modus während einer erneuten Installation an.                                                                                                                                                        |
| [Remove](remove-controlevent.md)                                   | Benachrichtigt das Installationsprogramm, wenn Features zum Entfernen ausgewählt werden.                                                                                                                                                |
| [Zurücksetzen](reset-controlevent.md)                                     | Setzt alle Eigenschaftswerte auf die Standardwerte zurück, die beim Erstellen des Dialog Felds verwendet wurden.                                                                                                                    |
| [Rmshutdownandrestart](rmshutdownandrestart-controlevent.md)       | Verwenden Sie den [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) , um alle Anwendungen mit verwendeten Dateien herunterzufahren und am Ende der Installation neu zu starten.                                                              |
| [Scriptinprogress](scriptinprogress-controlevent.md)               | Zeigt eine Zeichenfolge an, während das Ausführungs Skript kompiliert wird.                                                                                                                                                     |
| [Selectionaction](selectionaction-controlevent.md)                 | Wird von SelectionTree veröffentlicht, um ein Element zu beschreiben.                                                                                                                                                               |
| [Selectionbrowse](selectionbrowse-controlevent.md)                 | Wird von SelectionTree veröffentlicht, um ein Dialogfeld zu erzeugen.                                                                                                                                                             |
| [Selectiondescription](selectiondescription-controlevent.md)       | Veröffentlicht von SelectionTree, um eine Zeichenfolge im Beschreibungsfeld der Funktions Tabelle bereitzustellen.                                                                                                                 |
| [Selectionnoitems](selectionnoitems-controlevent.md)               | Wird von SelectionTree zum Löschen von Text oder Deaktivieren von Schaltflächen verwendet.                                                                                                                                                      |
| [Selectionpath](selectionpath-controlevent.md)                     | Veröffentlicht von SelectionTree, um den Pfad eines Elements bereitzustellen.                                                                                                                                                    |
| [Selectionpathon](selectionpathon-controlevent.md)                 | Veröffentlicht von SelectionTree, um anzugeben, ob ein Pfad mit einer Funktion verknüpft ist.                                                                                                                     |
| [Selectionsize](selectionsize-controlevent.md)                     | Veröffentlichung durch das SelectionTree-Steuerelement, um die Größe eines Elements anzugeben.                                                                                                                                            |
| [Setinstalllevel](setinstalllevel-controlevent.md)                 | Der Installer ändert die Installations Ebene in einen angegebenen Wert.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Wird vom Installationsprogramm veröffentlicht, um den Installationsfortschritt bereitzustellen.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Legt eine angegebene Eigenschaft fest.                                                                                                                                                                                    |
| [Settargetpath](settargetpath-controlevent.md)                     | Benachrichtigt das Installationsprogramm, einen Pfad zu überprüfen und festzulegen.                                                                                                                                                               |
| [Spawndialog](spawndialog-controlevent.md)                         | Benachrichtigt den Installer, ein untergeordnetes Element einer modalen Box zu erstellen.                                                                                                                                                      |
| [Spawnwaitdialog](spawnwaitdialog-controlevent.md)                 | Löst ein angegebenes Dialogfeld aus.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Veröffentlicht vom Installer, um die verbleibende Zeit in der Fortschritts Sequenz anzugeben.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Legt ProductID auf die vollständige Produkt-ID fest.                                                                                                                                                                        |



 

 

