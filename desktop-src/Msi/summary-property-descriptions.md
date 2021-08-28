---
description: Zusammenfassungseigenschaften für Installationspakete, Transformationen und Patches werden in den folgenden Tabellen beschrieben.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Zusammenfassungseigenschaftsbeschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb93e5881a25b6b79eef0fb0711acc1fec1b6666
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629543"
---
# <a name="summary-property-descriptions"></a>Zusammenfassungseigenschaftsbeschreibungen

Zusammenfassungseigenschaften für Installationspakete, Transformationen und Patches werden in den folgenden Tabellen beschrieben. Beachten Sie, dass die Bedeutung einer bestimmten Zusammenfassungseigenschaft unterschiedlich sein kann, je nachdem, ob die Datenbank zu einem Installationspaket, einer Transformation oder einem Patchpaket gehört. Weitere Informationen zu den Eigenschaften-IDs, PIDs und Typen finden Sie unter [Summary Information Stream Property Set](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Installationspakete



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Summary-Eigenschaft</th>
<th>Bedeutung dieser Eigenschaft in einer Installationsdatenbank</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titel</strong></a></td>
<td>Eine Beschreibung dieser Datei als Installationspaket. Die Beschreibung sollte den Ausdruck &quot; <a href="about-the-installer-database.md">Installationsdatenbank enthalten.</a>&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Subject</strong></a></td>
<td>Der Name des produkts, das von diesem Paket installiert wird. Dies sollte der gleiche Name wie in der <a href="productname.md"><strong>ProductName-Eigenschaft</strong></a> sein.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Der Name des Herstellers dieses Produkts. Dies sollte der gleiche Name wie in der <a href="manufacturer.md"><strong>Manufacturer-Eigenschaft</strong></a> sein.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Keywords</strong></a></td>
<td>Eine Liste von Schlüsselwörtern, die von Dateibrowsern verwendet werden können, um Schlüsselwortsuchen nach einer Datei durchzuführen. Die Schlüsselwörter sollten &quot; Installer &quot; sowie produktspezifische Schlüsselwörter enthalten.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Kommentare</strong></a></td>
<td>Enthält den Ausdruck: Diese Installationsdatenbank enthält die Logik und die Daten, die zum Installieren des <&quot; <em>erforderlich sind.</em> >&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Vorlage</strong></a> (ERFORDERLICH)</td>
<td>Die Plattform und die Sprachen, die mit diesem Installationspaket kompatibel sind. Syntax <a href="template-summary.md"><strong>finden Sie</strong></a> unter Vorlage.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></td>
<td>Entwickler von Datenbankbearbeitungstools können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zu verfolgen, die die Installationsdatenbank ändert. Diese Eigenschaft sollte in einer endgültigen Versanddatenbank auf NULL festgelegt werden. Das Installationsprogramm legt diese Eigenschaft während einer Administratorinstallation auf den Wert der <a href="logonuser.md"><strong>LogonUser-Eigenschaft</strong></a> <a href="administrative-installation.md"><strong>fest.</strong></a> Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss sie nie ändern.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (ERFORDERLICH)</td>
<td>Enthält den <a href="package-codes.md">Paketcode für</a> das Installationspaket.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></td>
<td>Kann auf das Datum und <a href="administrative-installation.md"></a> die Uhrzeit während einer Administratorinstallation festgelegt werden, um zu erfassen, wann das Administrative Image erstellt wurde.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Erstellen von Uhrzeit/Datum</strong></a></td>
<td>Die Uhrzeit und das Datum, zu denen diese Installer-Datenbank erstellt wurde.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Zuletzt gespeicherte Uhrzeit/Datum</strong></a></td>
<td>Die aktuelle Systemzeit und das aktuelle Datum zu dem Zeitpunkt, zu dem die Installationsprogrammdatenbank zuletzt gespeichert wurde. Anfangs NULL.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (ERFORDERLICH)</td>
<td>Enthält einen Wert, mit dem die für dieses Installationspaket erforderliche Mindestversion des Installationsprogramms identifiziert wird. Wenn das Paket beispielsweise mindestens die Version 2.0 des Installationsprogramms erfordert, sollte diese Eigenschaft auf eine ganze Zahl von 200 festgelegt werden.
<blockquote>
[!Note]<br />
Der Wert dieser Eigenschaft muss bei <a href="64-bit-windows-installer-packages.md">64-Bit-Paketen mit 64-Bit-Windows 200 oder höher sein.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Wortanzahl</strong></a> (ERFORDERLICH)</td>
<td>Der Typ des Quelldateiimages. Wird statt der standardmäßigen Count-Eigenschaft gespeichert. Diese Eigenschaft ist ein Bitfeld. Die Werte <a href="word-count-summary.md"><strong>finden Sie im</strong></a> Thema Wortanzahl.<br/> Ab version Windows Installer 4.0 unter Windows Vista enthält diese Eigenschaft Bits, um anzugeben, ob erhöhte Berechtigungen erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Zeichenanzahl</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Erstellen einer Anwendung</strong></a></td>
<td>Enthält den Namen der Software, die zum Erstellen dieser Installationsdatenbank verwendet wird.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Security</strong></a></td>
<td>Der Wert dieser Eigenschaft sollte 2 – Empfohlen schreibgeschützt sein.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Der numerische Wert der ANSI-Codepage, der zum Anzeigen der Zusammenfassungsinformationen verwendet wird. Diese Eigenschaft muss festgelegt werden, bevor Zeichenfolgeneigenschaften in den Zusammenfassungsinformationen festgelegt werden.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformationen



| Summary-Eigenschaft                                              | Bedeutung dieser Eigenschaft in einer Transformation                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Titel**](title-summary.md)                                | Eine Beschreibung dieser Datei als Transformation. Die Beschreibung sollte den Folgenden enthalten:["Transformieren".](database-transforms.md)                                                                                                                                                                     |
| [**Subject**](subject-summary.md)                            | Der Name des Produkts, das vom ursprünglichen Installationspaket installiert wurde. Dieser Wert sollte mit dem Wert der [**Eigenschaft Betreffzusammenfassung**](subject-summary.md) im ursprünglichen Installationspaket identisch sein.                                                                                            |
| [**Autor**](author-summary.md)                              | Der Name des Herstellers dieser Transformation.                                                                                                                                                                                                                                                   |
| [**Keywords**](keywords-summary.md)                          | Eine Liste von Schlüsselwörtern, die von Dateibrowsern verwendet werden können, um Schlüsselwortsuchen nach einer Datei durchzuführen. Die Schlüsselwörter sollten "Installer" sowie produktspezifische Schlüsselwörter enthalten.                                                                                                                             |
| [**Kommentare**](comments-summary.md)                          | Enthält den Folgenden: "Diese Transformation enthält die Logik und die Daten, die zum Installieren des <*Produktnamens>."*                                                                                                                                                                                     |
| [**Vorlage**](template-summary.md) (ERFORDERLICH)               | Die Plattform- und Sprachversionen, die mit dieser Transformation kompatibel sind. Dieser Wert bleibt möglicherweise leer, wenn keine Einschränkungen gelten. Für eine Transformation kann nur eine Sprache angegeben werden. Weitere Informationen zur Syntax finden Sie unter [**Vorlage**](template-summary.md).                                |
| [**Zuletzt gespeichert von**](last-saved-by-summary.md)                | Die Plattform- und Sprach-IDs, über die die Datenbank verfügt, nachdem sie transformiert wurde. Die [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) in der neuen Datenbank sollte auf die gleichen Werte festgelegt werden.                                                                                              |
| [**Revisionsnummer**](revision-number-summary.md) (ERFORDERLICH) | Eine Liste der Produktcode-GUIDs und der Version der neuen und ursprünglichen Produkte und der Upgradecode-GUID. Die Liste wird wie folgt durch Semikolons getrennt. *Original-Product-Code Original-Product-Version*; *New-Product Code New-Product-Version*; *Upgradecode*<br/>                       |
| [**Zuletzt gedruckt**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Erstellen von Uhrzeit/Datum**](create-time-date-summary.md)          | Die Uhrzeit und das Datum, zu denen die Transformation erstellt wurde.                                                                                                                                                                                                                                                 |
| [**Zuletzt gespeicherte Uhrzeit/Datum**](last-saved-time-date-summary.md)  | Die aktuelle Systemzeit und das aktuelle Datum zu dem Zeitpunkt, zu dem die Transformation gespeichert wurde. Anfangs NULL.                                                                                                                                                                                                             |
| [**Seitenanzahl**](page-count-summary.md) (ERFORDERLICH)           | Ein -Wert, der verwendet wird, um die Mindestversion des Installationsprogramms anzugeben, die zum Verarbeiten der Transformation erforderlich ist. Der Wert sollte auf den größeren der beiden Eigenschaftswerte der Seitenanzahl festgelegt werden, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden. [](page-count-summary.md)                                 |
| [**Wortanzahl**](word-count-summary.md) (ERFORDERLICH)           | Null                                                                                                                                                                                                                                                                                              |
| [**Zeichenanzahl**](character-count-summary.md)            | Dieser Teil des Zusammenfassungsinformationsdatenstroms ist in zwei 16-Bit-Wörter unterteilt. Das obere Wort enthält [*Transformationsvalidierungsflags.*](t-gly.md) Das untere Wort enthält [*Transformationsfehlerbedingungsflags.*](t-gly.md) |
| [**Erstellen einer Anwendung**](creating-application-summary.md)  | Enthält den Namen der Software, die zum Erstellen dieser Transformation verwendet wird.                                                                                                                                                                                                                                  |
| [**Security**](security-summary.md)                          | Der Wert dieser Eigenschaft sollte 4 – Schreibgeschützt erzwungen sein.                                                                                                                                                                                                                                      |
| [**Codepage**](codepage-summary.md)                          | Der numerische Wert der ANSI-Codepage, die zum Anzeigen der Zusammenfassungsinformationen verwendet wird. Diese Eigenschaft muss festgelegt werden, bevor Zeichenfolgeneigenschaften in den Zusammenfassungsinformationen festgelegt werden können.                                                                                                                    |



 

## <a name="patch-packages"></a>Patchpakete



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Summary-Eigenschaft</th>
<th>Bedeutung dieser Eigenschaft in einem Patchpaket</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titel</strong></a></td>
<td>Eine Beschreibung dieser Datei als Patchpaket. Die Beschreibung sollte den Folgenden enthalten: &quot; <a href="patch-packages.md">Patch .</a>&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Subject</strong></a></td>
<td>Eine Beschreibung des Patches, die den Namen des Produkts enthält.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Der Name des Herstellers des Patchpakets.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Keywords</strong></a></td>
<td>Eine durch Semikolons getrennte Liste von Quellen des Patches.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Kommentare</strong></a></td>
<td>Enthält den Ausdruck: &quot; Dieser Patch enthält die Logik und die Daten, die zum Installieren <<em>Produktnamens</em>erforderlich > sind.&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Vorlage</strong></a> (ERFORDERLICH)</td>
<td>Eine durch Semikolons getrennte Liste der Produktcodes, die diesen Patch akzeptieren können.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></td>
<td>Eine durch Semikolons getrennte Liste von Transformationsunterstoragenamen in der Reihenfolge, in der sie von diesem Patch angewendet werden.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (ERFORDERLICH)</td>
<td>Enthält den GUID-Patchcode für den Patch. Darauf folgt möglicherweise eine Liste der Patchcode-GUIDs für Patches, die entfernt werden, wenn dieser Patch angewendet wird. Die Patchcodes werden ohne Trennzeichen verkettet, die GUIDs in der Liste trennen.
<blockquote>
[!Note]<br />
Wenn das Patchpaket eine <a href="msipatchsequence-table.md"><strong>MsiPatchSequence-Tabelle</strong></a> enthält, entfernt der Patch keine Patches, die nach der GUID des aktuellen Patches aufgeführt sind.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Erstellen von Uhrzeit/Datum</strong></a></td>
<td>Uhrzeit und Datum der Erstellung der Patchdatei.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Zeitpunkt/Datum des letzten Gespeicherten</strong></a></td>
<td>Die aktuelle Systemzeit und das Datum zum Zeitpunkt der Speicherung des Patchpakets. Dieser Wert ist anfänglich NULL.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (ERFORDERLICH)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Wortanzahl</strong></a> (ERFORDERLICH)</td>
<td>Enthält einen Wert, der die mindest erforderliche Windows Installer-Version angibt, um den Patch zu installieren. Ein Patch mit dem Wortzählungswert 4 erfordert Windows Installer Version 3.0 oder höher, damit der Patch angewendet werden kann. Der Wert 3 gibt an, dass Windows Installer Version 2.0 oder höher erforderlich ist. Der Wert 2 gibt an, dass Windows Installer Version 1.2 oder höher erforderlich ist. Der Standardwert ist 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Zeichenanzahl</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Erstellen einer Anwendung</strong></a></td>
<td>Der Name der Software, die zum Erstellen des Patches verwendet wird.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Security</strong></a></td>
<td>Der Wert dieser Eigenschaft sollte 4 – Schreibgeschützt erzwungen sein.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Der numerische Wert der ANSI-Codepage, die zum Anzeigen der Zusammenfassungsinformationen verwendet wird. Diese Eigenschaft muss festgelegt werden, bevor Zeichenfolgeneigenschaften in den Zusammenfassungsinformationen festgelegt werden.</td>
</tr>
</tbody>
</table>



 

 

 




