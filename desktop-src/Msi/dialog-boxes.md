---
description: Dialogfelder werden in der Dialogfeld Spalte der Dialogfeld Tabelle angegeben. Weitere Informationen zum Hinzufügen eines Dialog Felds oder eines Billboards zu einer Benutzeroberfläche finden Sie unter Verwenden der Benutzeroberfläche.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Dialog Felder (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216751"
---
# <a name="dialog-boxes-windows-installer"></a>Dialog Felder (Windows Installer)

Dialogfelder werden in der Dialogfeld Spalte der [Dialogfeld Tabelle](dialog-table.md)angegeben. Weitere Informationen zum Hinzufügen eines Dialog Felds oder eines Billboards zu einer Benutzeroberfläche finden [Sie unter Verwenden der Benutzeroberfläche](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Reservierte Dialog Feld Namen

Die folgenden Dialogfeld Namen werden von Windows Installer reserviert und sollten nicht für benutzerdefinierte Dialogfelder verwendet werden. Das Installationsprogramm erfordert, dass diese Dialogfelder in der [Dialogfeld Tabelle](dialog-table.md) unter Verwendung der folgenden reservierten Namen aufgelistet werden. Alle Dialogfelder und Namen können nur einmal aufgelistet werden. Entwickler müssen diese Dialogfelder in der Benutzeroberfläche erstellen. Informationen zum Anzeigen von Dialogfeldern für die Vorschau finden Sie unter [Importieren der Benutzeroberfläche](importing-the-user-interface.md).



| Dialog Feld Name                                      | Kurze Beschreibung des Dialog Felds                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FilesInUse (Dialog Feld)](filesinuse-dialog.md)           | Warnt den Benutzer bei Prozessen, die Dateien überschreiben oder löschen.                                                                                                                 |
| [Dialog Feld "FIRSTRUN"](firstrun-dialog.md)               | Erfasst den Benutzernamen, den Firmennamen und die Produkt-ID.                                                                                                                       |
| [Dialog Feld "msirmfilesinuse"](msirmfilesinuse-dialog.md) | Benachrichtigt den Benutzer, Prozesse zu überschreiben oder zu löschen, und gibt dem Benutzer die Möglichkeit, Anwendungen mit dem [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) zu schließen und neu zu starten. |



 

## <a name="required-dialog-boxes"></a>Erforderliche Dialog Felder

Während der Installation bewirken bestimmte Ereignisse Windows Installer, dass die [Benutzeroberflächen-Sequenz Tabellen](using-a-sequence-table.md) im Paket überprüft und das angegebene Dialogfeld angezeigt werden. Im Falle eines schwerwiegenden Fehlers zeigt Windows Installer beispielsweise das Dialogfeld mit der Sequenznummer-3 in der Sequenz Tabelle der Benutzeroberfläche an, unabhängig davon, welches Dialogfeld in der [Dialogfeld Tabelle](dialog-table.md)benannt ist. In der folgenden Tabelle werden die jeweiligen Ereignisse und ihre entsprechende Sequenznummer in der Sequenz Tabelle der Benutzeroberfläche aufgelistet:



| Ereignistyp                        | Sequenznummer der Sequenz Tabelle der Benutzeroberfläche | Beschreibung des Dialog Felds                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Schwerwiegender Fehler](fatalerror-dialog.md) | -3                                            | Die Installation wurde durch einen schwerwiegenden Fehler beendet.      |
| [Benutzer beenden](userexit-dialog.md)     | -2                                            | Die Installation wurde bei der Anforderung des Benutzers beendet. |
| [Beenden](exit-dialog.md)              | -1                                            | Die Installation wurde erfolgreich abgeschlossen.               |



 

Außerdem muss der Paket Ersteller ein generisches Dialogfeld erstellen, um Windows Installer [Fehler](error-dialog.md) Meldungen anzuzeigen. Dieses Dialogfeld kann beliebig benannt werden, aber dieser Name muss in der **ErrorDialog** -Eigenschaft angegeben werden.

## <a name="typical-dialog-boxes"></a>Typische Dialog Felder

Die folgenden Dialogfelder sind optional und im Allgemeinen in der erstellten Benutzeroberfläche eines Installationspakets enthalten. Diese Dialogfelder sind typisch für die meisten [Benutzeroberflächen-Assistenten](user-interface-wizard-behavior.md) für die Installation von Dateien. Diese Dialogfelder können einen beliebigen Namen in der Dialogfeld Tabelle aufweisen. Die angezeigten Namen werden nur aus Gründen der Übersichtlichkeit empfohlen und können nach Bedarf geändert werden. Beispielsweise können zwei verschiedene benutzerdefinierte Dialogfelder für die **Lizenzvereinbarung** im Paket verwendet und in der Dialogfeld Tabelle nach den Namen "Professional-Agreement" und "limitedlicen* Agreement" unterschieden werden.



| Dialog Feldtyp                                             | Kurze Beschreibung des Dialog Felds                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Dialogfeld ' diskcost '](diskcost-dialog.md)                  | Gibt nicht genügend Speicherplatz für die Installation an. |
| [Durchsuchen des Dialogfelds](browse-dialog.md)                      | Ermöglicht es Benutzern, ein Verzeichnis auszuwählen.                     |
| [Dialogfeld "Abbrechen"](cancel-dialog.md)                      | Bestätigt eine Anforderung zum Beenden der Installation.       |
| [Dialogfeld "Lizenzvertrag"](licenseagreement-dialog.md) | Modales Feld mit dem Lizenzvertrag.             |
| [Auswahl (Dialogfeld)](selection-dialog.md)                | Modales Feld, das dem Benutzer ermöglicht, Elemente auszuwählen.            |



 

 

 
