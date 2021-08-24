---
description: Dialogfelder werden in der Spalte Dialog der Tabelle Dialog angegeben. Weitere Informationen zum Hinzufügen eines Dialogfelds oder einer Benutzeroberfläche finden Sie unter Verwenden der Benutzeroberfläche.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Dialogfelder (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38da0e4d562854abc32064eee06a303747c2587591a5526ae98177a13e0462a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764060"
---
# <a name="dialog-boxes-windows-installer"></a>Dialogfelder (Windows Installer)

Dialogfelder werden in der Spalte Dialog der [Tabelle Dialog angegeben.](dialog-table.md) Weitere Informationen zum Hinzufügen eines Dialogfelds oder einer Benutzeroberfläche finden Sie unter [Verwenden der Benutzeroberfläche](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Reservierte Dialogfeldnamen

Die folgenden Dialogfeldnamen werden vom Windows Installer reserviert und sollten nicht für benutzerdefinierte Dialogfelder verwendet werden, die vom Benutzer verfasst wurden. Das Installationsprogramm erfordert, dass diese Dialogfelder in der [Tabelle Dialog](dialog-table.md) mit den folgenden reservierten Namen aufgeführt werden. Jedes Dialogfeld und jeder Name kann nur einmal aufgeführt werden. Entwickler müssen diese Dialogfelder in der Benutzeroberfläche erstellen. Informationen zum Anzeigen einer Vorschau von Dialogfeldern finden Sie unter [Importieren der Benutzeroberfläche](importing-the-user-interface.md).



| Name des Dialogfelds                                      | Kurze Beschreibung des Dialogfelds                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FilesInUse-Dialogfeld](filesinuse-dialog.md)           | Warnt den Benutzer bei Prozessen, die Dateien überschreiben oder löschen.                                                                                                                 |
| [FirstRun-Dialogfeld](firstrun-dialog.md)               | Erfasst Benutzername, Unternehmensname und Produkt-ID.                                                                                                                       |
| [Dialogfeld "MsiRMFilesInUse"](msirmfilesinuse-dialog.md) | Benachrichtigt den Benutzer über Prozesse zum Überschreiben oder Löschen von Dateien und gibt dem Benutzer die Möglichkeit, den [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) zum Schließen und Neustarten von Anwendungen zu verwenden. |



 

## <a name="required-dialog-boxes"></a>Erforderliche Dialogfelder

Während der Installation führen bestimmte Ereignisse dazu, [](using-a-sequence-table.md) Windows Installer die Sequenztabellen der Benutzeroberfläche im Paket überprüft und das angegebene Dialogfeld angezeigt wird. Im Falle eines schwerwiegenden Fehlers zeigt der Windows-Installer beispielsweise das Dialogfeld an, das mit der Sequenznummer -3 in der Sequenztabelle der Benutzeroberfläche aufgeführt ist, unabhängig davon, was dieses Dialogfeld in der [Tabelle Dialog](dialog-table.md)heißt. In der folgenden Tabelle sind die spezifischen Ereignisse und die entsprechende Sequenznummer in der Sequenztabelle der Benutzeroberfläche aufgeführt:



| Ereignistyp                        | Sequenznummer der Sequenztabelle der Benutzeroberfläche | Beschreibung des Dialogfelds                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Schwerwiegender Fehler](fatalerror-dialog.md) | -3                                            | Die Installation wurde durch einen schwerwiegenden Fehler beendet.      |
| [Benutzerabstieg](userexit-dialog.md)     | –2                                            | Die Installation wurde auf Anforderung des Benutzers beendet. |
| [Beenden](exit-dialog.md)              | –1                                            | Die Installation wurde erfolgreich abgeschlossen.               |



 

Darüber hinaus muss der Paketautor ein generisches Dialogfeld erstellen, um fehlermeldungen Windows Installer [anzuzeigen.](error-dialog.md) Dieses Dialogfeld kann mit einem anderen Namen benannt werden, aber dieser Name muss in der **ErrorDialog-Eigenschaft angegeben** werden.

## <a name="typical-dialog-boxes"></a>Typische Dialogfelder

Die folgenden Dialogfelder sind optional und häufig in der erstellten Benutzeroberfläche eines Installationspakets enthalten. Diese Dialogfelder sind typisch für die [meisten Benutzeroberflächen-Assistenten](user-interface-wizard-behavior.md) zum Installieren von Dateien. Diese Dialogfelder können einen beliebigen Namen in der Tabelle Dialog haben. Die angezeigten Namen werden nur aus Gründen der Übersichtlichkeit empfohlen und können bei Bedarf geändert werden. Beispielsweise können zwei verschiedene benutzerdefinierte **LicenseAgreement-Dialogfelder** im Paket verwendet und in der Tabelle Dialog mit den Namen ProfessionalLicenseAgreement und LimitedLicenseAgreement unterschieden werden.



| Dialogfeldtyp                                             | Kurze Beschreibung des Dialogfelds                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Dialogfeld "DiskCost"](diskcost-dialog.md)                  | Gibt an, dass nicht genügend Speicherplatz für die Installation zur Verfügung steht. |
| [Durchsuchen des Dialogfelds](browse-dialog.md)                      | Ermöglicht dem Benutzer die Auswahl eines Verzeichnisses.                     |
| [Dialogfeld "Abbrechen"](cancel-dialog.md)                      | Bestätigt eine Anforderung zum Beenden der Installation.       |
| [Dialogfeld "Lizenzvertrag"](licenseagreement-dialog.md) | Modales Feld, in dem der Lizenzvertrag angezeigt wird.             |
| [Auswahldialogfeld](selection-dialog.md)                | Modales Feld, in dem der Benutzer Elemente auswählen kann.            |



 

 

 
