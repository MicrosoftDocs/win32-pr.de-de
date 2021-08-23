---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit International Support-Features.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Sicherheitsüberlegungen: Internationale Features'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e61566fdf51b80a76e5c8997018f35ce421dee6dd0e1b9e290888d96576249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147043"
---
# <a name="security-considerations-international-features"></a>Sicherheitsüberlegungen: Internationale Features

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit International Support-Features. Sie können es als Ausgangspunkt verwenden und dann die Dokumentation für die internationale Technologie von Interesse für technologiespezifische Sicherheitsüberlegungen lesen.

Dieses Thema enthält folgende Abschnitte:

-   [Sicherheitsüberlegungen für Zeichenkonvertierungsfunktionen](#security-considerations-for-character-conversion-functions)
-   [Sicherheitsüberlegungen für Vergleichsfunktionen](#security-considerations-for-comparison-functions)
-   [Sicherheitsüberlegungen für Zeichensätze in Dateinamen](#security-considerations-for-character-sets-in-file-names)
-   [Sicherheitsüberlegungen für internationalisierte Domänennamen](#security-considerations-for-internationalized-domain-names)
-   [Sicherheitsüberlegungen für ANSI-Funktionen](#security-considerations-for-ansi-functions)
-   [Sicherheitsüberlegungen zur Unicode-Normalisierung](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Sicherheitsüberlegungen für Zeichenkonvertierungsfunktionen

[**MultiByteToWideChar und**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) sind die Unicode- und Zeichensatzfunktionen, die am häufigsten zum Konvertieren von Zeichen zwischen ANSI und Unicode verwendet werden. Diese Funktionen können Sicherheitsrisiken verursachen, da sie die Elemente der Eingabe- und Ausgabepuffer unterschiedlich zählen. Beispielsweise verwendet [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) einen Eingabepuffer, der in Bytes gezählt wird, und setzt die konvertierten Zeichen in einen Puffer mit Unicode-Zeichengröße. Wenn Ihre Anwendung diese Funktion verwendet, muss sie die Größe der Puffer richtig sgrößeren, um einen Pufferüberlauf zu vermeiden.

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwendet standardmäßig die Zuordnung "am besten geeignet" für Codepages, z. B. 1252. Diese Art von Zuordnung ermöglicht jedoch mehrere Darstellungen derselben Zeichenfolge, was ihre Anwendung potenziell anfällig für Angriffe macht. Beispielsweise kann der lateinische Großbuchstaben A mit der Dieresis ("Ä") dem lateinischen Großbuchstaben A ("A") zuordnen. Ein Unicode-Zeichen in einer asienstischen Sprache kann einem Schrägstrich ("/") zuordnen. Die Verwendung des WC \_ NO \_ BEST FIT \_ \_ CHARS-Flags wird aus Sicherheitssicht bevorzugt.

Einige Codepages, z. B. die 5022x-Codepages (iso-2022-x), sind grundsätzlich unsicher, da sie mehrere Darstellungen derselben Zeichenfolge zulassen. Ordnungsgemäß geschriebener Code führt Sicherheitsüberprüfungen im Unicode-Format durch. Diese Arten von Codepages erweitern jedoch die Angriffsanfälligkeit Ihrer Anwendungen und sollten nach Möglichkeit vermieden werden.

## <a name="security-considerations-for-comparison-functions"></a>Sicherheitsüberlegungen für Vergleichsfunktionen

Zeichenfolgenvergleiche können zu Sicherheitsproblemen führen. Da sich alle Vergleichsfunktionen geringfügig unterscheiden, kann eine Funktion zwei Zeichenfolgen als gleich melden, während eine andere Funktion sie als unterschiedlich betrachten könnte. Im Folgenden finden Sie mehrere Funktionen, die Ihre Anwendungen zum Vergleichen von Zeichenfolgen verwenden können:

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Vergleicht zwei Zeichenfolgen gemäß den Regeln des -Locale ohne Unterschiedliche Zeichenfolgen. Die -Funktion vergleicht die Zeichenfolgen, indem sie die ersten Zeichen miteinander, die zweiten Zeichen miteinander und so weiter überprüft, bis sie eine Ungleichheit findet oder die Enden der Zeichenfolgen erreicht.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Vergleicht Zeichenfolgen mit techniken, die denen von [lstrcmpi ähneln.](/windows/win32/api/winbase/nf-winbase-lstrcmpia) Der einzige Unterschied ist, dass [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) einen Zeichenfolgenvergleich durchführt, bei dem die Zeichenfolgenschreibung beachtet wird.
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista und höher). Führen Sie einen Zeichenfolgenvergleich für ein von der Anwendung bereitgestelltes Locale durch. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ähnelt [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), identifiziert jedoch ein [Locale](locale-names.md) durch den Namen des Locale anstelle des [Locale Identifiers.](locale-identifiers.md) Diese Funktionen ähneln [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) und [lstrcmp,](/windows/win32/api/winbase/nf-winbase-lstrcmpa) mit dem Ausnahme, dass sie für ein bestimmtes Locale und nicht für ein vom Benutzer ausgewähltes Locale verwendet werden.
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista und höher). Vergleicht zwei Unicode-Zeichenfolgen, um binäre Äquivalenz zu testen. Mit Ausnahme der Option, bei der die Groß-/Kleinschreibung nicht beachtet wird, ignoriert diese Funktion alle nicht binären Äquivalenzen und testet alle Codepunkte auf Gleichheit, einschließlich Codepunkte, die in linguistischen Sortierungsschemas nicht gewichtet werden. [](sorting.md) Beachten Sie, dass die anderen in diesem Thema erwähnten Vergleichsfunktionen nicht alle Codepunkte auf Gleichheit testen.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista und höher). Suchen Sie eine Unicode-Zeichenfolge in einer anderen Unicode-Zeichenfolge. [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) ähnelt [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), mit der Ausnahme, dass ein Locale durch den Namen des Locale anstelle des Locale Identifier identifiziert wird.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 und höher). Sucht eine Unicode-Zeichenfolge in einer anderen Unicode-Zeichenfolge. Die Anwendung sollte diese Funktion anstelle von [**FindNLSString für**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) alle nicht linguistischen Vergleiche verwenden.

Wie [lstrcmpi und](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**wertet CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) Zeichenfolgen Zeichen für Zeichen aus. Viele Sprachen verfügen jedoch über Elemente mit mehreren Zeichen, z. B. das zwei zeichenbasierte Element "CH" in traditionellem Spanisch. Da [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) das von der Anwendung geerbte Locale verwendet, um Elemente mit mehreren Zeichen zu identifizieren, und [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) und [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) das Thread-Locale verwenden, werden identische Zeichenfolgen möglicherweise nicht als gleich verglichen.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignoriert nicht definierte Zeichen und gibt daher 0 (null) für viele Zeichenfolgenpaare zurück, die eindeutig sind. Eine Zeichenfolge kann Werte enthalten, die keinen Zeichen oder Zeichen mit Semantik außerhalb der Domäne der Anwendung zuordnen, z. B. Steuerzeichen in einer URL. Anwendungen, die diese Funktion verwenden, sollten Fehlerhandler und Testzeichenfolgen bereitstellen, um sicherzustellen, dass sie gültig sind, bevor sie verwendet werden.

> [!Note]  
> Für Windows Vista und höher ähnelt [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**compareString .**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) Die Sicherheitsprobleme sind für diese Funktionen identisch.

 

Ähnliche Sicherheitsprobleme gelten für Funktionen wie [**FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)die implizite Vergleiche ausführen. Abhängig von den festgelegten Flags können sich die Ergebnisse des Aufrufs von [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) zum Suchen nach einer Zeichenfolge innerhalb einer anderen Zeichenfolge erheblich unterscheiden.

> [!Note]  
> Für Windows Vista und höher ähnelt [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). Die Sicherheitsprobleme sind für diese Funktionen identisch.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Sicherheitsüberlegungen für Zeichensätze in Dateinamen

Windows Codepage und OEM-Zeichensätze, die auf Systemen in japanischer Sprache verwendet werden, enthalten das Symbol "Symbols" ((*) anstelle eines schrägen Schrägstrichs ( \\ ). Daher ist das Zeichen "Gegen" ein unzulässiges Zeichen für NTFS- und FAT-Dateisysteme. Beim Zuordnen von Unicode zu einer Codepage in japanischer Sprache ordnen Konvertierungsfunktionen denselben Zeichen sowohl den schrägen Schrägstrich (U+005C) als auch das normale Unicode-Symbol (U+00A5) zu. Aus Sicherheitsgründen sollten Ihre Anwendungen in der Regel nicht das Zeichen U+00A5 in einer Unicode-Zeichenfolge zulassen, die zur Verwendung als FAT-Dateiname konvertiert werden kann.

## <a name="security-considerations-for-internationalized-domain-names"></a>Sicherheitsüberlegungen für internationalisierte Domänennamen

Internationalisierte Domänennamen (IDNs) werden von der Netzwerkarbeitsgruppe [RFC 3490: Internationalizing Domain Names in Applications (IDNA) angegeben.](http://www.faqs.org/rfcs/rfc3490.html) Der Standard führt zu einer Reihe von Sicherheitsproblemen.

Glyphen, die bestimmte Zeichen aus verschiedenen Skripts darstellen, können ähnlich oder sogar identisch erscheinen. In vielen Schriftarten ist kyrillischer Kleinbuchstabe A ("a") beispielsweise nicht von lateinischem Kleinbuchstaben A ("a") zu unterscheiden. Es gibt keine Möglichkeit, visuell zu erkennen, dass "example.com" und "example.com" zwei verschiedene Domänennamen sind: einen mit einem lateinischen Kleinbuchstaben A im Namen, der andere mit kyrillischem Kleinbuchstaben A. Eine skrupellose Hostwebsite kann diese visuelle Mehrdeutigkeit verwenden, um vorzugeben, dass sie eine andere Website bei einem Spoofingangriff ist.

Der erweiterte Zeichensatz, den IDNA für IDNs zulässt, hat auch spoofing-Potenzial innerhalb eines bestimmten Skripts. Beispiel: es gibt eine starke Ähnlichkeit zwischen dem Bindestrich-Minus ("-" U+002D), dem Bindestrich ("—" U+2010), dem nicht brechenden Bindestrich ("-" U+20)11), den Strich ("\u2012" U+2012), den en-Bindestrich ("–" U+2013) und das Minuszeichen ("−" U+2212).

Ähnliche Probleme treten bei bestimmten Kompatibilitätskompositionen auf. Beispielsweise wird das einzelne Unicode-Zeichen NUMBER TWENTY FULL STOP ("20.", U+249B) in "20" konvertiert. (U+0032 U+0030 U+002E) in einem NamePrep-Schritt vor der Konvertierung in Punycode. Anders ausgedrückt: Diese Komposition fügt einen Zeitraum ein (vollständiger Stopp). Solche Kompositionen haben Spoofingpotenzial.

Das Mischen verschiedener Skripts in einem IDN deutet nicht notwendigerweise auf Spoofing- oder Absichtsabsichten hin. Technischer Bericht [ \# 36: Sicherheitsüberlegungen](https://www.unicode.org/reports/tr36/#international_domain_names) zu Unicode enthält mehrere Beispiele für sinnvolle IDNs, die eine Mischung aus Skripts enthalten, z.B. XML- );

Spoofingangriffe sind nicht auf IDNs beschränkt. Beispielsweise sieht "rnicrosoft.com" ähnlich wie "microsoft.com" aus, ist aber ein ASCII-Name. Darüber hinaus kann ein Spoofingangriff durch Beschädigung eines Namens vorgenommen werden. Das Hinzufügen zusätzlicher Bezeichnungen nach einem bekannten Markennamen oder das Hinzufügen des Markennamens in den Pfad einer URL mit der Bezeichnung "Sicher" kann benutzerverwirrend sein, unabhängig von der Verwendung des IDN. Für einige Locales sind IDNs erforderlich, und die Punycode-Form dieser Namen ist nicht akzeptabel, da sie die Namen wie gibberish aussehen lassen.

Weitere Informationen zu den hier erwähnten Sicherheitsproblemen sowie eine große Anzahl anderer Probleme, die für IDNA relevant sind, finden Sie unter Technical Report 36: Unicode Security Considerations ( Technische Bericht [ \# 36: Unicode-Sicherheitsüberlegungen](https://www.unicode.org/reports/tr36/#international_domain_names)). Neben ausführlichen Erläuterungen zu IDNA-bezogenen Sicherheitsproblemen bietet dieser Bericht Vorschläge für den Umgang mit verdächtigen IDNs in Ihren Anwendungen.

## <a name="security-considerations-for-ansi-functions"></a>Sicherheitsüberlegungen für ANSI-Funktionen

> [!Note]  
> Es wird empfohlen, Unicode in Ihren globalisierten Anwendungen zu verwenden, insbesondere in neuen Anwendungen, wenn dies überhaupt möglich ist. Sie sollten ANSI-Funktionen nur verwenden, wenn Sie überschreibende Gründe dafür haben, Unicode nicht zu verwenden, z. B. konformität mit einem älteren Protokoll, das Unicode nicht unterstützt.

 

Viele NLS-Funktionen (National Language Support), z. B. [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**GetCalendarInfo,**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)verfügen über bestimmte ANSI-Versionen, in diesem Fall **GetLocaleInfoA** bzw. **GetCalendarInfoA.** Wenn Ihre Anwendung die ANSI-Version einer Funktion mit einem Unicode-basierten Betriebssystem wie Windows NT, Windows 2000, Windows XP oder Windows Vista verwendet, kann die Funktion fehlschlagen oder undefinierte Ergebnisse erzeugen. Wenn Sie einen überzeugenden Grund haben, ANSI-Funktionen mit einem solchen Betriebssystem zu verwenden, stellen Sie sicher, dass die von Ihrer Anwendung übergebenen Daten für ANSI gültig sind.

## <a name="security-considerations-for-unicode-normalization"></a>Sicherheitsüberlegungen zur Unicode-Normalisierung

Da die Unicode-Normalisierung die Form einer Zeichenfolge ändern kann, sollten Sicherheitsmechanismen oder Zeichenvalidierungsalgorithmen in der Regel nach der Normalisierung implementiert werden. Stellen Sie sich beispielsweise eine Anwendung mit einer Webschnittstelle vor, die einen Dateinamen akzeptiert, aber keinen Pfadnamen akzeptiert. Eine U+FF43 U+FF1A U+FF3C U+FF57 U+FF49 U+FF4E U+FF44 U+FF4F U+FF57 U+FF53 wird in `(c : \ w i n d o w s)` U+0063 U+0 geändert.01A U+003C U+0077 U+0069 U+006E U+0064 U+006F U+0077 U+0073 `(c:\windows)` mit KC-Normalisierung. Wenn eine Anwendung testet, ob der Doppelpunkt und der schräge Schrägstrich vor der Implementierung der Normalisierung vorliegen, kann das Ergebnis ein unbeabsichtigter Dateizugriff sein.

Während die Unicode-Normalisierung ein Element zur Sicherheit von Betriebssystemen ist, denken Sie daran, dass die Normalisierung kein Ersatz für eine umfassende Sicherheitsrichtlinie ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In Dateinamen verwendete Zeichensätze](character-sets-used-in-file-names.md)
</dt> <dt>

[Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)
</dt> <dt>

[Behandeln der Sortierung in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[Behandeln von internationalisierten Domänennamen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
