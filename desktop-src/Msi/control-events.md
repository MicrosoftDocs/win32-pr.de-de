---
description: Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm oder eine Änderung der Attribute eines oder mehrere Steuerelemente in einem Dialogfeld ergriffen werden soll. Weitere Informationen zu ControlEvents finden Sie unter ControlEvent Overview.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Steuerungsereignisse (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd72e93da7ed84c845b5993b2a021119c861b682ab5eb4645c69c723b17a404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075090"
---
# <a name="control-events-windows-installer"></a>Steuerungsereignisse (Windows Installer)

Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm oder eine Änderung der Attribute eines oder mehrere Steuerelemente in einem Dialogfeld ergriffen werden soll. Weitere Informationen zu ControlEvents finden Sie unter [ControlEvent Overview](controlevent-overview.md).

Die folgende Tabelle enthält Links zu zusätzlichen Informationen zu bestimmten ControlEvents.



| Steuerungsereignis                                                       | Kurze Beschreibung von ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Veröffentlicht Daten für die neueste Aktion.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Veröffentlicht den Namen der aktuellen Aktion.                                                                                                                                                                     |
| [Addlocal](addlocal-controlevent.md)                               | Benachrichtigt das Installationsprogramm, dass Features lokal ausgeführt werden.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Benachrichtigt das Installationsprogramm, dass Features aus der Quelle ausgeführt werden.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Benachrichtigt das Installationsprogramm, um zu überprüfen, ob der Pfad geschrieben werden kann.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Benachrichtigt das Installationsprogramm, um zu überprüfen, ob der Pfad gültig ist.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Benachrichtigt das DirectoryList-Steuerelement, um einen neuen Ordner zu erstellen.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Wählt das Verzeichnis im DirectoryList-Steuerelement aus.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Benachrichtigt das DirectoryList-Steuerelement, um das übergeordnete Element des aktuellen Verzeichnisses auszuwählen.                                                                                                                             |
| [DoAction](doaction-controlevent.md)                               | Das Dialogfeld benachrichtigt das Installationsprogramm, eine benutzerdefinierte Aktion auszuführen.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Wird verwendet, um Rollbackfunktionen zu deaktivieren und zu aktivieren.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Wird vom DirectoryList-Steuerelement veröffentlicht, wenn ein Ordner hervorgehoben, aber nicht geöffnet wird.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Dieses Steuerelementereignis führt eine angegebene Datei aus. **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | Ermöglicht dem Benutzer das Drucken des Inhalts des [ScrollableText-Steuerelements.](scrollabletext-control.md) **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Benachrichtigt das Installationsprogramm, ein modales Dialogfeld in ein anderes Dialogfeld zu ändern.                                                                                                                                  |
| [Neuinstallation](reinstall-controlevent.md)                             | Initiiert eine Neuinstallation von Features.                                                                                                                                                                       |
| [Reinstallmode](reinstallmode-controlevent.md)                     | Gibt den Validierungsmodus während einer Neuinstallation an.                                                                                                                                                        |
| [Entfernen](remove-controlevent.md)                                   | Benachrichtigt das Installationsprogramm, wenn Features zum Entfernen ausgewählt sind.                                                                                                                                                |
| [Zurücksetzen](reset-controlevent.md)                                     | Setzt alle Eigenschaftswerte auf die Standardwerte zurück, die beim Erstellen des Dialogfelds verwendet wurden.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Verwenden Sie [den Neustart-Manager,](/windows/desktop/RstMgr/restart-manager-portal) um alle Anwendungen herunterfahren, in denen Dateien verwendet werden, und um sie am Ende der Installation neu zu starten.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Zeigt eine Zeichenfolge an, während das Ausführungsskript kompiliert wird.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Veröffentlicht von SelectionTree, um ein Element zu beschreiben.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Veröffentlicht von SelectionTree, um ein Dialogfeld zu erstellen.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Veröffentlicht von SelectionTree, um eine Zeichenfolge im Feld Beschreibung der Featuretabelle bereitstellen.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Wird von SelectionTree verwendet, um Text zu löschen oder Schaltflächen zu deaktivieren.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Veröffentlicht von SelectionTree zum Bereitstellen des Pfads eines Elements.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Veröffentlicht von SelectionTree, um anzugeben, ob einem Feature ein Pfad zugeordnet ist.                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | Wird vom SelectionTree-Steuerelement veröffentlicht, um die Größe eines Elements zu geben.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | Das Installationsprogramm ändert die Installationsebene in einen angegebenen Wert.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Wird vom Installationsprogramm veröffentlicht, um den Installationsfortschritt zu ermöglichen.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Legt eine angegebene Eigenschaft fest.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Benachrichtigt das Installationsprogramm, einen Pfad zu überprüfen und fest zu legen.                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | Benachrichtigt das Installationsprogramm, ein untergeordnetes Eines modalen Felds zu erstellen.                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Löst ein angegebenes Dialogfeld aus.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Wird vom Installationsprogramm veröffentlicht, um die verbleibende Zeit in der Statussequenz zur Verfügung zu stellen.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Legt ProductID auf die vollständige Produkt-ID fest.                                                                                                                                                                        |



 

 

