---
description: In diesem Abschnitt wird erläutert, wie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellt
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Erstellen von benutzerdefinierten Wörterbüchern für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345649"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Erstellen von benutzerdefinierten Wörterbüchern für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2

In diesem Abschnitt wird erläutert, wie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellt

Im Betriebssystem Windows 7 und unter dem Betriebssystem Windows Server 2008 R2 kann die Genauigkeit der Handschrifterkennung durch die Verwendung von benutzerdefinierten Wörterbüchern erheblich verbessert werden. Diese Wörterbücher ergänzen oder ersetzen System Wörterbücher für die Handschrift. Die Unterstützung für die Handschrifterkennung wird über das Freihand-und Handschriftdienste Feature bereitgestellt, das über Server-Manager aktiviert werden muss.

> [!Note]  
> Benutzerdefinierte Wörterbücher können nur für eine Sprache installiert werden, wenn die Handschrifterkennung für diese Sprache installiert ist.

 

Es gibt zwei grundlegende Schritte zum Einrichten eines benutzerdefinierten Wörterbuchs für die Handschrift:

-   Kompilieren Sie eine Wort Liste. Die Kompilierung erstellt eine kompilierte benutzerdefinierte Wörterbuchdatei (. hwrdict).
-   Installieren Sie das kompilierte Benutzerwörterbuch.

## <a name="compiling-a-word-list"></a>Kompilieren einer Word-Liste

Die zu kompilierende Wort Liste muss im nur-Text-Format vorliegen und muss mit einer Unicode-Codierung gespeichert werden. Andere Codierungen können nicht verwendet werden. Jede Zeile der Textdatei wird als einzelner Eintrag im Wörterbuch verwendet. Multiword-Einheiten Einträge, die ein oder mehrere Leerzeichen enthalten, sind zulässig. Leerzeichen am Anfang oder Ende einer Zeile werden ignoriert.

Ein benutzerdefiniertes Wörterbuch wird von einer Befehlszeile aus kompiliert. Öffnen Sie zum Kompilieren eines Wörterbuchs ein Befehlsfenster, navigieren Sie zu dem Ordner, der die Wort Liste enthält, und führen Sie HwrComp.exe mit den Befehlszeilenoptionen aus, die Sie verwenden möchten.

Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Erklärung der Optionen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang <localename></td>
<td>Der angegebene Gebiets Schema Name, der der kompilierten benutzerdefinierten Wörterbuchdatei zugewiesen ist. Das <localename> -Argument hat die Form Language-Region. Ein Beispiel hierfür ist "en-US", das die englische Sprache in der USA Region angibt. Beispiele für dieses Formular finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen. Die folgenden Sprachen werden für Windows 7 und Windows Server 2008 R2 durch dieses Feature unterstützt: en-US, en-GB, en-ca, en-au, de-de, de-ch, fr-FR, es-es, es-MX, es-ar, IT-IT, nl-nl, NL-BE, pt-br, pt-pt, da-DK, SV-SE, nb-no, nn-no, fi-fi, PL-PL, CS-CZ, ru-ru, RO-RO, SR-LATN-CS, SR-Cyrl-CS, ca-es und HR-HR.<br/></td>
</tr>
<tr class="even">
<td>-Typ <type></td>
<td>Das Option-Argument <type> ist eine Verkettung einer einzelnen Zeichenfolge für die Verwendung der Ressource als Haupt Wort Liste (primär) oder als Ergänzung zur Haupt Wort Liste (sekundär), gefolgt von dem Namen der eigentlichen Wort Liste, auf die die Ressource angewendet wird (z. b. Wörterbuch oder Nachname). Folgende Werte sind möglich:
<ul>
<li>Primary-CityName-List</li>
<li>Primary-CountryName-List</li>
<li>Primary-countryshortname-List</li>
<li>primär-Wörterbuch</li>
<li>primär-givenName-List</li>
<li>Primary-StateOrProvince-List</li>
<li>Primary-streetname-List</li>
<li>primär-Nachname-Liste</li>
<li>Sekundär-CityName-List</li>
<li>Sekundär-CountryName-List</li>
<li>Sekundär-countryshortname-List</li>
<li>Sekundär Wörterbuch</li>
<li>Sekundär-emailsmtp-Liste</li>
<li>Sekundär-emailusername-List</li>
<li>Sekundär-givenName-List</li>
<li>Sekundär-StateOrProvince-List</li>
<li>Sekundär-streetname-List</li>
<li>Sekundär-Nachname-Liste</li>
<li>Sekundär-URL-Liste</li>
</ul>
Wenn ein Typwert mit dem Präfix Primary beginnt, wird das kompilierte Wörterbuch nach der Installation durch das System Wörterbuch für diese Sprache ersetzt. Der Wert Primary-Dictionary stellt das Hauptsystem Wörterbuch für eine Sprache dar.
<blockquote>
[!Note]<br />
Das Ersetzen eines System Wörterbuchs führt nicht zum ursprünglichen Inhalt des System Wörterbuchs, da der Austausch nur wirksam ist, bis das benutzerdefinierte Wörterbuch entfernt wurde.
</blockquote>
<br/> Wenn ein Typwert mit dem Präfix Sekundär beginnt, ergänzt das kompilierte Wörterbuch Das System Wörterbuch, ohne es zu ersetzen.</td>
</tr>
<tr class="odd">
<td>-Kommentar <comment></td>
<td>Der angegebene Kommentar wird in die Wörterbuchdatei kompiliert. Der Kommentar muss eine einzelne Zeichenfolge und nicht länger als 64 Zeichen sein.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>Die Ausgabe wird in den Dateinamen geschrieben, der durch angegeben wird <dictfile.hwrdict> .<br/> Wenn diese Option fehlt, wird der Name der Ausgabedatei vom ursprünglichen Eingabe Dateinamen abgeleitet, wobei die Eingabedatei Erweiterung durch. hwrdict ersetzt wurde.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Standardeinstellungen

Wenn keine Parameter angegeben werden, lauten die Standard Optionswerte

-lang <current input language> -Typ Sekundär-Wörterbuch

### <a name="examples"></a>Beispiele

Im folgenden wird die Eingabedatei mylist1.txt kompiliert, die Standard Optionswerte angewendet und die Ausgabedatei mylist1. hwrdict erstellt.

``` syntax
hwrcomp mylist1.txt
```

Im Gegensatz dazu kompiliert der folgende mylist1.txt in myrsrc1. hwrdict, weist jedoch "English (US)" (en-US) als Sprache und das sekundäre Wörterbuch als Typ zu.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Installieren eines kompilierten Benutzer Wörterbuchs

HwrComp.exe erstellt eine hwrdict-Datei, die in einem Binärformat vorliegt, das von einer Handschrifterkennung verwendet werden kann. Diese Datei kann auf jedem Computer installiert werden, auf dem Windows 7 oder Windows Server 2008 R2 ausgeführt wird und der die Handschrifterkennung unterstützt. Ein Wörterbuch wird entweder nur für den aktuellen Benutzer oder für alle Benutzer auf einem Computer installiert.

Eine kompilierte benutzerdefinierte Wörterbuchdatei kann über die Befehlszeile mit dem Tool HwrReg.exe installiert werden. Dieses Tool ist nützlich, wenn Sie einige der Konfigurationswerte außer Kraft setzen möchten, die in die Datei kompiliert werden, oder die Standardwerte sind. Es gibt zwei Möglichkeiten, HwrReg.exe auszuführen: im Modus "überprüfen/installieren" und im Listen-/Entfernungs Modus.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Ausführen von HwrReg.exe im Modus "überprüfen/installieren"

Dieser Modus ist für benutzerdefinierte Wörterbuchdateien vorgesehen, die noch nicht installiert wurden. Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Erklärung der Optionen



| Parameter                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -Überprüfen                   | Die Wörterbuchdatei wird überprüft, ohne installiert zu werden. Die Option "Check" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden. Diese Option ist nützlich, um Registrierungsinformationen vor der Installation zu überprüfen. <br/> Wenn diese Option fehlt, installiert HwrReg.exe das benutzerdefinierte Wörterbuch.<br/>  |
|  Wochen <localename> | Die Wörterbuchdatei wird überprüft, ohne installiert zu werden. Die Option "Check" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden. Diese Option ist nützlich, um Registrierungsinformationen vor der Installation zu überprüfen. <br/> Wenn diese Option fehlt, installiert HwrReg.exe das benutzerdefinierte Wörterbuch. <br/> |
|  Bereich "{All \| Me}"         | Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (Bereich "Me") installiert. Die Installation mit dem Bereich "All" erfordert, dass der Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben. <br/> Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer beschränkt.<br/>                          |
|  noprompt                | HwrReg.exe wird nicht zur Bestätigung aufgefordert. Dies kann nützlich sein, wenn hwrReg.exe aus einem Skript ausgeführt wird. <br/>                                                                                                                                                                                                                                                                 |



 

Im folgenden Beispiel wird das benutzerdefinierte Wörterbuch myrsrc1. hwrdict für die Sprache "Danish (Dänemark)" (da DK) mit dem Standardbereich nur des aktuellen Benutzers installiert.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Ausführen von HwrReg.exe im Listen-/Entfernungs Modus

In diesem Modus werden installierte benutzerdefinierte Wörterbücher aufgelistet oder entfernt. Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Erklärung der Optionen



| Parameter                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  Wochen <localename> | Die Wörterbücher, die nur für diesen Gebiets Schema Namen registriert sind, werden aufgelistet oder entfernt. Das-Argument <localename> hat den Formular Sprachbereich. Beispiele für dieses Formular finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen. <br/> Wenn diese Option fehlt, werden Wörterbücher für alle Sprachen aufgelistet oder entfernt.<br/> |
|  Bereich "{All \| Me}"         | Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (Bereich "Me") installiert. Die Installation mit dem Bereich "All" erfordert, dass der Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben. <br/> Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer beschränkt.<br/>                      |
|  Sorte <type>       | Listet oder entfernt nur Wörterbücher, die mit dem angegebenen Typ registriert sind.<br/> Wenn diese Option fehlt, werden alle Wörterbuchtypen aufgelistet oder entfernt. Das Installieren oder Entfernen eines Benutzer Wörterbuchs eines anderen Typs (z. b. Primary-CountryName-List) kann die Handschrifterkennung in anderen Kontexten beeinträchtigen. <br/>                                              |
|  list                    | Listet alle installierten Wörterbücher auf, die den anderen Optionen entsprechen.<br/> Wenn diese Option fehlt, muss die Option remove angegeben werden.<br/>                                                                                                                                                                                                                          |
|  remove                  | Fordert zum Entfernen eines beliebigen Wörterbuchs auf, das mit den anderen Optionen übereinstimmt.<br/> Wenn diese Option fehlt, muss die Optionsliste angegeben werden.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Beispiele

Im folgenden finden Sie Wörterbücher mit der Sprache "English (US)" (en US) und dem primären Wörterbuch "Typ", die nur für den aktuellen Benutzer installiert werden.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Ebenso werden mit dem folgenden Wörterbücher entfernt, die denselben Kriterien entsprechen.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Allgemeine Hinweise zu benutzerdefinierten Wörterbüchern

-   Wenn Sie zwei benutzerdefinierte Wörterbücher mit dem gleichen Typ, der gleichen Sprache und dem gleichen Gültigkeitsbereich installieren, wird die erste Installation durch die zweite Installation überschrieben.
-   Wenn Sie zwei benutzerdefinierte Wörterbücher mit demselben Typ und derselben Sprache installieren, aber mit unterschiedlichen Bereichen (eines für alle Benutzer und eines für den aktuellen Benutzer), hat das für den aktuellen Benutzer installierte Wörterbuch Vorrang, und das für alle Benutzer installierte Wörterbuch wird ignoriert.

 

