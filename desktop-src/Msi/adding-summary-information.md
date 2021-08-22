---
description: Die folgenden Zusammenfassungsinformationseigenschaften müssen in jedem Installationspaket definiert werden, wobei ein Softwaretool verwendet wird, um auf die Istream-Schnittstelle des Zusammenfassungsinformationsstreams zuzugreifen.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Hinzufügen von Zusammenfassungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dc43ba8df737fb4d7c30998ec6c9581376df6ef6274140e68ec767e3a416f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328580"
---
# <a name="adding-summary-information"></a>Hinzufügen von Zusammenfassungsinformationen

Die folgenden Zusammenfassungsinformationseigenschaften müssen in jedem Installationspaket definiert werden, wobei ein Softwaretool verwendet wird, um auf die **Istream-Schnittstelle** des [Zusammenfassungsinformationsstreams](summary-information-stream.md)zuzugreifen. Sie können z. B. das Tool verwenden, das mit dem Windows Installer SDK bereitgestellt Msiinfo.exe, um diese Eigenschaften festzulegen. Wenn diese Eigenschaften nicht festgelegt sind, besteht das Paket nicht die [Paketvalidierung.](package-validation.md)



| Eigenschaft "Zusammenfassungsinformationen"                                                   | Daten                                   | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Vorlage**](template-summary.md)(Plattform und Sprache)<br/>         | ;1033                                  | Plattform und Sprache, die von der Datenbank verwendet werden. Wenn die Plattformspezifikation im Eigenschaftswert [**Vorlagenzusammenfassung**](template-summary.md) fehlt, geht das Installationsprogramm von der Intel-Architektur aus. Die [**ProductLanguage-Eigenschaft**](productlanguage.md) aus der Datenbank wird in der Regel für diese Zusammenfassungseigenschaft verwendet. Die Sprach-ID des Beispiels gibt an, dass das Paket englisch (USA) verwendet. |
| [**Revisionsnummer**](revision-number-summary.md)(Paketcode)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Dies ist die [Paketcode-GUID,](guid.md) die das Beispielpaket eindeutig identifiziert. Wenn Sie dieses Beispiel reproduzieren, verwenden Sie ein Hilfsprogramm wie GUIDGEN, um eine andere GUID für Ihr Paket zu generieren. Die Ergebnisse von GUIDGEN enthalten Kleinbuchstaben. Beachten Sie, dass Sie alle Kleinbuchstaben für einen gültigen Paketcode in Großbuchstaben ändern müssen. Weitere Informationen finden Sie unter [Paketcodes.](package-codes.md)             |
| [**Seitenanzahl**](page-count-summary.md)(Mindestversion des Installationsprogramms)<br/> | 200                                    | Für mindestens Windows Installer 2.0 sollte diese Eigenschaft auf die ganze Zahl 200 festgelegt werden.                                                                                                                                                                                                                                                                                                                 |
| [**Wortanzahl**](word-count-summary.md)(Quelltyp)<br/>            | 0                                      | Der globale Quelltyp für das Paket ist lange Dateinamen und nicht komprimiert. Weitere Informationen finden Sie unter [Komprimierte und unkomprimierte Quellen](compressed-and-uncompressed-sources.md) und in der Beschreibung der Spalte Attribute der [Dateitabelle.](file-table.md)                                                                                                                                |



 

Die restlichen Eigenschaften des Zusammenfassungsdatenstroms sind nicht erforderlich, sollten jedoch für das MNP2000.msi Beispiel festgelegt werden.



| Eigenschaft "Zusammenfassungsinformationen"                                 | Daten                                                                             | Hinweise                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Titel**](title-summary.md)                               | Installationsdatenbank                                                            | Informiert Benutzer, dass diese Datenbank für eine Installation und nicht für eine Transformation oder einen Patch vorgesehen ist.                        |
| [**Betreff**](subject-summary.md)                           | MNP2000                                                                          | Dateibrowser können dies als das Produkt anzeigen, das mit dieser Datenbank installiert werden soll.                                  |
| [**Keywords**](keywords-summary.md)                         | Installationsprogramm, MSI, Datenbank                                                         | Dateibrowser, die schlüsselwortsuchen können, können nach diesen Wörtern suchen.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Name des Herstellers des Produkts.                                                                                |
| [**Kommentare**](comments-summary.md)                         | Diese Installationsdatenbank enthält die Logik und die Daten, die für die Installation von Editor erforderlich sind. | Informiert Benutzer über den Zweck dieser Datenbank.                                                                  |
| [**Erstellen einer Anwendung**](creating-application-summary.md) | Orca                                                                             | Anwendung, die zum Erstellen der Installationsdatenbank verwendet wird. Im Beispiel wird der Orca-Datenbank-Editor als Beispiel angegeben. |
| [**Security**](security-summary.md)                         | 0                                                                                | Die Beispieldatenbank verfügt über uneingeschränkten Lese-/Schreibzugriff.                                                                    |



 

Sie müssen die Zusammenfassungseigenschaften [**Last Saved By**](last-saved-by-summary.md), Last Saved [**Time/Date**](last-saved-time-date-summary.md), [**Create Time/Date**](create-time-date-summary.md), [**Last Printed**](last-printed-summary.md), [**Character Count**](character-count-summary.md)und [**Codepage**](codepage-summary.md) nicht festlegen, um diese Beispieldatenbank abzuschließen. Das Beispiel basiert auf dem Datenbankbearbeitungstool, um diese optionalen Eigenschaften festzulegen und zu aktualisieren.

Um beispielsweise MsiInfo zum Hinzufügen der Zusammenfassungsinformationen zum Beispiel zu verwenden, wechseln Sie in das Verzeichnis, das die Datenbank enthält, und verwenden Sie die folgende Befehlszeile. Verwenden Sie die unten gezeigte Beispielpaket-ID nicht erneut.

**Msiinfo.exe MNP2000.msi -T "Installationsdatenbank" -J Betreff -A "Microsoft Corporation" -K "Installer, MSI, Database" -O "This installer database contains the logic and data required to install Editor." -P ;1033 -V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} -G 200 -W 0 -N Orca -U 0**

Weitere Informationen zu Zusammenfassungsinformationen finden Sie unter [About the Summary Information Stream](about-the-summary-information-stream.md), Using the [Summary Information Stream](using-the-summary-information-stream.md)und [Summary Information Stream Reference](summary-information-stream-reference.md).

Eine vollständige Liste aller Zusammenfassungsinformationseigenschaften [und](summary-property-descriptions.md) Beschreibungen der Zusammenfassungseigenschaften finden Sie unter Zusammenfassungsinformationsdatenstrom-Eigenschaftensatz. [](summary-information-stream-property-set.md)

[Fortsetzen](importing-the-user-interface.md)

 

 




