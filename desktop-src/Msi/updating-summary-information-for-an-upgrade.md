---
description: Der Paketcode des Upgradepakets muss von dem des ursprünglichen Produkts geändert werden.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Aktualisieren von Zusammenfassungsinformationen für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6849a315f5251538acc749d3c3a2ed5605d82ec4159fadf584b5a087a9beaeee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141596"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Aktualisieren von Zusammenfassungsinformationen für ein Upgrade

Der Paketcode des Upgradepakets muss von dem des ursprünglichen Produkts geändert werden. Der Paketcode wird in der [**Revisionsnummer-Zusammenfassungseigenschaft**](revision-number-summary.md) gespeichert. Weitere Informationen finden Sie unter [Paketcodes](package-codes.md). Verwenden Msiinfo.exe oder einen anderen Editor, um die Zusammenfassungsinformationen der MNP2001.msi wie unter Hinzufügen von [Zusammenfassungsinformationen beschrieben zu ändern.](adding-summary-information.md)



| Eigenschaft "Zusammenfassungsinformationen"                                                   | Daten                                                                             | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Vorlage**](template-summary.md)(Plattform und Sprache)<br/>         | ;1033                                                                            | Plattform und Sprache, die von der Datenbank verwendet werden. Wenn die Plattformspezifikation im Eigenschaftswert [**Vorlagenzusammenfassung**](template-summary.md) fehlt, geht das Installationsprogramm von der Intel-Architektur aus. Die [**ProductLanguage-Eigenschaft**](productlanguage.md) aus der Datenbank wird in der Regel für diese Zusammenfassungseigenschaft verwendet. Die Sprach-ID des Beispiels gibt an, dass das Paket englisch (USA) verwendet. |
| [**Revisionsnummer**](revision-number-summary.md)(Paketcode)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Dies ist die [Paketcode-GUID,](guid.md) die das Beispielpaket eindeutig identifiziert. Wenn Sie dieses Beispiel reproduzieren, verwenden Sie ein Hilfsprogramm wie GUIDGEN, um eine andere GUID für Ihr Paket zu generieren. Die Ergebnisse von GUIDGEN enthalten Kleinbuchstaben. Beachten Sie, dass Sie für einen gültigen Paketcode alle Kleinbuchstaben in Großbuchstaben ändern müssen.                                                     |
| [**Seitenanzahl**](page-count-summary.md)(Mindestversion des Installationsprogramms)<br/> | 200                                                                              | Für mindestens Windows Installer-Version 2.0 sollte diese Eigenschaft auf die ganze Zahl 200 festgelegt werden.                                                                                                                                                                                                                                                                                                         |
| [**Wortanzahl**](word-count-summary.md)(Typ der Quelle)<br/>            | 0                                                                                | Der globale Quelltyp für das Paket sind lange Dateinamen und unkomprimiert. Weitere Informationen finden Sie unter [Compressed and Uncompressed Sources](compressed-and-uncompressed-sources.md) (Komprimierte und nicht komprimierte Quellen) und in der Beschreibung der Attributes -Spalte der [File-Tabelle.](file-table.md)                                                                                                                               |
| [**Titel**](title-summary.md)                                                 | Installationsdatenbank                                                            | Informiert Benutzer darüber, dass diese Datenbank für eine Installation und nicht für eine Transformation oder einen Patch verwendet wird.                                                                                                                                                                                                                                                                                                          |
| [**Subject**](subject-summary.md)                                             | MNP2001                                                                          | Dateibrowser können dies als Produkt anzeigen, das mit dieser Datenbank installiert werden soll.                                                                                                                                                                                                                                                                                                                    |
| [**Keywords**](keywords-summary.md)                                           | Installationsprogramm, MSI, Datenbank                                                         | Dateibrowser, die schlüsselwortsuchen können, können nach diesen Wörtern suchen.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Name des Herstellers des Produkts.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Kommentare**](comments-summary.md)                                           | Diese Installationsdatenbank enthält die Logik und die Daten, die für die Installation von Editor. | Informiert Benutzer über den Zweck dieser Datenbank.                                                                                                                                                                                                                                                                                                                                                    |
| [**Erstellen einer Anwendung**](creating-application-summary.md)                   | Orca                                                                             | Anwendung, die zum Erstellen der Installationsdatenbank verwendet wird. Im Beispiel wird der Orca-Datenbank-Editor als Beispiel angegeben.                                                                                                                                                                                                                                                                                   |
| [**Security**](security-summary.md)                                           | 0                                                                                | Die Beispieldatenbank besteht aus uneingeschränktem Lese-/Schreibzugriff.                                                                                                                                                                                                                                                                                                                                                      |



 

[Fortsetzen](validating-an-installation-upgrade.md)

 

 




