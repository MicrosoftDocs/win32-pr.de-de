---
description: Der Paketcode des upgradepakets muss von dem des ursprünglichen Produkts geändert werden.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Aktualisieren von Zusammenfassungs Informationen für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050477"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Aktualisieren von Zusammenfassungs Informationen für ein Upgrade

Der Paketcode des upgradepakets muss von dem des ursprünglichen Produkts geändert werden. Der Paketcode wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " gespeichert. Weitere Informationen finden Sie unter [Paket Codes](package-codes.md). Verwenden Sie Msiinfo.exe oder einen anderen Editor, um die Zusammenfassungs Informationen MNP2001.msi zu ändern, wie unter [Hinzufügen von Zusammenfassungs Informationen](adding-summary-information.md)beschrieben.



| Eigenschaft für Zusammenfassungs Informationen                                                   | Daten                                                                             | Notizen                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Vorlage**](template-summary.md)(Plattform und Sprache)<br/>         | ; 1033                                                                            | Plattform und Sprache, die von der Datenbank verwendet werden. Wenn die Platt Form Spezifikation im Eigenschafts Wert für die [**Vorlagen**](template-summary.md) Zusammenfassung fehlt, nimmt das Installationsprogramm die Intel-Architektur an. Die [**productlanguage**](productlanguage.md) -Eigenschaft aus der Datenbank wird in der Regel für diese Zusammenfassungs Eigenschaft verwendet. Die Sprach-ID des Beispiels gibt an, dass das Paket US-Englisch verwendet. |
| [**Revisionsnummer**](revision-number-summary.md)(Paketcode)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Dies ist die Paket Code- [GUID](guid.md) , die das Beispiel Paket eindeutig identifiziert. Wenn Sie dieses Beispiel reproduzieren, verwenden Sie ein Dienstprogramm wie z. b. GUIDGEN, um eine andere GUID für das Paket zu generieren. Die Ergebnisse von Guidgen enthalten Kleinbuchstaben. Beachten Sie, dass Sie alle Kleinbuchstaben für einen gültigen Paketcode in Großbuchstaben ändern müssen.                                                     |
| [**Seitenanzahl**](page-count-summary.md)(minimale Installerversion)<br/> | 200                                                                              | Für eine minimale Windows Installer Version 2,0 sollte diese Eigenschaft auf die ganze Zahl 200 festgelegt werden.                                                                                                                                                                                                                                                                                                         |
| [**Wort Anzahl**](word-count-summary.md)(Quelltyp)<br/>            | 0                                                                                | Der globale Quelltyp für das Paket ist lange Dateinamen und unkomprimiert. Weitere Informationen finden Sie unter [komprimierte und nicht komprimierte Quellen](compressed-and-uncompressed-sources.md) und in der Beschreibung der Spalte Attribute der [Dateitabelle](file-table.md).                                                                                                                               |
| [**Titel**](title-summary.md)                                                 | Installations Datenbank                                                            | Teilt den Benutzern mit, dass es sich bei dieser Datenbank um eine Installation anstelle einer Transformation oder eines Patches handelt.                                                                                                                                                                                                                                                                                                          |
| [**Subject**](subject-summary.md)                                             | MNP2001                                                                          | Dateibrowser können dies als Produktanzeigen, das mit dieser Datenbank installiert werden soll.                                                                                                                                                                                                                                                                                                                    |
| [**Keywords**](keywords-summary.md)                                           | Installer, MSI, Datenbank                                                         | Dateibrowser, die für die Suche nach Schlüsselwörtern geeignet sind, können nach diesen Wörtern suchen.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Der Name des Herstellers des Produkts.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Kommentare**](comments-summary.md)                                           | Diese Installerdatenbank enthält die Logik und die Daten, die zum Installieren von Notepad erforderlich sind. | Informiert Benutzer über den Zweck dieser Datenbank.                                                                                                                                                                                                                                                                                                                                                    |
| [**Anwendung wird erstellt**](creating-application-summary.md)                   | Orca                                                                             | Anwendung, die zum Erstellen der Installations Datenbank verwendet wird. Das Beispiel gibt den Orca-Datenbank-Editor als Beispiel an.                                                                                                                                                                                                                                                                                   |
| [**Sicherheit**](security-summary.md)                                           | 0                                                                                | Die Beispieldatenbank weist uneingeschränkten Lese-/Schreibzugriff auf.                                                                                                                                                                                                                                                                                                                                                      |



 

[Fortsetzen](validating-an-installation-upgrade.md)

 

 




