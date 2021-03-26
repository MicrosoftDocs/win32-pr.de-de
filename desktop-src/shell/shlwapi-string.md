---
description: In diesem Abschnitt werden die Funktionen der Zeichen folgen Behandlung in Windows Shell beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Verarbeitungsfunktionen für shellzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960584"
---
# <a name="shell-string-handling-functions"></a>Verarbeitungsfunktionen für shellzeichenfolgen

In diesem Abschnitt werden die Funktionen der Zeichen folgen Behandlung in Windows Shell beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>Chrcmpi</strong></a><br/></td>
<td>Führt einen Vergleich zwischen zwei Zeichen aus. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>Getakzeptlanguages</strong></a><br/></td>
<td>Ruft beim Angeben von Spracheinstellungen eine Zeichenfolge ab, die mit Websites verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>Intlstreqn</strong></a><br/></td>
<td>Führt einen Vergleich der angegebenen Anzahl von Zeichen ab dem Anfang von zwei lokalisierten Zeichen folgen unter Beachtung der Groß-und Kleinschreibung durch.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>Intlstreqni</strong></a><br/></td>
<td>Führt einen Vergleich der angegebenen Anzahl von Zeichen vom Anfang zweier lokalisierter Zeichen folgen ohne Beachtung der Groß-/Kleinschreibung aus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>Intlstreqworker</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier lokalisierter Zeichen folgen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>Ischarspace</strong></a><br/></td>
<td>Bestimmt, ob ein Zeichen ein Leerzeichen darstellt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>Shloadderetstring</strong></a><br/></td>
<td>Extrahiert eine angegebene Text Ressource, wenn diese Ressource in Form einer indirekten Zeichenfolge angegeben wird (eine Zeichenfolge, die mit dem Symbol "@" beginnt).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>Shstraudup</strong></a><br/></td>
<td>Erstellt eine Kopie einer Zeichenfolge in neu zugewiesener Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br/></td>
<td>Fügt eine Zeichenfolge an eine andere Zeichenfolge an. <br/>
<blockquote>
[!Note]<br />
Darf nicht verwendet werden. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>Strauch</strong></a><br/></td>
<td>Kopiert Zeichen aus einer Zeichenfolge und fügt Sie an das Ende einer anderen Zeichenfolge an. <br/>
<blockquote>
[!Note]<br />
Darf nicht verwendet werden. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>"Erw"</strong></a><br/></td>
<td>Verkettet zwei Unicode-Zeichen folgen. Wird verwendet, wenn wiederholte Verkettungen desselben Puffers erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das mit dem angegebenen Zeichen übereinstimmt. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>Strauch</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das mit dem angegebenen Zeichen übereinstimmt. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>"Straume"</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>"Strauchrnw"</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br/></td>
<td>Vergleicht zwei Zeichen folgen, um zu bestimmen, ob Sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>"Straume"</strong></a><br/></td>
<td>Vergleicht Zeichen folgen mithilfe von C-Lauf Zeit Sortierregeln (ASCII). Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br/></td>
<td>Vergleicht zwei Zeichen folgen, um zu bestimmen, ob Sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>"Straucmpic"</strong></a><br/></td>
<td>Vergleicht zwei Zeichen folgen mithilfe von C-Lauf Zeit Sortierregeln (ASCII). Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>"Straucmplogicalw"</strong></a><br/></td>
<td>Vergleicht zwei Unicode-Zeichen folgen. Ziffern in den Zeichen folgen werden als numerischer Inhalt anstelle von Text betrachtet. Bei diesem Test wird keine Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>"Straun"</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob diese identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung beachtet. Das " <strong>strinncmp</strong> "-Makro unterscheidet sich nur in "Name".<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>"Strauch"</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen ab dem Anfang von zwei Zeichen folgen mithilfe von C-Lauf Zeit Regeln (ASCII). Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>"Straucmpni"</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob diese identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt. Das " <strong>strauncmpi</strong> "-Makro unterscheidet sich nur in "Name".<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>"Straucmpnic"</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen ab dem Anfang von zwei Zeichen folgen mithilfe von C-Lauf Zeit Regeln (ASCII). Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br/></td>
<td>Kopiert eine Zeichenfolge in eine andere. <br/>
<blockquote>
[!Note]<br />
Darf nicht verwendet werden. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>"Straucpyn"</strong></a><br/></td>
<td>Kopiert eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge in eine andere.<br/>
<blockquote>
[!Note]<br />
Verwenden Sie diese Funktion oder das " <strong>strinncpy</strong> "-Makro nicht. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer beliebigen Gruppe von Zeichen. Bei der Suchmethode wird die Groß-/Kleinschreibung beachtet, und das abschließende <strong>null</strong> -Zeichen ist innerhalb der Suchmuster Übereinstimmung enthalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>"Straucspni"</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer beliebigen Gruppe von Zeichen. Bei der Suchmethode wird die Groß-/Kleinschreibung nicht beachtet, und das abschließende <strong>null</strong> -Zeichen ist innerhalb der Suchmuster Übereinstimmung enthalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br/></td>
<td>Dupliziert eine Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br/></td>
<td>Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>"Straume"</strong></a><br/></td>
<td>Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird. Unterscheidet sich von " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>stuformatbytesizew</strong></a> " in einem Parametertyp.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>"Straume"</strong></a><br/></td>
<td>Konvertiert einen numerischen Wert abhängig von der Größe in eine Zeichenfolge, die die Zahl in Byte, Kilobyte, Megabyte oder Gigabyte darstellt. Erweitert <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>strformatbytesizew</strong></a> durch die Option zum Runden auf die nächste angezeigte Ziffer oder zum verwerfen nicht angezeigter Ziffern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>"Strintesizew"</strong></a><br/></td>
<td>Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird. Unterscheidet sich von " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>stuformatbytesizea</strong></a> " in einem Parametertyp.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>"Straubgröße"</strong></a><br/></td>
<td>Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die in Kilobyte als Größen Wert ausgedrückt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>"Strauch"</strong></a><br/></td>
<td>Konvertiert ein Zeitintervall, das in Millisekunden angegeben ist, in eine Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>Strisintlequal</strong></a><br/></td>
<td>Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob Sie gleich sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br/></td>
<td>Fügt eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge an das Ende einer anderen Zeichenfolge an. <br/>
<blockquote>
[!Note]<br />
Verwenden Sie diese Funktion oder das- <strong>Makro nicht</strong> . Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines in einem angegebenen Puffer enthaltenen Zeichens. Diese Suche umfasst nicht das abschließende Null Zeichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>"Strinrchri"</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>"Straurbstr"</strong></a><br/></td>
<td>Akzeptiert eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>-Struktur, die eine Zeichen</strong></a> Folge enthält, oder verweist auf eine Zeichenfolge und gibt diese Zeichenfolge als <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>"Stringebuf"</strong></a><br/></td>
<td>Konvertiert eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strauch</strong></a> Struktur in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>"Strauch"</strong></a><br/></td>
<td>Nimmt eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene " <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>strinret</strong></a> "-Struktur an und gibt einen Zeiger auf eine zugeordnete Zeichenfolge zurück, die den anzeigen Amen enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="strrettostrn.md"><strong>"Strauch"</strong></a><br/></td>
<td>Nimmt eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>zurückgegebene " <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>strinret</strong></a> "-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>"Straurstri"</strong></a><br/></td>
<td>Sucht nach dem letzten Vorkommen einer angegebenen Teil Zeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br/></td>
<td>Ruft die Länge einer Teil Zeichenfolge innerhalb einer Zeichenfolge ab, die vollständig aus Zeichen besteht, die in einem angegebenen Puffer enthalten sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br/></td>
<td>Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>"Straume"</strong></a><br/></td>
<td>Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>"Stringeint"</strong></a><br/></td>
<td>Konvertiert eine Zeichenfolge, die einen Dezimalwert darstellt, in eine ganze Zahl. Das " <strong>strautolong</strong> "-Makro ist mit dieser Funktion identisch.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br/></td>
<td>Konvertiert eine Zeichenfolge, die einen Dezimal-oder Hexadezimalwert darstellt, in eine ganze Zahl mit 64 Bit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>"Straume"</strong></a><br/></td>
<td>Konvertiert eine Zeichenfolge, die eine Dezimal-oder hexadezimal Zahl darstellt, in eine ganze Zahl.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>"Straume"</strong></a><br/></td>
<td>Entfernt die angegebenen führenden und nachfolgenden Zeichen aus einer Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br/></td>
<td>Nimmt eine Argumentliste variabler Länge an und gibt die Werte der Argumente als Format Zeichenfolge im <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-Format zurück. <br/>
<blockquote>
[!Note]<br />
Verwenden Sie diese Funktion nicht. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br/></td>
<td>Nimmt eine Liste von Argumenten an und gibt die Werte der Argumente als eine im <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>formatierte Zeichenfolge zurück. <br/>
<blockquote>
[!Note]<br />
Verwenden Sie diese Funktion nicht. Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
