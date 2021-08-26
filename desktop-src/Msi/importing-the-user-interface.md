---
description: Zusätzlich zu den in den vorherigen Abschnitten erläuterten Informationen enthält uisample.msi auch Daten für eine Beispiel-Benutzeroberfläche.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importieren der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2678eb2c6fb1c53f0d052c6bb1553af0f3d773b75d057969c66d74a39e499f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043640"
---
# <a name="importing-the-user-interface"></a>Importieren der Benutzeroberfläche

Zusätzlich zu den in den vorherigen Abschnitten erläuterten Informationen enthält uisample.msi auch Daten für eine Beispiel-Benutzeroberfläche. Wenn Sie uisample.msi im Abschnitt Importieren einer leeren Datenbank in MNP2000.msi zusammengeführt [haben,](importing-a-blank-database.md)sind diese Informationen auch in MNP2000.msi vorhanden. Die Informationen für die Beispiel-Benutzeroberfläche sind in den folgenden Tabellen aufgeführt.

-   [ActionText-Tabelle](actiontext-table.md)
-   [Binäre Tabelle](binary-table.md)
-   [Steuertabelle](control-table.md)
-   [ControlEvent-Tabelle](controlevent-table.md)
-   [Dialogtabelle](dialog-table.md)
-   [Fehlertabelle](error-table.md)
-   [EventMapping-Tabelle](eventmapping-table.md)
-   [RadioButton-Tabelle](radiobutton-table.md)
-   [TextStyle-Tabelle](textstyle-table.md)
-   [UIText-Tabelle](uitext-table.md)

Der mit dem Installationsprogramm bereitgestellte Datenbank-Editor Orca enthält eine Dialogfeldvorschauoption, mit der Sie eine Vorschau der Dialogfelder der Benutzeroberfläche anzeigen können, die von den Daten in den obigen Tabellen angegeben werden.

Das Beispielinstallationspaket MNP2000.msi jetzt für die Paketvalidierung bereit. Führen Sie die Validierung immer für ein neues Paket aus, bevor Sie versuchen, das Paket zum ersten Mal zu installieren. Dies wird unter Überprüfen des Installationsbeispiels erläutert.

Wenn Sie die Benutzeroberfläche nicht in das Beispielpaket ein- oder auslassen möchten, lassen Oder entfernen Sie alle Informationen in den oben gezeigten Tabellen mit Ausnahme der [TextStyle-Tabelle](textstyle-table.md) (die zum Definieren der [**DefaultUIFont-Eigenschaft erforderlich**](defaultuifont.md) ist). Sie sollten auch Benutzeroberflächeneigenschaften aus der [Eigenschaftentabelle entfernen.](property-table.md) Im Folgenden finden Sie eine Beispieltabelle Editor Eigenschaft für das Beispiel ohne Benutzeroberfläche. Verwenden Sie die in der Tabelle angezeigten GUIDs nicht wieder, wenn Sie dieses Beispiel kopieren.

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                                   | Wert                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Hersteller**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1033                                   |
| [**Productname**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**Upgradecode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Ein Paket ohne Benutzeroberfläche kann über die Befehlszeile oder über ein Programm installiert werden. Verwenden Sie zum Installieren eines Pakets über die Befehlszeile die unter [Befehlszeilenoptionen beschriebenen Methoden.](command-line-options.md) Verwenden Sie zum Installieren eines Pakets aus einem Programm die unter [Verwenden von Installerfunktionen beschriebenen Methoden.](using-installer-functions.md) Führen Sie die Validierung immer für ein neues Paket aus, bevor Sie zum ersten Mal versuchen, ein neues Paket zu installieren.

[Fortsetzen](validating-an-installation-database.md)

 

 



