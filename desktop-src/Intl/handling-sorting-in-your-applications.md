---
description: Einige Anwendungen, z. B. Microsoft Active Directory, Microsoft Exchange und Microsoft Access, verwalten eine sortierbare Datenbank mit Gebietsschema- und Sprachzeichenfolgen, die nach Namen indiziert sind (UTF-16-Zeichenfolge) und die zugehörigen Sortiergewichtungen.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Behandeln der Sortierung in Ihren Anwendungen
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 73c7ca897cb5f83e5a073205341f8b0d0f96ff2d0a9d4c7144a914cd5c96c44d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822690"
---
# <a name="handling-sorting-in-your-applications"></a>Behandeln der Sortierung in Ihren Anwendungen

Einige Anwendungen, z. B. Microsoft Active Directory, Microsoft Exchange und Microsoft Access, verwalten eine sortierbare Datenbank mit Gebietsschema- und Sprachzeichenfolgen, die nach Namen indiziert sind (UTF-16-Zeichenfolge) und die zugehörigen Sortiergewichtungen.

[Die Sortierung](sorting.md) ist in der Regel für Benutzer in ihren eigenen Gebietsschemas intuitiv. Es kann jedoch für Anwendungsentwickler nicht intuitiv sein. In diesem Thema werden Überlegungen zur Sortierung in Ihren Anwendungen erläutert. Die Sortierung kann entweder linguistisch oder ordinal (nicht linguistisch) sein.

## <a name="sorting-functions"></a>Sortierfunktionen

Sie können eine Vielzahl von Sortierfunktionen in Ihren Anwendungen verwenden:

-   NLS-Zeichenfolgenvergleichsfunktionen. Beispiele hierfür sind [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**CompareStringOrdinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)und [**FindStringOrdinal.**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) Unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md) finden Sie eine Erläuterung der Sicherheitsprobleme im Zusammenhang mit den Zeichenfolgenvergleichsfunktionen.
-   Wrapperfunktionen, die die Zeichenfolgenvergleichsfunktionen intern aufrufen. Die gängigsten Funktionen sind [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) und [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)die [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)aufrufen.

In der Regel werten die Sortierfunktionen Zeichenfolgen nach Zeichen aus. Viele Sprachen verfügen jedoch über Mehrere-Zeichen-Elemente, z.B. das Zwei-Zeichen-Paar "CH" in traditionellem Spanisch. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) verwenden den von der Anwendung bereitgestellten Gebietsschemabezeichner oder -namen, um Elemente mit mehreren Zeichen zu identifizieren. Im Gegensatz dazu verwenden [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)und [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) das Gebietsschema des Benutzers.

Ein weiteres Beispiel ist Dies ist Dies ist Einfallszeichen, das viele zweistellige Elemente enthält, z. B. die gültigen Groß-, Titel- und Kleinbuchstaben von "GI", also "GI", "Gi" bzw. "gi". Jede dieser Formen wird als einzelnes Sortierelement behandelt und, wenn die Groß-/Kleinschreibung ignoriert wird, als gleich verglichen. Da "gI" jedoch nicht als einzelnes Element gültig ist, behandeln [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)und [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) "gI" als zwei separate Elemente.

Die Funktionen [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp,**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)und [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) verwenden standardmäßig eine "Wortsortierung"-Technik. Bei dieser Art von Sortierung werden alle Interpunktionszeichen und andere nicht alphanumerische Zeichen, mit Ausnahme des Bindestrichs und des Apostrophs, vor einem alphanumerischen Zeichen angezeigt. Der Bindestrich und der Apostroph werden anders behandelt als die anderen nicht alphanumerischen Zeichen, um sicherzustellen, dass Wörter wie "coop" und "co-op" in einer sortierten Liste zusammen bleiben.

Anstelle einer Wortsortierung kann die Anwendung eine "Zeichenfolgensortierung" von den Sortierfunktionen anfordern, indem sie das \_ SORT STRINGSORT-Flag angibt. Eine Zeichenfolgensortiert den Bindestrich und den Apostroph wie jedes andere nicht alphanumerische Zeichen. Ihre Positionen in der Sortiersequenz liegen vor den alphanumerischen Zeichen.

In der folgenden Tabelle werden die Ergebnisse einer Wortsortierreihenfolge mit den Ergebnissen einer Zeichenfolgensortierreihenfolge verglichen. 

| Wortsortieren | Zeichenfolgensortieren |
|-----------|-------------|
| Billet    | der Rechnung      |
| Rechnungen     | Billet      |
| der Rechnung    | Rechnungen       |
| nicht    | Nicht       |
| Cant      | nicht      |
| Nicht     | Cant        |
| Con       | Co-Op       |
| Coop      | Con         |
| Co-Op     | Coop        |



 

## <a name="sort-strings-linguistically"></a>Linguistisches Sortieren von Zeichenfolgen

Die [**Funktionen CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) testen auf linguistische Gleichheit. Ihre Anwendungen sollten diese Funktionen mit dem richtigen Gebietsschema verwenden, um Zeichenfolgen linguistisch zu sortieren.

> [!Note]  
> Aus Gründen der Kompatibilität mit Unicode sollte eine Anwendung [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) oder die Unicode-Version von [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)bevorzugen. Ein weiterer Grund für die Bevorzugte Verwendung von [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ist, dass Microsoft aus Interoperabilitätsgründen zur Verwendung von Gebietsschemanamen anstelle von Gebietsschemabezeichnern für neue Gebietsschemas migriert. Jede Anwendung, die nur auf Windows Vista und höher ausgeführt wird, sollte [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)verwenden.

 

Eine weitere Möglichkeit zum Testen auf linguistische Gleichheit ist die Verwendung von [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) oder [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)die immer eine Wortsortierung verwenden. Die [**lstrcmpi-Funktion**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) ruft [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) mit dem NORM \_ IGNORECASE-Flag auf, während [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) es ohne dieses Flag aufruft. Eine Übersicht über die Verwendung der Wrapperfunktionen finden Sie unter [**Zeichenfolgen.**](../menurc/strings.md)

Die Funktionen rufen linguistisch geeignete Ergebnisse für alle Gebietsschemas ab. Die Benutzererwartungen für verschiedene Gebietsschemas können sich im Sortierverhalten erheblich unterscheiden, wie in den folgenden Beispielen gezeigt.

-   Viele Gebietsschemas entsprechen den Buchstaben ae und ae. Allerdings betrachtet Dies ein separater Buchstabe und platziert ihn nach Z in der Sortiersequenz.
-   Der A-Ring (Å) sortiert normalerweise nur mit einem diakritischen Unterschied zu A. Allerdings platziert Schwedisch (Schwedisch) den A-Ring nach Z in der Sortiersequenz.

Die Funktionen versuchen gründlich zu überprüfen, ob im Unicode-Standard definierte Codepunkte kanonisch gleich einer Zeichenfolge gleichwertiger Codepunkte sind. Beispielsweise ist der Codepunkt, der ein Kleinbuchstabe "u" mit einer Dieresis (ü) darstellt, kanonisch gleich einem Kleinbuchstaben "u" in Kombination mit der -Dieresis ( sstelle). Beachten Sie jedoch, dass die kanonische Äquivalenz nicht immer möglich ist.

Da fast alle Daten, die mit Windows Tastaturen und Eingabemethoden-Editoren (IMEs) eingegeben werden, der im Unicode-Standard definierten Form C-Normalisierung entsprechen, liefert die Konvertierung eingehender Daten von anderen Plattformen mithilfe der NLS Unicode-Normalisierungsfunktionen die meisten konsistenten Ergebnisse, insbesondere für Gebietsschemas, die das Skript "Hinweise" oder das Hangul-Skript für modernen Hangul verwenden. Weitere Informationen zur Unterstützung der Unicode-Normalisierung in Windows Vista und höher finden Sie unter [Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen.](using-unicode-normalization-to-represent-strings.md)

Wenn der Zeichenfolgenvergleich der Spracheinstellung des Benutzers entspricht, z. B. beim Sortieren von Elementen für ein geordnetes ListView-Steuerelement, kann die Anwendung eine der folgenden Schritte ausführen:

-   Rufen Sie [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) oder [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) mit dem Gebietsschema des Benutzers auf.
-   Rufen Sie [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) auf, um ein Gebietsschema für den Vergleich zu definieren, zusätzliche Flags zu übergeben, NULL-Zeichen einzubetten oder explizite Längen zu übergeben, um Teile einer Zeichenfolge abzugleichen.

Wenn die Ergebnisse des Vergleichs unabhängig vom Gebietsschema konsistent sein sollen, z. B. wenn abgerufene Daten mit einer vordefinierten Liste oder einem internen Wert verglichen werden, sollte die Anwendung [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) verwenden, wobei der *Locale-Parameter* auf LOCALE \_ INVARIANT festgelegt ist. Für [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)stimmt einer der folgenden Aufrufe auch dann überein, wenn mystr "INLAP" ist. In diesem Fall schlägt ein gebietsschemaabhängiger Aufruf von [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) fehl, wenn das aktuelle Gebietsschema "Gilt" ist.

Unter Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Unter früheren Betriebssystemen:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Sortieren von Zeichenfolgen normalerweise

Für die Ordinalsortierung (nicht linguistisch) sollten Ihre Anwendungen immer die [**CompareStringOrdinal-Funktion**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) verwenden.

> [!Note]  
> Diese Funktion ist nur für Windows Vista und höher verfügbar.

 

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) vergleicht zwei [Unicode-Zeichenfolgen,](unicode.md) um binäre Gleichheit im Gegensatz zur linguistischen Gleichheit zu testen. Beispiele für solche nicht linguistischen Zeichenfolgen sind NTFS-Dateinamen, Umgebungsvariablen und die Namen von Mutexes, Named Pipes oder Mailslots. Mit Ausnahme der Option der Unterscheidung nach Groß-/Kleinschreibung ignoriert diese Funktion alle nicht binären Äquivalenzen. Im Gegensatz zu einigen anderen Sortierfunktionen testet es alle Codepunkte auf Gleichheit, einschließlich derjenigen, denen keine Gewichtung in linguistischen Sortierschemas gegeben ist.

Alle folgenden Anweisungen gelten für [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) in binären Vergleichen, jedoch nicht für [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)oder [**lstrcmpi.**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

-   Kanonisch äquivalente Sequenzen in Unicode, z. B. LATIN SMALL LETTER A WITH RING ABOVE (U+00e5) und LATIN SMALL LETTER A + COMBINING RING ABOVE (U+0061 U+030a), sind nicht gleich, obwohl sie identisch erscheinen ("μ").
-   Kanonisch ähnliche Zeichenfolgen in Unicode, z. B. LATIN LETTER SMALL CAPITAL Y (U+028f) und LATIN CAPITAL LETTER Y (U+0059), die sehr ähnlich aussehen ("ʏ" und "Y"), und nur durch einige Sonderfallgewichtungen in den linguistischen Tabellen variieren, werden als völlig unterschiedliche Zeichen betrachtet. Selbst wenn die Anwendung *bIgnoreCase* auf **TRUE** festlegt, werden diese Zeichenfolgen als unterschiedlich verglichen.
-   Codepunkte, die definiert sind, aber keine linguistische Sortiergewichtung aufweisen, z. B. ZERO WIDTH JOINER (U+200d), werden so behandelt, als hätten sie ihre Codepunktgewichtungen.
-   Codepunkte, die in späteren Versionen von Unicode definiert sind, aber in aktuellen linguistischen Tabellen keine Gewichtung aufweisen, werden so behandelt, als hätten sie ihre Codepunktgewichtungen.
-   Codepunkte, die von Unicode nicht definiert sind, werden so behandelt, als hätten sie ihre Codepunktgewichtungen.
-   Wenn die Anwendung *bIgnoreCase* auf **TRUE** festlegt, ordnet die Funktion die Groß-/Kleinschreibung mithilfe der Tabelle mit dem Betriebssystem uppercasing anstelle der Informationen in den linguistischen Sortiertabellen zu. Daher ist die Zuordnung unabhängig vom Gebietsschema.

Weitere Informationen zu kanonisch gleichwertigen Sequenzen in Unicode und kanonisch ähnlichen Zeichenfolgen in Unicode finden Sie unter [Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen.](using-unicode-normalization-to-represent-strings.md)

## <a name="sort-code-points"></a>Sortieren von Codepunkten

Einige Unicode-Codepunkte haben keine Gewichtung, z. B. ZERO WIDTH NON JOINER, U+200c. Die Sortierfunktionen werten absichtlich die Codepunkte ohne Gewichtung als gleichwertig aus, da sie keine Gewichtung bei der Sortierung haben. Auf Windows Vista und höher kann die Anwendung diese Codepunkte sortieren, indem sie die NLS-Zeichenfolgenvergleichsfunktionen, insbesondere [**CompareStringOrdinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)aufruft, um alle Codepunkte in einem literalen, binären Sinn zu bewerten, z. B. bei der Kennwortüberprüfung. Bei Betriebssystemen vor Windows Vista sollte die Anwendung die C-Laufzeitfunktion **strcmp** oder **wcscmp** verwenden.

Sortierfunktionen ignorieren diakritische Zeichen, z. B. NON SPACING BREVE, U+0306, wenn die Anwendung das \_ hlink NONSPACE-Flag angibt. Auf ähnliche Weise ignorieren diese Funktionen Symbole, z. B. EQUALS SIGN, U+003d, wenn das \_ hlink SYMBOLS-Flag angegeben wird. In Windows Vista und höher ruft die Anwendung [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) auf, um diakritische Zeichen und Symbolcodepunkte im literalen, binären Sinn zu auswertet. Bei Vor-Windows Vista-Betriebssystemen sollte die Anwendung **strcmp** oder **wcscmp verwenden.**

Einige Codepunkte, z. B. 0xFFFF und 0x058b, werden derzeit nicht in Unicode zugewiesen. Diese Codepunkte erhalten keine Gewichtung bei der Sortierung und sollten nie an die Sortierfunktionen übergeben werden. Die Anwendung sollte [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) verwenden, um Nicht-Unicode-Codepunkte in einem Datenstrom zu erkennen.

> [!Note]  
> Die Ergebnisse [**von IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) können je nach der übergebenen Unicode-Version variieren, wenn unicode in einer späteren Version ein Zeichen hinzugefügt wird und es anschließend den Windows hinzugefügt wird. Weitere Informationen finden Sie unter [Use Sort Versioning](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Ziffern als Zahlen sortieren

Ab Windows 7 kann die Anwendung [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)oder [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mithilfe des SORT \_ DIGITSASNUMBERS-Flags aufrufen. Dieses Flag unterstützt die Sortierung, die Ziffern als Zahlen behandelt, z. B. die Sortierung von "2" vor "10".

Beachten Sie, dass die Verwendung dieses Flags für Hexadezimalziffern wie die folgenden nicht geeignet ist. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

In diesem Fall werden die "Zahlen" in der Reihenfolge sortiert, aber der Benutzer nimmt eine schlecht sortierte Hexadezimalliste wahr.

## <a name="map-strings"></a>Zuordnen von Zeichenfolgen

Die Anwendung verwendet die [**LCMapString-**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**LCMapStringEx-Funktion**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) zum Zuordnen von Zeichenfolgen, wenn LCMAP \_ SORTKEY nicht angegeben ist. Eine zugeordnete Zeichenfolge wird mit NULL beendet, wenn die Quellzeichenfolge null-terminiert ist.

Bei der Transformation zwischen Groß- und Kleinbuchstaben garantiert die Funktion nicht, dass ein einzelnes Zeichen einem einzelnen Zeichen zuordnen wird. Beispielsweise können die Flags LCMAP LOWERCASE und LCMAP UPPERCASE das deutsche \_ \_ Sharp S (" ") sich selbst zuordnen. Alternativ kann das LCMAP \_ UPPERCASE-Flag "lk" "SS" zuordnen, und das LCMAP LOWERCASE-Flag kann \_ "SS" "lk" zuordnen. Das Verhalten hängt von der NLS-Version ab.

Bei der Transformation zwischen Groß- und Kleinbuchstaben ist die Funktion nicht kontextempfindlich. Während beispielsweise das LCMAP UPPERCASE-Flag sowohl das griechisch-kleingeschriebene Sigma ("σ") als auch das griechisch kleingeschriebene final sigma ("σ") dem griechisch großgeschriebenen Sigma ("Σ") ordnungsgemäß zu ordnet, ordnet das \_ LCMAP \_ LOWERCASE-Flag immer "Σ" "σ" zu, nie "σ".

Standardmäßig ordnet die Funktion den Kleinbuchstaben "i" dem groß geschriebenen "I" zu, auch wenn der *Locale-Parameter* Türkisch oder Einei angibt. Um dieses Verhalten für Türkisch oder Türkisch zu überschreiben, muss die Anwendung LCMAP \_ LINGUISTIC \_ CASING angeben. Wenn dieses Flag mit dem entsprechenden -Locale angegeben wird, ist "â" (punktloses I in Kleinbuchstaben) die Kleinbuchstabenform von "I" (punktloses I in Großbuchstaben) und "i" (gepunktete I-Datei in Kleinbuchstaben) die Kleinbuchstabenform "2" (gepunktete I-Großbuchstaben).

Wenn das LCMAP HIRAGANA-Flag angegeben ist, um \_ Hiragana-Zeichen Katakana-Zeichen zu zuordnen, und LCMAP FULLWIDTH nicht angegeben ist, ordnet \_ [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) nur Zeichen mit voller Breite hiragana zu. In diesem Fall werden alle Katakana-Zeichen mit halber Breite als in der Zielzeichenfolge platziert, ohne dass hiragana zuordnen wird. Die Anwendung muss LCMAP \_ FULLWIDTH angeben, um Hiragana Katakana-Zeichen halber Breite zuordnen zu können. Der Grund für diese Einschränkung ist, dass alle Hiragana-Zeichen Zeichen mit voller Breite sind.

Wenn die Anwendung Zeichen aus der Quellzeichenfolge stripen muss, kann sie die Zuordnungsfunktion mit den festgelegten Flags NORM \_ IGNORESYMBOLS und NORM IGNORENONSPACE aufrufen und alle anderen \_ Flags löschen. Wenn die Anwendung dies mit einer Quellzeichenfolge macht, die nicht auf NULL endet, kann die Funktion eine leere Zeichenfolge zurückgeben und keinen Fehler zurückgeben.

## <a name="create-sort-keys"></a>Erstellen von Sortierschlüsseln

Wenn die Anwendung LCMAP \_ SORTKEY angibt, [**generiert LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) einen Sortierschlüssel, ein binäres Array von Bytewerten. Der Sortierschlüssel ist keine echte Zeichenfolge, und seine Werte stellen das Sortierverhalten der Quellzeichenfolge dar, sind jedoch keine aussagekräftigen Anzeigewerte.

> [!Note]  
> Die Funktion ignoriert die arabische Kashida während der Generierung eines Sortierschlüssels. Wenn eine Anwendung die Funktion aufruft, um einen Sortierschlüssel für eine Zeichenfolge zu erstellen, die eine arabische Kashida enthält, erstellt die Funktion keinen Sortierschlüsselwert.

 

Der Sortierschlüssel kann eine ungerade Anzahl von Bytes enthalten. Das LCMAP \_ BYTEREV-Flag kehrt nur eine gerade Anzahl von Bytes um. Das letzte (ungerade) Byte im Sortierschlüssel wird nicht umgekehrt. Wenn das abschließende 0x00 byte ein ungerades positioniertes Byte ist, bleibt es das letzte Byte im Sortierschlüssel. Wenn das beendende 0x00 byte ein gleichmäßig positioniertes Byte ist, tauscht es Positionen mit dem vorangehenden Byte aus.

Beim Generieren des Sortierschlüssels behandelt die Funktion den Bindestrich und das Apostroph anders als andere Interpunktionssymbole, sodass Wörter wie "list" und "co-op" in einer Liste zusammen bleiben. Alle Interpunktionssymbole außer bindestrich und Apostroph werden vor alphanumerischen Zeichen sortiert. Die Anwendung kann dieses Verhalten ändern, indem das SORT \_ STRINGSORT-Flag wie unter Sortierfunktionen [beschrieben wird.](#sorting-functions)

Bei Verwendung in [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp)erzeugt der Sortierschlüssel die gleiche Reihenfolge wie bei verwendung der Quellzeichenfolge in [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**CompareStringEx.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) Die [memcmp-Funktion](/cpp/c-runtime-library/reference/memcmp-wmemcmp) sollte anstelle von [strcmp verwendet](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)werden, da der Sortierschlüssel eingebettete NULL-Bytes enthalten kann.

## <a name="use-sort-versioning"></a>Verwenden der Sortierversionsierung

Eine [Sortiertabelle](sorting.md) enthält zwei Zahlen, die ihre Version identifizieren: die definierte Version und die NLS-Version. Beide Zahlen sind DWORD-Werte, die aus einem Haupt- und einem Nebenwert bestehen. Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die Nebenversion dar. Hexadezimal ist das Muster 0xRRMMMMmm, wobei R gleich Reserved, M gleich major und m gleich minor ist. Beispielsweise wird eine Hauptversion von 3 mit einer Nebenversion von 4 als 0x304.

Die definierte Version identifiziert den Code points-Code und ist für alle Locales identisch. Die Hauptversion wird erhöht, um Änderungen an vorhandenen Codepunkten anzugeben. Die Nebenversion wird erhöht, um anzugeben, dass Codepunkte hinzugefügt wurden, aber keine bereits vorhandenen Codepunkte geändert wurden.

Die NLS-Version ist spezifisch für einen [Locale](locale-identifiers.md) Identifier oder [Locale Name](locale-names.md)und verfolgt Änderungen an der Codepunktgewichtung für das betroffene Locale nach. Die Hauptversion wird erhöht, wenn die Gewichtungen für Codepunkte geändert werden, die bereits sortierbar waren. Die Nebenversion wird erhöht, wenn neuen Codepunkten Gewichtungen zugewiesen werden, aber alle anderen zuvor sortierbaren Codepunktgewichtungen bleiben unverändert.

> [!Note]  
> Bei einer Hauptversion werden ein oder mehrere Codepunkte geändert, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind. Bei einer Nebenversion wird nichts verschoben, aber Codepunkte werden hinzugefügt. Bei dieser Version muss die Anwendung nur Zeichenfolgen mit zuvor nicht amortisierbaren Werten neu indizieren.

 

> [!IMPORTANT]
> Die Hauptversion wurde in der Windows 8. Daten, die unter früheren Versionen von Windows wurden, müssen erneut indiziert werden.

 

Sowohl die definierte Version als auch die NLS-Version gelten für sortierbare Codepunkte, die mithilfe der [**LCMapString-**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**LCMapStringEx-Funktion**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mit dem LCMAP SORTKEY-Flag abgerufen und auch von den \_ Funktionen [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)und [**FindNLSStringEx verwendet**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) werden. Wenn ein oder mehrere Codepunkte in einer Zeichenfolge nicht amortisiert werden können, gibt die [**IsNLSDefinedString-Funktion**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) **FALSE** zurück, wenn diese Zeichenfolge als Parameter an sie übergeben wird.

Die Anwendung kann entweder [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) oder [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortiertabelle abzurufen.

## <a name="index-the-database"></a>Indizieren der Datenbank

Aus Leistungsgründen sollte die Anwendung dieses Verfahren beim Indizieren der Datenbank befolgen.

**So indizieren Sie die Datenbank ordnungsgemäß**

1.  Speichern Sie für jede Funktion die NLS-Version, die Sortierschlüssel dieser Version und einen Hinweis auf die Sortierbarkeit für jede indizierte Zeichenfolge.
2.  Wenn die Nebenversion inkrementiert wird, indizieren Sie zuvor unortierbare Zeichenfolgen neu. Die von diesem Update betroffenen Zeichenfolgen sollten auf die Zeichenfolgen beschränkt sein, für die [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) zuvor FALSE zurückgegeben **hat.**
3.  Wenn die Hauptversion inkrementiert wird, indizieren Sie alle Zeichenfolgen neu, da die aktualisierten Gewichtungen das Verhalten einer beliebigen Zeichenfolge ändern können. Hauptversionsversionen sind sehr selten.

Probleme bei der Datenbankindizierung können aus den folgenden Gründen auftreten:

-   Ein späteres Betriebssystem kann Codepunkte definieren, die für ein früheres Betriebssystem nicht definiert sind, wodurch die Sortierung geändert wird.
-   Codepunkte können aufgrund von Korrekturen bei der Sprachunterstützung unterschiedliche Sortiergewichtungen in verschiedenen Betriebssystemen haben.

Um die Notwendigkeit einer erneuten Indizierung der Datenbank in diesen Fällen zu minimieren, kann die Anwendung [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) verwenden, um definierte von nicht definierten Zeichenfolgen zu unterscheiden, damit die Anwendung Zeichenfolgen mit nicht definierten Codepunkten ablehnen kann. Die Verwendung [**von GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) oder [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) ermöglicht der Anwendung zu bestimmen, ob eine NLS-Änderung das für eine bestimmte Indextabelle verwendete Locale beeinflusst. Wenn die Änderung keine Auswirkungen auf das -Locale hat, muss die Anwendung die Tabelle nicht erneut indizieren.

## <a name="examples"></a>Beispiele

Die folgende Tabelle veranschaulicht die Auswirkungen bestimmter Flags, die mit den Sortierfunktionen verwendet werden. In jedem Fall bestimmt die Auswahl von Flags, ob zwei verschiedene Zeichen zu Sortierzwecken als gleich betrachtet werden.



| Zeichen 1                                                        | Zeichen 2                                             | Standard | NORM \_ IGNOREWIDTH | NORM \_ IGNOREKANA | NORM \_ IGNOREWIDTH\| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U+3042 HIRAGANA LETTER A<br/>                | "ガ"<br/> U+30A2 KATAKANA LETTER A<br/>     | Ungleiche | Ungleiche           | Gleich            | Gleich                              |
| "ｵ"<br/> U+FF75 HALFWIDTH KATAKANA LETTER O<br/>       | "オ"<br/> U+30AA KATAKANA LETTER O<br/>     | Ungleiche | Gleich             | Ungleiche          | Gleich                              |
| "B"<br/> U+FF22 FULLWIDTH LATEINISCHER GROßBUCHSTABEN B<br/> | „B“<br/> U+0042 LATEINISCHER GROßBUCHSTABEN B<br/> | Ungleiche | Gleich             | Ungleiche          | Gleich                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung der Landessprache](using-national-language-support.md)
</dt> <dt>

[Sortierung](sorting.md)
</dt> <dt>

[Abrufen und Festlegen von Informationen zum Locale](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
