---
description: In diesem Abschnitt wird erläutert, wie Sie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellen.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Erstellen benutzerdefinierter Wörterbücher für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c7b27fbb03897b406609590420bd8b69b7ceee
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631195"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Erstellen benutzerdefinierter Wörterbücher für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2

In diesem Abschnitt wird erläutert, wie Sie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellen.

Im Windows 7- und Windows Server 2008 R2-Betriebssystem kann die Genauigkeit der Handschrifterkennung durch die Verwendung benutzerdefinierter Wörterbücher erheblich verbessert werden. Diese Wörterbücher ergänzen oder ersetzen Systemwörterbücher, die für die Handschrift verwendet werden. Unterstützung für die Handschrifterkennung wird über das Freihand- und Handschriftdienste bereitgestellt, das über die Server-Manager.

> [!Note]  
> Benutzerdefinierte Wörterbücher können nur für eine Sprache installiert werden, wenn die Handschrifterkennung für diese Sprache installiert ist.

 

Es gibt zwei grundlegende Schritte zum Einrichten eines benutzerdefinierten Wörterbuchs für die Handschrift:

-   Kompilieren Sie eine Wortliste. Die Kompilierung erstellt eine kompilierte benutzerdefinierte Wörterbuchdatei (.hwrdict).
-   Installieren Sie das kompilierte benutzerdefinierte Wörterbuch.

## <a name="compiling-a-word-list"></a>Kompilieren einer Wortliste

Die zu kompilierende Wortliste muss im Nur-Text-Format vorliegen und sollte mithilfe einer Unicode-Codierung gespeichert werden. Andere Codierungen funktionieren nicht. Jede Zeile der Textdatei wird als einzelner Eintrag im Wörterbuch verwendet. Einträge für Multiwordeinheiten, die einen oder mehrere Leerzeichen enthalten, sind zulässig. Leerzeichen am Anfang oder Ende einer Zeile werden ignoriert.

Ein benutzerdefiniertes Wörterbuch wird über eine Befehlszeile kompiliert. Öffnen Sie zum Kompilieren eines Wörterbuchs ein Befehlsfenster, navigieren Sie zu dem Ordner, der die Wortliste enthält, und führen Sie dann HwrComp.exe mit den Befehlszeilenoptionen aus, die Sie verwenden möchten.

Das folgende Beispiel zeigt die Verwendungssyntax für die Befehlszeilenoptionen.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Erläuterung der Optionen



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang <localename></td>
<td>Der angegebene Name des der kompilierten benutzerdefinierten Wörterbuchdatei zugewiesenen Locale. Das Argument <localename> hat das Formular language-REGION. Ein Beispiel hierfür ist en-US, das die englische Sprache in der region USA bezeichnet. Beispiele für dieses Formular finden Sie unter [Sprachbezeichnerkonst konstanten und Zeichenfolgen](/windows/desktop/Intl/language-identifier-constants-and-strings). Die folgenden Sprachen werden für Windows 7 und Windows Server 2008 R2 von diesem Feature unterstützt: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-PT, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES und hr-HR.<br/></td>
</tr>
<tr class="even">
<td>-type <type></td>
<td>Das Optionsargument ist eine Einzelne-Zeichenfolge-Verkettung der Verwendung der Ressource als Hauptwortliste (PRIMARY) oder als Ergänzung zur Hauptwortliste (SECONDARY), gefolgt vom tatsächlichen Namen der Wortliste, auf die die Ressource angewendet wird (z. B. DICTIONARY oder <type> SURNAME). Folgende Werte sind möglich:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>PRIMARY-DICTIONARY</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-SURNAME-LIST</li>
<li>SECONDARY-CITYNAME-LIST</li>
<li>SECONDARY-COUNTRYNAME-LIST</li>
<li>SECONDARY-COUNTRYSHORTNAME-LIST</li>
<li>SECONDARY-DICTIONARY</li>
<li>SECONDARY-EMAILSMTP-LIST</li>
<li>SECONDARY-EMAILUSERNAME-LIST</li>
<li>SECONDARY-GIVENNAME-LIST</li>
<li>SECONDARY-STATEORPROVINCE-LIST</li>
<li>SECONDARY-STREETNAME-LIST</li>
<li>SECONDARY-SURNAME-LIST</li>
<li>SECONDARY-URL-LIST</li>
</ul>
Wenn ein Typwert mit dem Präfix PRIMARY beginnt, ersetzt das kompilierte Wörterbuch nach seiner Installation das Systemwörterbuch für diese Sprache. Der Wert PRIMARY-DICTIONARY stellt das Hauptsystemwörterbuch für eine Sprache dar.
<blockquote>
[!Note]<br />
Das Ersetzen eines Systemwörterbuchs hat keine Auswirkungen auf den ursprünglichen Systemwörterbuchinhalt, da die Ersetzung nur wirksam ist, bis das benutzerdefinierte Wörterbuch entfernt wurde.
</blockquote>
<br/> Wenn ein Typwert mit dem Präfix SECONDARY beginnt, ergänzt das kompilierte Wörterbuch das Systemwörterbuch, ohne es zu ersetzen.</td>
</tr>
<tr class="odd">
<td>-comment <comment></td>
<td>Der angegebene Kommentar wird in die Wörterbuchdatei kompiliert. Der Kommentar muss eine einzelne Zeichenfolge sein und darf nicht länger als 64 Zeichen sein.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>Die Ausgabe wird in den durch angegebenen Dateinamen <dictfile.hwrdict> geschrieben.<br/> Wenn diese Option fehlt, wird der Name der Ausgabedatei vom ursprünglichen Eingabedateinamen abgeleitet, und die Eingabedateierweiterung wird durch .hwrdict ersetzt.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Standardeinstellungen

Wenn keine Parameter angegeben werden, sind die Standardoptionswerte

-lang <current input language> -type SECONDARY-DICTIONARY

### <a name="examples"></a>Beispiele

Im Folgenden wird die Eingabedatei mylist1.txt kompiliert, die Standardwerte der Option angewendet und die Ausgabedatei mylist1.hwrdict erstellt.

``` syntax
hwrcomp mylist1.txt
```

Im Gegensatz dazu kompiliert der folgende mylist1.txt in myrsrc1.hwrdict, weist jedoch "English (US)" (en-US) als Sprache und SECONDARY-DICTIONARY als Typ zu.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Installieren eines kompilierten benutzerdefinierten Wörterbuchs

HwrComp.exe erstellt eine HWRDICT-Datei in einem Binärformat, das von einer Handschrifterkennung verwendet werden kann. Diese Datei kann auf jedem Computer mit Windows 7 oder Windows Server 2008 R2 installiert werden, der die Handschrifterkennung unterstützt. Ein Wörterbuch wird entweder nur für den aktuellen Benutzer oder für alle Benutzer auf einem Computer installiert.

Eine kompilierte benutzerdefinierte Wörterbuchdatei kann über die Befehlszeile mithilfe des Tools installiert HwrReg.exe. Dieses Tool ist nützlich, wenn Sie einige der Konfigurationswerte überschreiben möchten, die entweder in die Datei kompiliert werden oder die Standardwerte sind. Es gibt zwei Möglichkeiten zum Ausführen von HwrReg.exe: im Check/Install-Modus und im Listen-/Entfernungsmodus.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Ausführen HwrReg.exe im Check/Install-Modus

Dieser Modus gilt für benutzerdefinierte Wörterbuchdateien, die noch nicht installiert wurden. Im Folgenden wird die Verwendungssyntax für die Befehlszeilenoptionen veranschaulicht.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Erläuterung der Optionen



| Parameter                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -check                   | Die Wörterbuchdatei wird überprüft, ohne installiert zu werden. Die Option "Überprüfen" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden. Diese Option ist nützlich, um Registrierungsinformationen zu überprüfen, bevor die Installation ausgeführt wird. <br/> Wenn diese Option fehlt, HwrReg.exe das benutzerdefinierte Wörterbuch installiert.<br/>  |
|  lang <localename> | Die Wörterbuchdatei wird überprüft, ohne installiert zu werden. Die Option "Überprüfen" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden. Diese Option ist nützlich, um Registrierungsinformationen zu überprüfen, bevor die Installation ausgeführt wird. <br/> Wenn diese Option fehlt, HwrReg.exe das benutzerdefinierte Wörterbuch installiert. <br/> |
|  scope {all \| me}         | Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (bereich mich) installiert. Für die Installation mit scope all muss der Befehl in einer Eingabeaufforderung mit erhöhten Rechten ausgeführt werden. Andernfalls wird ein Fehlercode zurückgegeben. <br/> Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer ausdingt.<br/>                          |
|  noprompt                | HwrReg.exe wird nicht zur Bestätigung aufgefordert. Dies kann nützlich sein, wenn sie hwrReg.exe Skripts ausführen. <br/>                                                                                                                                                                                                                                                                 |



 

Im folgenden Beispiel wird das benutzerdefinierte Wörterbuch myrsrc1.hwrdict für die Sprache "Dänisch (Spanien)" (da DK) mit dem Standardbereich nur des aktuellen Benutzers installiert.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Ausführen HwrReg.exe im Listen-/Entfernungsmodus

In diesem Modus werden installierte benutzerdefinierte Wörterbücher entweder aufgeführt oder entfernt. Im Folgenden wird die Verwendungssyntax für die Befehlszeilenoptionen veranschaulicht.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Erläuterung der Optionen



| Parameter                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang <localename> | Die Wörterbücher, die nur für diesen Namen registriert sind, werden aufgelistet oder entfernt. Das Argument <localename> hat die Formsprache REGION. Beispiele für dieses Formular finden Sie unter [Sprachbezeichnerkonst konstanten und Zeichenfolgen](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Wenn diese Option fehlt, werden Wörterbücher für alle Sprachen aufgelistet oder entfernt.<br/> |
|  scope {all \| me}         | Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (bereich mich) installiert. Für die Installation mit scope all muss der Befehl in einer Eingabeaufforderung mit erhöhten Rechten ausgeführt werden. Andernfalls wird ein Fehlercode zurückgegeben. <br/> Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer ausdingt.<br/>                      |
|  Typ <type>       | Listet oder entfernt nur Wörterbücher, die mit dem angegebenen Typ registriert sind.<br/> Wenn diese Option fehlt, werden alle Wörterbuchtypen aufgelistet oder entfernt. Das Installieren oder Entfernen eines benutzerdefinierten Wörterbuchs eines anderen Typs (z. B. PRIMARY-COUNTRYNAME-LIST) kann sich auf die Handschrifterkennung in anderen Kontexten auswirken. <br/>                                              |
|  list                    | Listet alle installierten Wörterbücher auf, die mit den anderen Optionen übereinstimmen.<br/> Wenn diese Option fehlt, muss die Option remove angegeben werden.<br/>                                                                                                                                                                                                                          |
|  remove                  | Fordert zum Entfernen eines Wörterbuchs auf, das den anderen Optionen entspricht.<br/> Wenn diese Option fehlt, muss die Optionsliste angegeben werden.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Beispiele

Im Folgenden werden Wörterbücher mit der Sprache "Englisch (US)" (en US) und dem Typ PRIMARY DICTIONARY aufgeführt, die nur für den aktuellen Benutzer installiert sind.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Auf ähnliche Weise werden wörterbücher entfernt, die denselben Kriterien entsprechen.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Allgemeine Hinweise zu benutzerdefinierten Wörterbüchern

-   Wenn Sie zwei benutzerdefinierte Wörterbücher installieren, die denselben Typ, die gleiche Sprache und denselben Bereich haben, überschreibt die zweite Installation das erste.
-   Wenn Sie zwei benutzerdefinierte Wörterbücher mit demselben Typ und derselben Sprache, aber mit unterschiedlichen Bereichen (eines für alle Benutzer und eines für den aktuellen Benutzer) installieren, hat das für den aktuellen Benutzer installierte Wörterbuch Vorrang, und das für alle Benutzer installierte Wörterbuch wird ignoriert.

 

