---
description: Zusätzlich zu den Informationen, die in den vorherigen Abschnitten erläutert wurden, enthält uisample.msi auch Daten für eine Beispiel Benutzeroberfläche.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importieren der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863039"
---
# <a name="importing-the-user-interface"></a>Importieren der Benutzeroberfläche

Zusätzlich zu den Informationen, die in den vorherigen Abschnitten erläutert wurden, enthält uisample.msi auch Daten für eine Beispiel Benutzeroberfläche. Wenn Sie uisample.msi im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md)in MNP2000.msi zusammengeführt haben, sind diese Informationen auch in MNP2000.msi vorhanden. Die Informationen für die Beispiel Benutzeroberfläche finden Sie in den folgenden Tabellen.

-   [Tabelle "aktiontext"](actiontext-table.md)
-   [Binäre Tabelle](binary-table.md)
-   [Steuerungs Tabelle](control-table.md)
-   [ControlEvent-Tabelle](controlevent-table.md)
-   [Dialog Feld Tabelle](dialog-table.md)
-   [Fehler Tabelle](error-table.md)
-   [EventMapping-Tabelle](eventmapping-table.md)
-   [RadioButton-Tabelle](radiobutton-table.md)
-   [TextStyle-Tabelle](textstyle-table.md)
-   [UIText-Tabelle](uitext-table.md)

Der Datenbank-Editor, der mit dem Installationsprogramm bereitgestellt wird, enthält eine Dialogfeld Vorschau-Option, mit der Sie eine Vorschau der Dialogfelder der Benutzeroberfläche anzeigen können, die in den obigen Tabellen in den Daten angegeben sind.

Das Beispiel Installationspaket MNP2000.msi ist jetzt für die Paketüberprüfung bereit. Führen Sie die Überprüfung immer für ein neues Paket aus, bevor Sie das Paket zum ersten Mal installieren. Dies wird unter Validieren des Installations Beispiels erläutert.

Wenn Sie die Benutzeroberfläche nicht in das Beispiel Paket einschließen möchten, können Sie alle Informationen in den oben gezeigten Tabellen weglassen oder entfernen, mit Ausnahme der [TextStyle-Tabelle](textstyle-table.md) (die zum Definieren der [**defaultuifont**](defaultuifont.md) -Eigenschaft erforderlich ist). Sie sollten auch die Eigenschaften der Benutzeroberfläche aus der Eigenschaften [Tabelle](property-table.md)entfernen. Im folgenden wird eine Beispiel Eigenschaften Tabelle für das Notepad-Beispiel ohne Benutzeroberfläche angezeigt. Verwenden Sie die in der Tabelle gezeigten GUIDs nicht erneut, wenn Sie dieses Beispiel kopieren.

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                                   | Wert                                  |
|--------------------------------------------|----------------------------------------|
| [**Defaultuifont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**Limitui**](limitui.md)                 | 1                                      |
| [**Hersteller**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18a9233c-0b34-4127-a966-c257386270bc} |
| [**Productlanguage**](productlanguage.md) | 1033                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode auch**](upgradecode.md)         | {908e378a-9551-4772-BF1D-5cfaf6fd9cb4} |



 

Ein Paket ohne Benutzeroberfläche kann von der Befehlszeile oder von einem Programm installiert werden. Verwenden Sie die unter [Befehlszeilenoptionen](command-line-options.md)beschriebenen Methoden, um ein Paket über die Befehlszeile zu installieren. Verwenden Sie zum Installieren eines Pakets von einem Programm die unter [using Installer Functions](using-installer-functions.md)beschriebenen Methoden. Führen Sie die Überprüfung immer für ein neues Paket aus, bevor Sie ein neues Paket zum ersten Mal installieren.

[Fortsetzen](validating-an-installation-database.md)

 

 



