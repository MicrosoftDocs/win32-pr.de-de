---
description: In diesem Abschnitt werden die Windows Shell-Zeichenfolgenbehandlungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.
title: Shell-Zeichenfolgenbehandlungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473316"
---
# <a name="shell-string-handling-functions"></a>Shell-Zeichenfolgenbehandlungsfunktionen

In diesem Abschnitt werden die Windows Shell-Zeichenfolgenbehandlungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrycmpI</strong></a><br /> | Führt einen Vergleich zwischen zwei Zeichen aus. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br /> | Ruft eine Zeichenfolge ab, die bei der Angabe von Spracheinstellungen mit Websites verwendet wird.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br /> | Führt einen Vergleich einer angegebenen Anzahl von Zeichen ab dem Anfang von zwei lokalisierten Zeichenfolgen durch, bei dem die Groß-/Kleinschreibung beachtet wird.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br /> | Führt einen Vergleich einer angegebenen Anzahl von Zeichen ab dem Anfang von zwei lokalisierten Zeichenfolgen ohne Unterscheidung nach Groß-/Kleinschreibung durch.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei lokalisierten Zeichenfolgen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br /> | Bestimmt, ob ein Zeichen ein Leerzeichen darstellt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br /> | Extrahiert eine angegebene Textressource, wenn diese Ressource in Form einer indirekten Zeichenfolge angegeben wird (eine Zeichenfolge, die mit dem @-Symbol beginnt).<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br /> | Erstellt eine Kopie einer Zeichenfolge im neu zugeordneten Speicher.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>Strcat</strong></a><br /> | Fügt eine Zeichenfolge an eine andere an. <br /><blockquote>[!Note]<br />Darf nicht verwendet werden. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br /> | Kopiert Und fügt Zeichen aus einer Zeichenfolge an das Ende einer anderen an. <br /><blockquote>[!Note]<br />Darf nicht verwendet werden. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br /> | Verkettet zwei Unicode-Zeichenfolgen. Wird verwendet, wenn wiederholte Verkettungen mit demselben Puffer erforderlich sind.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das dem angegebenen Zeichen entspricht. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das dem angegebenen Zeichen entspricht. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>Strcmp</strong></a><br /> | Vergleicht zwei Zeichenfolgen, um zu bestimmen, ob sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br /> | Vergleicht Zeichenfolgen mithilfe von ASCII-Sortierungsregeln (C-Laufzeit). Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br /> | Vergleicht zwei Zeichenfolgen, um zu bestimmen, ob sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br /> | Vergleicht zwei Zeichenfolgen mithilfe von ASCII-Sortierungsregeln (C-Laufzeit). Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br /> | Vergleicht zwei Unicode-Zeichenfolgen. Ziffern in den Zeichenfolgen werden als numerischer Inhalt und nicht als Text betrachtet. Bei diesem Test wird die Groß-/Kleinschreibung nicht beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei Zeichenfolgen, um zu bestimmen, ob sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung beachtet. Das <strong>StrNCmp-Makro</strong> unterscheidet sich nur im Namen von dieser Funktion.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei Zeichenfolgen mithilfe von ASCII-Sortierungsregeln (C-Laufzeit). Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei Zeichenfolgen, um zu bestimmen, ob sie identisch sind. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt. Das <strong>StrNCmpI-Makro</strong> unterscheidet sich nur im Namen von dieser Funktion.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei Zeichenfolgen mithilfe von ASCII-Sortierungsregeln (C-Laufzeit). Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>Strcpy</strong></a><br /> | Kopiert eine Zeichenfolge in eine andere. <br /><blockquote>[!Note]<br />Darf nicht verwendet werden. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br /> | Kopiert eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge in eine andere.<br /><blockquote>[!Note]<br />Verwenden Sie diese Funktion oder das <strong>StrNCpy-Makro</strong> nicht. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer Beliebigen Zeichengruppe. Bei der Suchmethode wird die Groß-/Kleinschreibung beachtet, und das abschließende <strong>NULL-Zeichen</strong> ist in der Übereinstimmung mit dem Suchmuster enthalten.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer Beliebigen Zeichengruppe. Bei der Suchmethode wird die Groß-/Kleinschreibung nicht beachtet, und das abschließende <strong>NULL-Zeichen</strong> ist in der Übereinstimmung mit dem Suchmuster enthalten.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>Strings.strdup</strong></a><br /> | Dupliziert eine Zeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe als Größenwert in Bytes, Kilobytes, Megabytes oder Gigabyte ausgedrückt wird.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br /> | Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe als Größenwert in Bytes, Kilobytes, Megabytes oder Gigabyte ausgedrückt wird. Unterscheidet sich von <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in einem Parametertyp.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br /> | Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Anzahl in Bytes, Kilobytes, Megabytes oder Gigabytes darstellt, je nach Größe. Erweitert <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW,</strong></a> indem die Option zum Runden auf die nächste angezeigte Ziffer oder zum Verwerfen von nicht wiedergegebenen Ziffern angeboten wird.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br /> | Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe als Größenwert in Bytes, Kilobytes, Megabytes oder Gigabyte ausgedrückt wird. Unterscheidet sich von <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in einem Parametertyp.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br /> | Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die als Größenwert in Kilobyte ausgedrückt wird.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br /> | Konvertiert ein in Millisekunden angegebenes Zeitintervall in eine Zeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br /> | Vergleicht eine angegebene Anzahl von Zeichen am Anfang von zwei Zeichenfolgen, um zu bestimmen, ob sie gleich sind.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | Fügt eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge an das Ende einer anderen an. <br /><blockquote>[!Note]<br />Verwenden Sie diese Funktion oder das <strong>StrCatN-Makro</strong> nicht. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das in einem angegebenen Puffer enthalten ist. Diese Suche enthält nicht das abschließende NULL-Zeichen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br /> | Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br /> | Akzeptiert eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> zurückgegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET-Struktur,</strong></a> die eine Zeichenfolge enthält oder auf diese zeigt, und gibt diese Zeichenfolge als <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br /> | Konvertiert eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>strret-Struktur,</strong></a> die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> zurückgegeben wird, in eine Zeichenfolge und platziert das Ergebnis in einen Puffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br /> | Verwendet eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET-Struktur,</strong></a> die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> zurückgegeben wird, und gibt einen Zeiger auf eine zugeordnete Zeichenfolge zurück, die den Anzeigenamen enthält.<br /> | 
| <a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br /> | Übernimmt eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET-Struktur,</strong></a> die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>zurückgegeben wird, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br /> | Sucht nach dem letzten Vorkommen einer angegebenen Teilzeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | Ruft die Länge einer Teilzeichenfolge innerhalb einer Zeichenfolge ab, die vollständig aus Zeichen besteht, die in einem angegebenen Puffer enthalten sind.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>Strstr</strong></a><br /> | Sucht das erste Vorkommen einer Teilzeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br /> | Sucht das erste Vorkommen einer Teilzeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br /> | Konvertiert eine Zeichenfolge, die einen Dezimalwert darstellt, in eine ganze Zahl. Das <strong>StrToLong-Makro</strong> ist mit dieser Funktion identisch.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | Konvertiert eine Zeichenfolge, die einen Dezimal- oder Hexadezimalwert darstellt, in eine 64-Bit-Ganzzahl.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br /> | Konvertiert eine Zeichenfolge, die eine Dezimal- oder Hexadezimalzahl darstellt, in eine ganze Zahl.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br /> | Entfernt angegebene führende und nachfolgende Zeichen aus einer Zeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br /> | Verwendet eine Argumentliste variabler Länge und gibt die Werte der Argumente als formatierte Zeichenfolge im <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf-Format</strong></a>zurück. <br /><blockquote>[!Note]<br />Verwenden Sie diese Funktion nicht. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br /> | Verwendet eine Liste von Argumenten und gibt die Werte der Argumente als <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>formatierte Printf-Formatzeichenfolge</strong></a>zurück. <br /><blockquote>[!Note]<br />Verwenden Sie diese Funktion nicht. Informationen zu alternativen Funktionen finden Sie unter Hinweise.</blockquote><br /> | 




 

 

 
