---
title: Zeichenfolgen
description: In diesem Abschnitt werden die Zeichen folgen Funktionen erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- Ressourcen, Zeichen folgen
- Zeichenfolgen
- Zeichenfolgenfunktionen (string-Funktionen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732097"
---
# <a name="strings"></a>Zeichenfolgen

In diesem Abschnitt werden die Zeichen folgen Funktionen beschrieben und erläutert, wie Sie in Ihren Anwendungen verwendet werden.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                     | BESCHREIBUNG                                             |
|------------------------------------------|---------------------------------------------------------|
| [Informationen über Zeichenfolgen](about-strings.md)       | Erläutert die Zeichen folgen Funktionen.<br/>              |
| [Informationen zu "strausafe. h"](strsafe-ovw.md)       | Erläutert die Zeichen folgen Funktionen in "strausafe. h".<br/> |
| [Zeichen folgen Verweis](string-reference.md) | Enthält die API-Referenz.<br/>                  |



 

### <a name="string-functions"></a>Zeichenfolgenfunktionen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>Charlower</strong></a></td>
<td>Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>Charlowerbuff</strong></a></td>
<td>Konvertiert Großbuchstaben in einem Puffer in Kleinbuchstaben. Die-Funktion konvertiert die Zeichen an Ort und Stelle. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>Charnext</strong></a></td>
<td>Ruft einen Zeiger auf das nächste Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>Charnextexa</strong></a></td>
<td>Ruft den Zeiger auf das nächste Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>Charprev</strong></a></td>
<td>Ruft einen Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>Charprevexa</strong></a></td>
<td>Ruft den Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>Charper OEM</strong></a></td>
<td>Übersetzt eine Zeichenfolge in den von OEM definierten Zeichensatz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>Chartoken</strong></a></td>
<td>Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge in den von OEM definierten Zeichensatz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>Charupper</strong></a></td>
<td>Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Großbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>Charupperbuff</strong></a></td>
<td>Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben. Die-Funktion konvertiert die Zeichen an Ort und Stelle. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></td>
<td>Vergleicht zwei Zeichen folgen unter Verwendung des angegebenen Gebiets Schemas.
<blockquote>
[!Note]<br />
Verwenden Sie für die Kompatibilität mit Unicode <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>comparestringex</strong></a> oder die Unicode-Version von <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>Comparestringex</strong></a></td>
<td>Vergleicht zwei Unicode-Zeichen folgen (breit Zeichen) unter Verwendung des angegebenen Gebiets Schemas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></td>
<td>Ordnet eine Zeichenfolge einer anderen zu, wobei eine angegebene Transformations Option durchgeführt wird. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>Getstringtypea</strong></a></td>
<td>Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest. Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>Getstringtypeex</strong></a></td>
<td>Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest. Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt. <br/> Im Gegensatz zu seinen close-verwandten " <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>getstringtypea</strong></a> " und " <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>getstringtypew</strong></a>" zeigt <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>getstringtypeex</strong></a> das Standardverhalten durch die Verwendung des Unicode-Schalters " <strong> # define</strong> ". Dies ist die empfohlene Funktion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>Getstringtypew</strong></a></td>
<td>Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest. Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>Ischaralpha</strong></a></td>
<td>Bestimmt, ob ein Zeichen ein alphabetisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>Ischaralpha numerisch</strong></a></td>
<td>Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>Ischarlower</strong></a></td>
<td>Bestimmt, ob ein Zeichen klein geschrieben ist. Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>Ischarupper</strong></a></td>
<td>Bestimmt, ob ein Zeichen in Großbuchstaben vorliegt. Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></td>
<td>Lädt eine Zeichen folgen Ressource aus der ausführbaren Datei, die einem angegebenen Modul zugeordnet ist, kopiert die Zeichenfolge in einen Puffer und fügt ein abschließendes NULL-Zeichen an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrincat</strong></a></td>
<td>Fügt eine Zeichenfolge an eine andere Zeichenfolge an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstraucmp</strong></a></td>
<td>Vergleicht zwei Zeichen folgen. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstraucmpi</strong></a></td>
<td>Vergleicht zwei Zeichen folgen. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrincpy</strong></a></td>
<td>Kopiert eine Zeichenfolge in einen Puffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrincpyn</strong></a></td>
<td>Kopiert eine angegebene Anzahl von Zeichen aus einer Quell Zeichenfolge in einen Puffer. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></td>
<td>Bestimmt die Länge der angegebenen Zeichenfolge (ohne das abschließende Null Zeichen).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>Oemto Char</strong></a></td>
<td>Übersetzt eine Zeichenfolge aus dem OEM-definierten Zeichensatz in eine ANSI-oder Zeichenfolge mit breit Zeichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>Oemzu charbuff</strong></a></td>
<td>Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge aus dem OEM-definierten Zeichensatz in eine ANSI-oder eine Zeichenfolge mit breit Zeichen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></td>
<td>Schreibt formatierte Daten in den angegebenen Puffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>Wvsprintf</strong></a></td>
<td>Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in den angegebenen Puffer.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a>Strauchsichere Funktionen



| Name                                             | BESCHREIBUNG                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Stringcbcat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**Stringcb-Ex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**Stringcb-n**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge zu einer anderen Zeichenfolge.<br/>         |
| [**Stringcbcr-x**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge zu einer anderen Zeichenfolge.<br/>         |
| [**Stringcbcopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**Stringcbcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**Stringcbcopyn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Kopiert die angegebene Anzahl von Bytes von einer Zeichenfolge in eine andere.<br/>                      |
| [**Stringcbcopynetx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Kopiert die angegebene Anzahl von Bytes von einer Zeichenfolge in eine andere.<br/>                      |
| [**Stringcbgets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.<br/>  |
| [**Stringcbgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.<br/>  |
| [**Stringcblength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Bestimmt, ob eine Zeichenfolge die angegebene Länge in Bytes überschreitet.<br/>                   |
| [**Stringcbprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**Stringcbprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**Stringcbvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**Stringcbvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**Stringcch| Ex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**Stringcch.**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Verkettet die angegebene Anzahl von Zeichen aus einer Zeichenfolge zu einer anderen Zeichenfolge.<br/>    |
| [**Stringcchcatcher**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Verkettet die angegebene Anzahl von Zeichen aus einer Zeichenfolge zu einer anderen Zeichenfolge.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**Stringcchcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**Stringcchcopyn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.<br/>                 |
| [**Stringcchcopynetx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.<br/>                 |
| [**Stringcchgets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.<br/>  |
| [**Stringcchgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.<br/>  |
| [**Stringcchlength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Bestimmt, ob eine Zeichenfolge die angegebene Länge in Zeichen überschreitet.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**Stringcchprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**Stringcchvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**Stringcchvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |



 

 

