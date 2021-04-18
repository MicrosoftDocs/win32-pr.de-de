---
description: In den folgenden Tabellen werden die Zusammenfassungs Eigenschaften für Installationspakete, Transformationen und Patches beschrieben.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Beschreibungen der Zusammenfassungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352552"
---
# <a name="summary-property-descriptions"></a>Beschreibungen der Zusammenfassungs Eigenschaften

In den folgenden Tabellen werden die Zusammenfassungs Eigenschaften für Installationspakete, Transformationen und Patches beschrieben. Beachten Sie, dass die Bedeutung einer bestimmten Zusammenfassungs Eigenschaft je nachdem, ob die Datenbank zu einem Installationspaket, einer Transformation oder einem Patchpaket gehört, unterschiedlich sein kann. Weitere Informationen zu den Eigenschaften-IDs, PIDs und Typen finden Sie unter [Summary Information Stream-Eigenschaften Satz](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Installationspakete



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Summary-Eigenschaft</th>
<th>Bedeutung dieser Eigenschaft in einer Installations Datenbank</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titel</strong></a></td>
<td>Eine Beschreibung dieser Datei als Installationspaket. Die Beschreibung sollte den Begriff &quot; <a href="about-the-installer-database.md">Installations Datenbank</a>enthalten.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Subject</strong></a></td>
<td>Der Name des Produkts, das von diesem Paket installiert wird. Dabei sollte es sich um den gleichen Namen wie in der <a href="productname.md"><strong>ProductName</strong></a> -Eigenschaft handeln.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Der Name des Herstellers dieses Produkts. Dabei sollte es sich um den gleichen Namen wie in der <a href="manufacturer.md"><strong>Hersteller</strong></a> Eigenschaft handeln.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Keywords</strong></a></td>
<td>Eine Liste von Schlüsselwörtern, die von Datei Browsern verwendet werden können, um nach einer Datei zu suchen. Die Schlüsselwörter sollten &quot; &quot; sowohl Installer als auch produktspezifische Schlüsselwörter enthalten.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Kommentare</strong></a></td>
<td>Enthält den Ausdruck: &quot; Diese Installerdatenbank enthält die Logik und die Daten, die erforderlich sind, um <<em>Produktnamen</em>zu installieren > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Vorlage</strong></a> (erforderlich)</td>
<td>Die Plattform und die Sprachen, die mit diesem Installationspaket kompatibel sind. Die Syntax finden Sie unter <a href="template-summary.md"><strong>Template</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></td>
<td>Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen. Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden. Diese Eigenschaft wird von dem Installer während einer <a href="administrative-installation.md"><strong>administrativen Installation</strong></a>auf den Wert der <a href="logonuser.md"><strong>LogonUser</strong></a> -Eigenschaft festgelegt. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (erforderlich)</td>
<td>Enthält den <a href="package-codes.md">Paket Code</a> für das Installer-Paket.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></td>
<td>Kann auf das Datum und die Uhrzeit während einer <a href="administrative-installation.md">administrativen Installation</a> festgelegt werden, um aufzuzeichnen, wann das administrative Image erstellt wurde.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Uhrzeit/Datum erstellen</strong></a></td>
<td>Das Datum und die Uhrzeit, zu der die Installer-Datenbank erstellt wurde.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Letzte gespeicherte Uhrzeit/Datum</strong></a></td>
<td>Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der letzten Speicherung der Installer-Datenbank. Anfänglich NULL.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (erforderlich)</td>
<td>Enthält einen Wert, der verwendet wird, um die für dieses Installationspaket erforderliche mindestinstallerversion zu identifizieren. Wenn das Paket z. b. mindestens die Version 2,0 des Installers erfordert, sollte diese Eigenschaft auf eine ganze Zahl 200 festgelegt werden.
<blockquote>
[!Note]<br />
Der Wert dieser Eigenschaft muss bei <a href="64-bit-windows-installer-packages.md">64-Bit-Windows Installer Paketen</a>200 oder größer sein.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> (erforderlich)</td>
<td>Der Typ des Quelldatei Bilds. Wird anstelle der Standard Count-Eigenschaft gespeichert. Diese Eigenschaft ist ein Bitfeld. Die Werte finden Sie im Thema <a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> .<br/> Ab Windows Installer Version 4,0 unter Windows Vista schließt diese Eigenschaft Bits ein, um anzugeben, ob erhöhte Rechte erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Zeichen Anzahl</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Anwendung wird erstellt</strong></a></td>
<td>Enthält den Namen der Software, mit der diese Installations Datenbank erstellt wird.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicherheit</strong></a></td>
<td>Der Wert dieser Eigenschaft sollte "2-empfohlen" lauten.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen. Diese Eigenschaft muss festgelegt werden, bevor alle Zeichen folgen Eigenschaften in den Zusammenfassungs Informationen festgelegt werden.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformationen



| Summary-Eigenschaft                                              | Bedeutung dieser Eigenschaft in einer Transformation                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Titel**](title-summary.md)                                | Eine Beschreibung dieser Datei als Transformation. Die Beschreibung sollte den folgenden Ausdruck enthalten: "[Transform](database-transforms.md)".                                                                                                                                                                     |
| [**Subject**](subject-summary.md)                            | Der Name des Produkts, das vom ursprünglichen Installationspaket installiert wurde. Dabei sollte es sich um den gleichen Wert wie die Eigenschaft " [**betreffzusammenfassung**](subject-summary.md) " im ursprünglichen Installationspaket handeln.                                                                                            |
| [**Autor**](author-summary.md)                              | Der Name des Herstellers dieser Transformation.                                                                                                                                                                                                                                                   |
| [**Keywords**](keywords-summary.md)                          | Eine Liste von Schlüsselwörtern, die von Datei Browsern verwendet werden können, um nach einer Datei zu suchen. Die Schlüsselwörter sollten "Installer" und produktspezifische Schlüsselwörter enthalten.                                                                                                                             |
| [**Kommentare**](comments-summary.md)                          | Enthält den folgenden Ausdruck: "Diese Transformation enthält die Logik und die Daten, die für die Installation <*Produkt namens*> erforderlich sind."                                                                                                                                                                                     |
| [**Vorlage**](template-summary.md) (erforderlich)               | Die Plattform-und Sprachversionen, die mit dieser Transformation kompatibel sind. Wenn keine Einschränkungen vorliegen, wird dieser Wert möglicherweise leer gelassen. Für eine Transformation kann nur eine Sprache angegeben werden. Weitere Informationen zur Syntax finden Sie unter [**Template**](template-summary.md).                                |
| [**Zuletzt gespeichert von**](last-saved-by-summary.md)                | Die Plattform-und Sprach-IDs, die die Datenbank nach dem Transformieren hat. Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft in der neuen Datenbank sollte auf die gleichen Werte festgelegt werden.                                                                                              |
| [**Revisionsnummer**](revision-number-summary.md) (erforderlich) | Eine Liste der Produktcode-GUIDs und-Versionen der neuen und ursprünglichen Produkte sowie der UpgradeCode-GUID. Die Liste wird wie folgt durch Semikolons getrennt. *Original-Product-Code Original-Product-Version*; *New-Product Code New-Product-Version*; *UpgradeCode*<br/>                       |
| [**Zuletzt gedruckt**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Uhrzeit/Datum erstellen**](create-time-date-summary.md)          | Das Datum und die Uhrzeit der Erstellung der Transformation.                                                                                                                                                                                                                                                 |
| [**Letzte gespeicherte Uhrzeit/Datum**](last-saved-time-date-summary.md)  | Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der Speicherung der Transformation. Anfänglich NULL.                                                                                                                                                                                                             |
| [**Seitenanzahl**](page-count-summary.md) (erforderlich)           | Ein-Wert, mit dem die für die Verarbeitung der Transformation erforderliche mindestinstallerversion angegeben wird. Der Wert sollte auf die größere der beiden Eigenschaften Werte der [**Seitenanzahl**](page-count-summary.md) festgelegt werden, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden.                                 |
| [**Wort Anzahl**](word-count-summary.md) (erforderlich)           | Null                                                                                                                                                                                                                                                                                              |
| [**Zeichen Anzahl**](character-count-summary.md)            | Dieser Teil des Zusammenfassungs Informationsdaten Stroms ist in 2 16-Bit-Wörter unterteilt. Das obere Wort enthält [*Transformations-Validierungsflags*](t-gly.md). Das untere Wort enthält [*Transformations fehlerbedingungs-Flags*](t-gly.md). |
| [**Anwendung wird erstellt**](creating-application-summary.md)  | Enthält den Namen der Software, die zum Erstellen dieser Transformation verwendet wurde.                                                                                                                                                                                                                                  |
| [**Sicherheit**](security-summary.md)                          | Der Wert dieser Eigenschaft sollte 4-erzwungen lauten.                                                                                                                                                                                                                                      |
| [**Codepage**](codepage-summary.md)                          | Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen. Diese Eigenschaft muss festgelegt werden, bevor in den Zusammenfassungs Informationen Zeichen folgen Eigenschaften festgelegt werden können.                                                                                                                    |



 

## <a name="patch-packages"></a>Patch-Pakete



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Eine Beschreibung dieser Datei als Patchpaket. Die Beschreibung sollte den folgenden Ausdruck enthalten: &quot; <a href="patch-packages.md">Patch</a>.&quot;</td>
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
<td>Eine durch Semikolons getrennte Liste der Quellen des Patches.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Kommentare</strong></a></td>
<td>Enthält den Ausdruck: &quot; dieser Patch enthält die Logik und die Daten, die erforderlich sind, um <<em>Produktnamen</em>zu installieren > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Vorlage</strong></a> (erforderlich)</td>
<td>Eine durch Semikolons getrennte Liste der Produktcodes, die diesen Patch annehmen können.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></td>
<td>Eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (erforderlich)</td>
<td>Enthält den GUID-Patchcode für den Patch. Auf diese kann eine Liste von Patchcode-GUIDs für Patches folgen, die beim Anwenden dieses Patches entfernt werden. Die Patchcodes werden ohne Trennzeichen verkettet, in denen GUIDs in der Liste getrennt sind.
<blockquote>
[!Note]<br />
Wenn das Patchpaket eine <a href="msipatchsequence-table.md"><strong>msipatchsequence</strong></a> -Tabelle enthält, entfernt der Patch keine Patches, die nach der GUID des aktuellen Patches aufgeführt sind.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Uhrzeit/Datum erstellen</strong></a></td>
<td>Das Datum und die Uhrzeit der Erstellung der Patchdatei.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Letzte gespeicherte Uhrzeit/Datum</strong></a></td>
<td>Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der Speicherung des Patchpakets. Dieser Wert ist anfänglich NULL.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (erforderlich)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> (erforderlich)</td>
<td>Enthält einen Wert, der die minimale Windows Installer Version angibt, die für die Installation des Patches erforderlich ist. Für einen Patch mit einem Wort Zähl Wert von 4 ist Windows Installer Version 3,0 oder höher erforderlich, damit der Patch angewendet werden muss. Der Wert 3 gibt an, dass Windows Installer Version 2,0 oder höher erforderlich ist. Der Wert 2 gibt an, dass Windows Installer Version 1,2 oder höher erforderlich ist. Der Standardwert ist 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Zeichen Anzahl</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Anwendung wird erstellt</strong></a></td>
<td>Der Name der zum Erstellen des Patches verwendeten Software.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicherheit</strong></a></td>
<td>Der Wert dieser Eigenschaft sollte 4-erzwungen lauten.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen. Diese Eigenschaft muss festgelegt werden, bevor alle Zeichen folgen Eigenschaften in den Zusammenfassungs Informationen festgelegt werden.</td>
</tr>
</tbody>
</table>



 

 

 




