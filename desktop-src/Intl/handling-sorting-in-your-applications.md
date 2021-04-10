---
description: Einige Anwendungen, wie z. b. Microsoft Active Directory, Microsoft Exchange und Microsoft Access, pflegen eine sortierbare Datenbank mit Gebiets Schema-und sprach Zeichenfolgen, die anhand des Namens (UTF-16-Zeichenfolge) und der zugehörigen Sortierungs Gewichtungen indiziert werden.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Behandeln von Sortierungen in Ihren Anwendungen
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: c0bba3d78a5219781226ecf58292ed461c902090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869080"
---
# <a name="handling-sorting-in-your-applications"></a>Behandeln von Sortierungen in Ihren Anwendungen

Einige Anwendungen, wie z. b. Microsoft Active Directory, Microsoft Exchange und Microsoft Access, pflegen eine sortierbare Datenbank mit Gebiets Schema-und sprach Zeichenfolgen, die anhand des Namens (UTF-16-Zeichenfolge) und der zugehörigen Sortierungs Gewichtungen indiziert werden.

Das [Sortieren](sorting.md) ist in der Regel für Benutzer in ihren eigenen Gebiets Schemas intuitiv. Dies kann für Anwendungsentwickler jedoch nicht intuitiv sein. In diesem Thema werden Überlegungen zur Behandlung von Sortierungen in Ihren Anwendungen erläutert. Die Sortierung kann entweder linguistisch oder Ordnungszahl (nicht linguistisch) sein.

## <a name="sorting-functions"></a>Sortierfunktionen

Sie können eine Vielzahl von Sortierungs Funktionen in Ihren Anwendungen verwenden:

-   NLS-Zeichen folgen Vergleichsfunktionen. Beispiele hierfür sind [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)und [**findstringordinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal). Weitere Informationen zu Sicherheitsproblemen im Zusammenhang mit den Zeichen folgen Vergleichsfunktionen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md) .
-   Wrapper Funktionen, die intern die Zeichen folgen Vergleichsfunktionen aufzurufen. Die gängigsten Funktionen sind [**lstraucmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) und [**lstraucmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), die [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)aufzurufen.

Normalerweise werden von den Sortierfunktionen Zeichen folgen Zeichen nach Zeichen ausgewertet. Viele Sprachen haben jedoch Elemente mit mehreren Zeichen, z. b. das zwei-Zeichen-paar "ch" in traditionellem Spanisch. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) verwenden den von der Anwendung bereitgestellten Gebiets Schema Bezeichner oder-Namen zum Identifizieren von Elementen mit mehreren Zeichen. Im Gegensatz dazu verwenden [**lstraucmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)und [**lstrancmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) das Gebiets Schema des Benutzers.

Ein weiteres Beispiel ist Vietnamese, das viele zwei Zeichen große Elemente enthält, z. b. die gültigen groß-und Kleinbuchstaben sowie die Formen "GI", die "GI", "GI" bzw. "GI" sind. Jede dieser Formulare wird als einzelnes Sortier Element behandelt. wenn die Groß-/Kleinschreibung ignoriert wird, wird als gleich verglichen. Da "GI" jedoch nicht als einzelnes Element, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)und [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) gültig ist, wird "GI" als zwei separate Elemente behandelt.

Die Funktionen [**"CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)", " [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)", " [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)", " [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)", " [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)", " [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)", " [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)" und " [**findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) " werden standardmäßig als "Wort Sortiermethode" verwendet. Bei dieser Art von Sortierung sind alle Interpunktions Zeichen und andere nicht alphanumerische Zeichen (mit Ausnahme des Bindestrichs und des Apostroph) vor allen alphanumerischen Zeichen. Der Bindestrich und der Apostroph werden anders behandelt als andere nicht alphanumerische Zeichen, um sicherzustellen, dass Wörter wie "Coop" und "Co-op" in einer sortierten Liste zusammen bleiben.

Anstelle eines Wort Sortier Verfahrens kann die Anwendung eine "Zeichen folgen Sortiermethode" aus den Sortierfunktionen anfordern, indem das Flag "StringSort sortieren" angegeben wird \_ . Eine Zeichen folgen Sortierung behandelt den Bindestrich und Apostroph wie jedes andere nicht alphanumerische Zeichen. Ihre Positionen in der Sortiersequenz liegen vor den alphanumerischen Zeichen.

In der folgenden Tabelle werden die Ergebnisse einer Wort Sortierung mit den Ergebnissen einer Zeichen folgen Sortierung verglichen. 

| Wort Sortierung | Zeichen folgen Sortierung |
|-----------|-------------|
| Billet    | Rechnung      |
| scheinen     | Billet      |
| Rechnung    | scheinen       |
| nicht    | kann       |
| än      | nicht      |
| kann     | än        |
| Lexikon       | Koop       |
| Betreuung      | Lexikon         |
| Koop     | Betreuung        |



 

## <a name="sort-strings-linguistically"></a>Zeichen folgen linguistisch sortieren

Die [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) -Funktion und die [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) -Funktion testen auf linguistische Gleichheit. Ihre Anwendungen sollten diese Funktionen mit dem richtigen Gebiets Schema zum linguistisch Sortieren von Zeichen folgen verwenden.

> [!Note]  
> Aus Gründen der Kompatibilität mit Unicode sollte eine Anwendung [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) oder die Unicode-Version von [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)bevorzugen. Ein weiterer Grund für das bevorzugen von [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) besteht darin, dass Microsoft aus Interoperabilitäts Gründen zur Verwendung von Gebiets Schema Namen anstelle von Gebiets Schema bezeichnerwerten für neue Gebiets Schemas migriert. Jede Anwendung, die nur unter Windows Vista und höher ausgeführt wird, sollte [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)verwenden.

 

Eine andere Möglichkeit, auf linguistische Gleichheit zu testen, ist die Verwendung von [**lstrincmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) oder [**lstraucmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), bei dem immer eine Wort Sortierung verwendet wird. Die [**lstrincmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) -Funktion ruft [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) mit dem \_ normignorecase-Flag auf, während [**lstraucmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) Sie ohne dieses Flag aufruft. Eine Übersicht über die Verwendung der Wrapper [**Funktionen finden Sie**](../menurc/strings.md)unter Zeichen folgen.

Die Funktionen rufen linguistisch geeignete Ergebnisse für alle Gebiets Schemas ab. Die Erwartungen von Benutzern für verschiedene Gebiets Schemas können sich beim Sortier Verhalten erheblich unterscheiden, wie in den folgenden Beispielen gezeigt.

-   Viele Gebiets Schemas entsprechen der AE-Ligaturen (æ) und den Buchstaben AE. Allerdings betrachtet Isländisch (Island) einen separaten Buchstaben und platziert ihn nach Z in der Sortierreihenfolge.
-   Der a-Ring (Å) sortiert normalerweise nur einen diakritischen Unterschied von einer. Der schwedische (Schweden) platziert den Ring jedoch nach Z in der Sortierreihenfolge.

Die Funktionen versuchen, zu überprüfen, ob im Unicode-Standard definierte Code Punkte kanonisch gleich einer Zeichenfolge mit gleichwertigen Code Punkten sind. Beispielsweise ist der Codepunkt, der einen Kleinbuchstaben "u" mit einem Dieresis (ü) darstellt, kanonisch gleich einem Kleinbuchstaben "u", kombiniert mit der Distribution ("a"). Beachten Sie jedoch, dass die kanonische Äquivalenz nicht immer möglich ist.

Da fast alle Daten, die mit Windows-Tastaturen und Eingabemethoden-Editoren (Input Method Editors, IMEs) eingegeben wurden, mit der im Unicode-Standard definierten Form-C-Normalisierung übereinstimmen, bietet das Einfügen eingehender Daten von anderen Plattformen mithilfe der NLS-Unicode-normalisierungs Funktionen die meisten konsistenten Ergebnisse, insbesondere für Gebiets Schemas, die das tibetische Skript verwenden Weitere Informationen zur Unterstützung von Unicode-Normalisierungen in Windows Vista und höher finden [Sie unter Verwenden der Unicode-Normalisierung zur Darstellung](using-unicode-normalization-to-represent-strings.md)von Zeichen folgen.

Wenn der Zeichen folgen Vergleich der Spracheinstellung des Benutzers folgt, z. b. beim Sortieren von Elementen für ein sortiertes ListView-Steuerelement, kann die Anwendung eine der folgenden Aktionen ausführen:

-   Nennen Sie [**lstrecmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) oder [**lstrincmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) mit dem Gebiets Schema des Benutzers.
-   Aufrufen von [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) zum Definieren eines Gebiets Schemas für den Vergleich, zum übergeben zusätzlicher Flags, zum Einbetten von NULL-Zeichen oder zum Übergeben von expliziten Längen, um Teile einer Zeichenfolge abzugleichen.

Wenn die Ergebnisse des Vergleichs unabhängig vom Gebiets Schema konsistent sein sollen, z. b. wenn abgerufene Daten mit einer vordefinierten Liste oder einem internen Wert verglichen werden, sollte die Anwendung [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) mit dem *locale* -Parameter verwenden, der auf locale invariant festgelegt ist \_ . Für [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)stimmt jeder der folgenden Aufrufe gleich, auch wenn myStr den Wert "inlap" hat. In diesem Fall tritt bei einem Gebiets Schema bezogenen Aufrufe von [**lstrincmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) ein Fehler auf, wenn das aktuelle Gebiets Schema Vietnamese ist.

Unter Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Unter früheren Betriebssystemen:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Zeichen folgen Ordnungs mäßig sortieren

Für eine Ordinalzahl (nicht linguistische Sortierung) sollten Ihre Anwendungen immer die [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) -Funktion verwenden.

> [!Note]  
> Diese Funktion ist nur für Windows Vista und höher verfügbar.

 

[**Comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) vergleicht zwei [Unicode](unicode.md) -Zeichen folgen, um auf binäre Gleichheit zu testen (im Gegensatz zur linguistischen Gleichheit). Beispiele für solche nicht linguistischen Zeichen folgen sind NTFS-Dateinamen, Umgebungsvariablen und die Namen von Mutexen, Named Pipes oder Mailslots. Mit Ausnahme der Option für die Unterscheidung nach Groß-/Kleinschreibung ignoriert diese Funktion alle nicht binären äquivalente. Im Gegensatz zu einigen anderen Sortierfunktionen testet es alle Code Punkte auf Gleichheit, einschließlich derjenigen, die in linguistischen Sortier Schemas keine Gewichtung erhalten.

Alle der folgenden Anweisungen gelten für [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) in binären vergleichen, jedoch nicht für [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)oder [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   Kanonisch äquivalente Sequenzen in Unicode, wie z. b. Lateinische Kleinbuchstaben a mit Ring oberhalb (u + 00e5) und Latin Small Letter a + kombinierungsring oberhalb (u + 0061 U + 030A), sind nicht gleich, obwohl Sie identisch ("å") sind.
-   Kanonisch ähnliche Zeichen folgen in Unicode, wie z. b. lateinische Buchstabe Small Capital y (u + 028f) und Latin Capital Letter y (u + 0059), die sehr ähnlich aussehen ("ʏ" und "Y") und sich nur durch einige sondergewichtungen in den linguistischen Tabellen unterscheiden, werden als vollständig abweichende Zeichen betrachtet. Auch wenn die Anwendung *bignorecase* auf " **true**" festlegt, vergleichen diese Zeichen folgen als verschieden.
-   Code Punkte, die zwar definiert sind, aber keine linguistische Sortier Gewichtung aufweisen, wie z. b. "Joiner (null)" (U + 200D), werden so behandelt, als wären Sie mit Ihren Code
-   Code Punkte, die in neueren Versionen von Unicode definiert sind, aber keine Gewichtung in den aktuellen linguistischen Tabellen haben, werden so behandelt, als hätten Sie Ihre Code Punkt Gewichtungen.
-   Code Punkte, die von Unicode nicht definiert werden, werden als Code Punkt Gewichtungen behandelt.
-   Wenn in der Anwendung *bignorecase* auf **true** festgelegt wird, wird die-Funktion mithilfe der Tabelle für die Betriebssystem-groß Schreibung anstelle der Informationen in den linguistischen Sortier Tabellen verwendet. Daher ist die Zuordnung unabhängig vom Gebiets Schema.

Weitere Informationen zu kanonalen äquivalenten Sequenzen in Unicode und kanonalen ähnlichen Zeichen folgen in Unicode finden [Sie unter Verwenden der Unicode-Normalisierung zur Darstellung von](using-unicode-normalization-to-represent-strings.md)Zeichen folgen.

## <a name="sort-code-points"></a>Code Punkte sortieren

Einige Unicode-Code Punkte haben keine Gewichtung, z. b. NULL-Breite, nicht Joiner, U + 200C. Die Sortierfunktionen Werten die nicht Gewichtungs Code Punkte absichtlich als gleichwertig aus, da Sie keine Gewichtung beim Sortieren haben. Unter Windows Vista und höher kann die Anwendung diese Code Punkte sortieren, indem Sie die NLS-Zeichen folgen Vergleichsfunktionen aufrufen, insbesondere [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), für die Auswertung aller Code Punkte in einem literalen, Binär Sinn, z. b. bei der Kenn Wort Validierung. Bei Betriebssystemen vor Windows Vista sollte die Anwendung die C-Lauf Zeitfunktion " **trecmp** " oder " **wcscmp**" verwenden.

Sortierungs Funktionen ignorieren Diakritik, wie z. b. "Non-SPACING Breve", U + 0306, wenn die Anwendung das Flag "hlink \_ nonspace" angibt. Ebenso ignorieren diese Funktionen Symbole, z. b. Gleichheitszeichen, U + 003d, wenn das Flag für die Hlink- \_ Symbole angegeben wird. Unter Windows Vista und höher Ruft die Anwendung [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) auf, um die Diakritik und Symbol Code Punkte in einem literalen, binären Sinn, zu evaluieren. Bei Betriebssystemen vor Windows Vista sollte die Anwendung " **straucmp** " oder " **wcscmp**" verwenden.

Einige Code Punkte, z. b. 0xFFFF und 0x058b, sind derzeit nicht in Unicode zugewiesen. Diese Code Punkte erhalten keine Gewichtung beim Sortieren und sollten niemals an die Sortierungs Funktionen übermittelt werden. Die Anwendung sollte [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) verwenden, um nicht-Unicode-Code Punkte in einem Datenstrom zu erkennen.

> [!Note]  
> Die Ergebnisse von [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) variieren möglicherweise abhängig von der zurückgegebenen Unicode-Version, wenn ein Zeichen zu Unicode in einer neueren Version hinzugefügt wird, und wird anschließend den Windows-Sortier Tabellen hinzugefügt. Weitere Informationen finden Sie unter [use Sort Versioning](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Ziffern als Zahlen sortieren

Unter Windows 7 und höher kann die Anwendung " [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)", " [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)", " [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)" oder " [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) " aufrufen, indem das \_ Flag "digitsasnumbers sortieren" verwendet wird. Dieses Flag unterstützt das Sortieren, bei dem Ziffern als Zahlen behandelt werden, z. b. das Sortieren von "2" vor "10".

Beachten Sie, dass die Verwendung dieses Flags für hexadezimale Ziffern wie die folgende nicht geeignet ist. <dl> 01af  
1bcd  
002A  
12fa  
AB1C  
AB02  
Ab12  
</dl>

In diesem Fall werden die Zahlen in der richtigen Reihenfolge sortiert, aber der Benutzer spürt eine schlecht sortierte hexadezimal Liste ab.

## <a name="map-strings"></a>Zuordnen von Zeichen folgen

Die Anwendung verwendet die [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) -oder [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) -Funktion, um Zeichen folgen zuzuordnen, wenn lcmap \_ SortKey nicht angegeben ist. Eine zugeordnete Zeichenfolge wird auf NULL festgelegt, wenn die Quell Zeichenfolge auf NULL endet.

Beim Transformieren zwischen Groß-und Kleinbuchstaben garantiert die-Funktion nicht, dass ein einzelnes Zeichen einem einzelnen Zeichen zugeordnet wird. Beispielsweise können die Großbuchstaben lcmap \_ Kleinbuchstaben und lcmap \_ die deutschen Sharp-S ("ß") selbst zuordnen. Alternativ kann das Flag für die lcmap \_ -groß Schreibung "ß" zu "SS" zuordnen, und das lcmap- \_ Flag für Kleinbuchstaben kann "SS" zu "ß" zuordnen. Das Verhalten hängt von der NLS-Version ab.

Beim Transformieren zwischen Groß-und Kleinbuchstaben ist die-Funktion nicht für den kontextsensibel. Beispielsweise ordnet das Flag "lcmap \_ Großbuchstaben" ordnungsgemäß sowohl den griechischen Kleinbuchstaben "Sigma" (".") als auch den griechischen Kleinbuchstaben ("...)" mit dem griechischen Großbuchstaben "Sigma" (".") zu. das lcmap-Flag für Kleinbuchstaben ordnet jedoch immer "Zuordnungen" und \_ nie "." zu.

Standardmäßig ordnet die-Funktion den Kleinbuchstaben "i" dem Großbuchstaben "i" zu, auch wenn der Gebiets *Schema Parameter Türkisch* oder Aserbaidschanisch angibt. Um dieses Verhalten für Türkisch oder Aserbaidschanisch außer Kraft zu setzen, sollte die Anwendung eine linguistische lcmap-Schreibweise angeben \_ \_ . Wenn dieses Flag mit dem entsprechenden Gebiets Schema angegeben wird, ist "ı" (Kleinbuchstaben: i) die klein geschriebene Form von "i" (Großbuchstabe ohne bitweise i) und "i" (Großbuchstabe i) ist die klein geschriebene Form von "i" (Großbuchstabe i).

Wenn das lcmap- \_ Hiragana-Flag für die Zuordnung von Katakana-Zeichen in Hiragana-Zeichen angegeben wird und lcmap \_ Fullwidth nicht angegeben ist, ordnet [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) nur Zeichen voller Breite zu Hiragana zu. In diesem Fall werden alle Katakana-Zeichen der Hälfte Breite als Ziel Zeichenfolge ohne Zuordnung zu Hiragana platziert. Die Anwendung muss lcmap \_ Fullwidth angeben, um Katakana-Zeichen mit halber Breite zu Hiragana zuzuordnen. Der Grund für diese Einschränkung besteht darin, dass alle Hiragana-Zeichen Zeichen mit voller Breite sind.

Wenn die Anwendung Zeichen aus der Quell Zeichenfolge entfernen muss, kann Sie die Zuordnungs Funktion mit den \_ festgelegten Standardflags IgnoreSymbols und Norm \_ IgnoreNonSpace aufzurufen, und alle anderen Flags werden gelöscht. Wenn die Anwendung diese mit einer Quell Zeichenfolge durchführt, die nicht auf NULL endet, kann die Funktion eine leere Zeichenfolge zurückgeben und keinen Fehler zurückgeben.

## <a name="create-sort-keys"></a>Sortierschlüssel erstellen

Wenn die Anwendung lcmap \_ SortKey angibt, generiert [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) oder [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) einen Sortierschlüssel, ein binäres Array von Byte Werten. Der Sortierschlüssel ist keine echte Zeichenfolge, und seine Werte stellen das Sortier Verhalten der Quell Zeichenfolge dar, sind jedoch keine aussagekräftigen Anzeigewerte.

> [!Note]  
> Die-Funktion ignoriert die arabische Kashida während der Generierung eines Sortier Schlüssels. Wenn eine Anwendung die-Funktion aufruft, um einen Sortierschlüssel für eine Zeichenfolge zu erstellen, die einen arabischen Kashida enthält, erstellt die-Funktion keinen Sortierschlüssel Wert.

 

Der Sortierschlüssel kann eine ungerade Anzahl von Bytes enthalten. Das lcmap \_ byterev-Flag kehrt nur eine gerade Anzahl von Bytes um. Das letzte Byte (ungerade positioniert) im Sortierschlüssel ist nicht umgekehrt. Wenn das abschließende 0x00-Byte ein ungerade positioniertes Byte ist, bleibt es das letzte Byte im Sortierschlüssel. Wenn das abschließende 0x00-Byte ein gleich positioniertes Byte ist, tauscht es Positionen mit dem vorangestellten Byte aus.

Beim Erstellen des Sortier Schlüssels behandelt die-Funktion den Bindestrich und Apostroph anders als andere Interpunktions Symbole, sodass Wörter wie "Coop" und "Co-op" in einer Liste zusammen bleiben. Alle Interpunktions Symbole außer dem Bindestrich und Apostroph Sortieren vor alphanumerischen Zeichen. Die Anwendung kann dieses Verhalten ändern, indem Sie das \_ Flag "StringSort sortieren" festlegen, wie in [Sortierungs Funktionen](#sorting-functions)beschrieben.

Bei Verwendung in [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp)erzeugt der Sortierschlüssel dieselbe Reihenfolge, in der die Quell Zeichenfolge in [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) oder [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)verwendet wird. Die [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) -Funktion sollte anstelle von " [straucmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)" verwendet werden, da der Sortierschlüssel eingebettete NULL-Bytes aufweisen kann.

## <a name="use-sort-versioning"></a>Verwenden der Sortier Versionsverwaltung

Eine [Sortier](sorting.md) Tabelle verfügt über zwei Zahlen, die Ihre Version identifizieren: die definierte Version und die NLS-Version. Beide Zahlen sind DWORD-Werte, die aus einem Haupt-und einem nebenwert bestehen. Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die neben Version dar. In hexadezimalen begriffen ist das Muster "0xrrmmmmmm", wobei "R" reserviert ist, "m" den Wert "Major" und "m" kleiner ist. Beispielsweise wird eine Hauptversion von 3 mit einer neben Version von 4 als 0x304 dargestellt.

Die definierte Version identifiziert das Repertoire von Code Punkten und ist für alle Gebiets Schemas identisch. Die Hauptversion erhöht sich, um Änderungen an vorhandenen Code Punkten anzugeben. Die neben Versions Inkremente, um anzugeben, dass Code Punkte hinzugefügt wurden, jedoch keine bereits vorhandenen Code Punkte geändert wurden.

Die NLS-Version ist spezifisch für einen Gebiets Schema [Bezeichner](locale-identifiers.md) oder Gebiets Schema [Namen](locale-names.md)und verfolgt Änderungen an den Code Punkt Gewichtungen für das betroffene Gebiets Schema nach. Die Hauptversion erhöht sich, wenn Gewichtungen für Code Punkte geändert werden, die bereits sortierbar waren. Die neben Versions Zunahme erhöht sich, wenn neuen Code Punkten Gewichtungen zugewiesen werden, aber alle anderen zuvor sortierbaren Code Punkt Gewichtungen bleiben unverändert.

> [!Note]  
> Bei einer Hauptversion werden ein oder mehrere Code Punkte geändert, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind. Für eine neben Version wird nichts verschoben, aber Code Punkte werden hinzugefügt. Bei dieser Art von Version muss die Anwendung nur Zeichen folgen mit zuvor nicht sortierbar-Werten neu indizieren.

 

> [!IMPORTANT]
> Die Hauptversion wurde in Windows 8 geändert. Daten, die unter früheren Versionen von Windows erstellt wurden, müssen neu indiziert werden.

 

Sowohl die definierte Version als auch die NLS-Version gelten für sortierbare Code Punkte, die mithilfe der [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) -oder [**lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) -Funktion mit dem lcmap \_ SortKey-Flag abgerufen und auch von den Funktionen [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)und [**findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) verwendet werden. Wenn ein oder mehrere Code Punkte in einer Zeichenfolge Unsortable sind, gibt die [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) -Funktion **false** zurück, wenn diese Zeichenfolge als Parameter übergeben wird.

Die Anwendung kann entweder [**getnlsversion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) oder [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortier Tabelle abzurufen.

## <a name="index-the-database"></a>Indizieren der Datenbank

Aus Leistungsgründen sollte die Anwendung dieses Verfahren befolgen, wenn Sie die Datenbank indizieren.

**So indizieren Sie die Datenbank ordnungsgemäß**

1.  Speichern Sie für jede Funktion die NLS-Version, die Sortierschlüssel dieser Version und eine Angabe der Sortier barkeit für jede indizierte Zeichenfolge.
2.  Wenn die neben Versions Zunahme Inkrementen ist, indizieren Sie zuvor nicht sortierbar-Zeichen folgen neu. Die in diesem Update betroffenen Zeichen folgen sollten auf diejenigen beschränkt werden, für die [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) zuvor **false** zurückgegeben hat.
3.  Wenn die Hauptversion erhöht wird, indizieren Sie alle Zeichen folgen neu, da die aktualisierten Gewichtungen das Verhalten einer beliebigen Zeichenfolge ändern können. Haupt Versions Releases sind sehr selten.

Probleme mit der Daten Bank Indizierung können aus folgenden Gründen auftreten:

-   Ein späteres Betriebssystem kann Code Punkte definieren, die für ein früheres Betriebssystem nicht definiert sind. Dadurch wird die Sortierung geändert.
-   Code Punkte können aufgrund von Korrekturen in der Sprachunterstützung verschiedene Sortierungs Gewichtungen in verschiedenen Betriebssystemen aufweisen.

Um die Notwendigkeit zu minimieren, dass die Datenbank in diesen Fällen neu indiziert werden kann, kann die Anwendung [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) verwenden, um die Definition von nicht definierten Zeichen folgen zu unterscheiden, sodass die Anwendung Zeichen folgen mit nicht definierten Code Punkten ablehnen kann. Durch die Verwendung von [**getnlsversion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) oder [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) kann die Anwendung bestimmen, ob sich eine NLS-Änderung auf das für eine bestimmte Indextabelle verwendete Gebiets Schema auswirkt. Wenn die Änderung keine Auswirkungen auf das Gebiets Schema hat, muss die Anwendung die Tabelle nicht neu indizieren.

## <a name="examples"></a>Beispiele

In der folgenden Tabelle werden die Auswirkungen bestimmter Flags veranschaulicht, die mit den Sortierfunktionen verwendet werden. In jedem Fall bestimmt die Auswahl der Flags, ob zwei verschiedene Zeichen zu Sortier Zwecken als gleich betrachtet werden.



| Zeichen 1                                                        | Zeichen 2                                             | Standard | Norm \_ IgnoreWidth | Norm \_ ignorekana | Norm \_ IgnoreWidth \| Normignorekana |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U + 3042 Hiragana-Buchstabe A<br/>                | "ガ"<br/> U + 30A2 Katakana-Buchstabe A<br/>     | Ungleich | Ungleich           | Equal            | Equal                              |
| "ｵ"<br/> U + FF75 halbwidth Katakana-Buchstabe O<br/>       | "オ"<br/> U + 30aa Katakana-Buchstabe O<br/>     | Ungleich | Equal             | Ungleich          | Equal                              |
| B<br/> U + FF22 vollwidth Lateinische Großbuchstaben B<br/> | „B“<br/> U + 0042 Lateinische Großbuchstaben B<br/> | Ungleich | Equal             | Ungleich          | Equal                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Sortierung](sorting.md)
</dt> <dt>

[Abrufen und Festlegen von Gebiets Schema Informationen](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Verwenden der Unicode-Normalisierung zur Darstellung von Zeichen folgen](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Überlegungen zur Sicherheit: Internationale Features](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**Comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**Findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**Findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**Lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
