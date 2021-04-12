---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit internationalen Support Features.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Überlegungen zur Sicherheit: Internationale Features'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb9f8b849e9fb1a07f01031832449b9c9027ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218549"
---
# <a name="security-considerations-international-features"></a>Überlegungen zur Sicherheit: Internationale Features

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit internationalen Support Features. Sie können Sie als Ausgangspunkt verwenden und dann die Dokumentation für die internationale Technologie von Interesse für technologiespezifische Sicherheitsüberlegungen ansehen.

Dieses Thema enthält folgende Abschnitte:

-   [Sicherheitsüberlegungen für Zeichen Konvertierungs Funktionen](#security-considerations-for-character-conversion-functions)
-   [Sicherheitsüberlegungen für Vergleichsfunktionen](#security-considerations-for-comparison-functions)
-   [Sicherheitsüberlegungen für Zeichensätze in Dateinamen](#security-considerations-for-character-sets-in-file-names)
-   [Sicherheitsüberlegungen für internationalisierte Domänen Namen](#security-considerations-for-internationalized-domain-names)
-   [Sicherheitsüberlegungen für ANSI-Funktionen](#security-considerations-for-ansi-functions)
-   [Sicherheitsüberlegungen für die Unicode-Normalisierung](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Sicherheitsüberlegungen für Zeichen Konvertierungs Funktionen

" [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) " und " [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) " sind die Unicode-und Zeichensatz Funktionen, die am häufigsten zum Konvertieren von Zeichen zwischen ANSI und Unicode verwendet werden. Diese Funktionen haben das Potenzial, Sicherheitsrisiken zu verursachen, da Sie die Elemente der Eingabe-und Ausgabepuffer anders zählen. Beispielsweise nimmt [**multibyteeswidechar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) einen in Bytes gezählten Eingabepuffer an und versetzt die konvertierten Zeichen in eine Puffergröße in Unicode-Zeichen. Wenn Ihre Anwendung diese Funktion verwendet, muss Sie die Puffer ordnungsgemäß verkleinern, um einen Pufferüberlauf zu vermeiden.

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) ist standardmäßig auf die "beste Anpassung"-Zuordnung für Codepages, z. b. 1252. Diese Art von Zuordnung ermöglicht jedoch mehrere Darstellungen derselben Zeichenfolge, sodass die Anwendung möglicherweise anfällig für Angriffe wird. Beispielsweise kann der lateinische Großbuchstabe a mit der Dieresis ("Ä") dem lateinischen Großbuchstaben a ("a") zugeordnet werden. ein Unicode-Zeichen in einer asiatischen Sprache kann einem Schrägstrich ("/") zugeordnet werden. Die Verwendung des Flags "WC \_ No \_ Best \_ fit \_ chars" wird aus Sicherheitsgründen bevorzugt.

Einige Codepages, z. b. die Codepages 5022x (ISO-2022-x), sind grundsätzlich unsicher, da Sie mehrere Darstellungen derselben Zeichenfolge zulassen. Ordnungsgemäß geschriebener Code führt Sicherheitsüberprüfungen im Unicode-Format durch. diese Typen von Codepages erweitern jedoch die Angriffs Anfälligkeit ihrer Anwendungen und sollten nach Möglichkeit vermieden werden.

## <a name="security-considerations-for-comparison-functions"></a>Sicherheitsüberlegungen für Vergleichsfunktionen

Zeichen folgen Vergleiche können Sicherheitsprobleme darstellen. Da alle Vergleichsfunktionen etwas verschieden sind, meldet eine Funktion möglicherweise zwei Zeichen folgen als gleich, während Sie von einer anderen Funktion unterschiedlich betrachtet werden können. Die folgenden Funktionen können von Ihren Anwendungen zum Vergleichen von Zeichen folgen verwendet werden:

-   [lstrincmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Vergleicht zwei Zeichen folgen gemäß den Regeln des Gebiets Schemas ohne Berücksichtigung der Groß-/Kleinschreibung. Die-Funktion vergleicht die Zeichen folgen, indem die ersten Zeichen gegenseitig überprüft werden, die zweiten Zeichen gegenseitig usw., bis eine Ungleichheit gefunden wird oder die Enden der Zeichen folgen erreicht werden.
-   [lstraucmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Vergleicht Zeichen folgen mit ähnlichen Techniken wie [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Der einzige Unterschied besteht darin, dass [lstraucmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) einen Zeichen folgen Vergleich mit Berücksichtigung von Groß-und Kleinschreibung
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista und höher). Führt einen Zeichen folgen Vergleich für ein vom Anwendungs bereitgestelltes Gebiets Schema aus. [**Comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ähnelt [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), identifiziert aber ein Gebiets Schema anhand des Gebiets Schema [namens](locale-names.md) anstelle des Gebiets Schema [Bezeichners](locale-identifiers.md). Diese Funktionen ähneln [lstrincmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) und [lstraucmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) , mit dem Unterschied, dass Sie anstelle eines vom Benutzer ausgewählten Gebiets Schemas auf einem bestimmten Gebiets Schema arbeiten.
-   [**Comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista und höher). Vergleicht zwei Unicode-Zeichen folgen, um binäre Äquivalenz zu testen. Mit Ausnahme der Option, dass die Groß-/Kleinschreibung nicht beachtet wird, ignoriert diese Funktion alle nicht binären äquivalente und testet alle Code Punkte auf Gleichheit, einschließlich der Code Punkte, die in linguistischen [Sortier](sorting.md) Schemas keine Gewichtung erhalten. Beachten Sie, dass die anderen in diesem Thema erwähnten Vergleichsfunktionen nicht alle Code Punkte auf Gleichheit testen.
-   [**Findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista und höher). Eine Unicode-Zeichenfolge in einer anderen Unicode-Zeichenfolge suchen. " [**Findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) " ähnelt " [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)", mit dem Unterschied, dass ein Gebiets Schema nach Gebiets Schema Namen anstelle des Gebiets Schema Bezeichners identifiziert wird.
-   [**Findstringordinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 und höher). Gibt eine Unicode-Zeichenfolge in einer anderen Unicode-Zeichenfolge an. Die Anwendung sollte diese Funktion anstelle von [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) für alle nicht linguistischen Vergleiche verwenden.

Wie [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) und [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)wertet [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) Zeichen folgen Zeichen nach Zeichen aus. Viele Sprachen haben jedoch Elemente mit mehreren Zeichen, z. b. das zwei-Zeichen-Element "ch" in traditionellem Spanisch. Da [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) das von der Anwendung bereitgestellten Gebiets Schema verwendet, um mehrere Zeichen Elemente zu identifizieren, und [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) und [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) das Thread Gebiets Schema verwenden, können identische Zeichen folgen nicht als gleich verglichen werden.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignoriert nicht definierte Zeichen und gibt folglich 0 (null) für viele Zeichen folgen Paare zurück, die sehr unterschiedlich sind. Eine Zeichenfolge kann Werte enthalten, die keinem Zeichen zugeordnet sind, oder Zeichen mit Semantik außerhalb der Domäne der Anwendung enthalten, wie z. b. Steuerzeichen in einer URL. Anwendungen, die diese Funktion verwenden, sollten Fehlerhandler und Test Zeichenfolgen bereitstellen, um sicherzustellen, dass Sie gültig sind, bevor Sie verwendet werden.

> [!Note]  
> Für Windows Vista und höher ähnelt [**comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Die Sicherheitsprobleme sind für diese Funktionen identisch.

 

Ähnliche Sicherheitsprobleme gelten für Funktionen wie [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), die implizite Vergleiche durchführen. Abhängig von den festgelegten Flags können die Ergebnisse des Abrufens von [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) für die Suche nach einer Zeichenfolge in einer anderen Zeichenfolge beträchtlich abweichen.

> [!Note]  
> Für Windows Vista und höher ist " [**findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) " vergleichbar mit " [**findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)". Die Sicherheitsprobleme sind für diese Funktionen identisch.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Sicherheitsüberlegungen für Zeichensätze in Dateinamen

Windows-Codepage-und OEM-Zeichensätze, die auf Systemen japanischer Sprache verwendet werden, enthalten das Yen-Symbol (Yen) anstelle eines umgekehrten Schrägstrichs ( \\ ). Daher ist das Yen-Zeichen ein unzulässiges Zeichen für NTFS-und FAT-Dateisysteme. Bei der Zuordnung von Unicode zu einer japanischen Codepage ordnen Konvertierungs Funktionen den umgekehrten Schrägstrich (u + 005c) und das normale Unicode-Yen-Symbol (u + 00a5) dem gleichen Zeichen zu. Aus Sicherheitsgründen sollten Ihre Anwendungen in der Regel nicht das Zeichen U + 00a5 in einer Unicode-Zeichenfolge zulassen, die zur Verwendung als FAT-Dateinamen konvertiert werden kann.

## <a name="security-considerations-for-internationalized-domain-names"></a>Sicherheitsüberlegungen für internationalisierte Domänen Namen

Internationalisierte Domänen Namen (Internationalized Domain Names, IDNs) werden von der Netzwerk Arbeitsgruppe [RFC 3490: internationalisieren von Domänen Namen in Anwendungen (IDNA)](http://www.faqs.org/rfcs/rfc3490.html)angegeben. Der Standard führt zu einer Reihe von Sicherheitsproblemen.

Symbole, die bestimmte Zeichen aus unterschiedlichen Skripts darstellen, können ähnlich oder sogar identisch erscheinen. Beispielsweise ist in vielen Schriftarten Kyrillisch Kleinbuchstaben a ("a") nicht von lateinischen Kleinbuchstaben a ("a") zu unterscheiden. Es gibt keine Möglichkeit, visuell zu erkennen, dass "example.com" und "example.com" zwei verschiedene Domänen Namen sind, eine mit einem lateinischen Kleinbuchstaben a im Namen, der andere mit einem kyrillischen Kleinbuchstaben a. Eine skrupellose Host Site kann diese visuelle Mehrdeutigkeit verwenden, um zu verhindern, dass eine andere Website in einem Spoofing-Angriff verwendet wird.

Der erweiterte Zeichensatz, den IDNA für IDNs zulässt, verfügt in einem bestimmten Skript auch über Spoofing-Möglichkeiten. Beispielsweise gibt es eine starke Ähnlichkeit zwischen dem Bindestrich ("-" U + 002D), der Bindestrich ("–" u + 2010), der nicht unterbrechende Bindestrich ("-" u + 2011), der Abbildung Strich ("\u2012" u + 2012), der "en Dash" ("–" u + 2013) und das Minuszeichen ("−" u + 2212).

Ähnliche Probleme ergeben sich aus bestimmten Kompatibilitäts Kompositionen. Beispielsweise wird die einzelne Unicode-Zeichen Nummer 20 vollständige Beendigung ("20.", U + 249b) in "20" konvertiert. (U + 0032 u + 0030 u + 002e) in einem Nameprep-Schritt vor der Konvertierung in Punycode. Mit anderen Worten: diese Komposition fügt einen Punkt (vollständiges Ende) ein. Solche Kompositionen haben Spoofing-Möglichkeiten.

Das Kombinieren verschiedener Skripts in einem IDN deutet nicht notwendigerweise auf Spoofing oder irreführende Absicht hin. [Technischer Bericht \# 36: bei Unicode-Sicherheitsüberlegungen](https://www.unicode.org/reports/tr36/#international_domain_names) sind einige Beispiele für angemessene IDNs enthalten, die eine Mischung aus Skripts enthalten, wie z. b. xml-"--", "-".

Spoofing-Angriffe sind nicht auf IDNs beschränkt. Beispiel: "rnicrosoft.com" sieht in etwa wie folgt aus: "Microsoft.com", aber es handelt sich um einen ASCII-Namen. Außerdem kann ein spoofinganangriff durch eine Beschädigung eines Namens durchgeführt werden. Das Hinzufügen zusätzlicher Bezeichnungen nach einem bekannten Markennamen oder das Einschließen des Marken namens im Pfad einer URL, die als sicher gekennzeichnet ist, kann Anfänger und unabhängig von der Verwendung des IDN verwirren. Bei manchen Gebiets Schemas sind IDNs erforderlich, und das Punycode-Format dieser Namen ist nicht akzeptabel, da die Namen wie giberish aussehen.

Weitere Informationen zu den hier erwähnten Sicherheitsproblemen sowie eine große Anzahl anderer Probleme, die für IDNA relevant sind, finden Sie unter [technischer Bericht \# 36: Sicherheitsüberlegungen für Unicode](https://www.unicode.org/reports/tr36/#international_domain_names). Dieser Bericht enthält zusammen mit ausführlichen Erörterung von IDNA-bezogenen Sicherheitsproblemen Vorschläge für den Umgang mit verdächtigen IDNs in Ihren Anwendungen.

## <a name="security-considerations-for-ansi-functions"></a>Sicherheitsüberlegungen für ANSI-Funktionen

> [!Note]  
> Es wird empfohlen, Unicode in ihren globalisieren zu verwenden, insbesondere in neuen, wenn dies möglich ist. ANSI-Funktionen sollten nur verwendet werden, wenn Sie Gründe für die Verwendung von Unicode überschreiben, z. b. die Konformität mit einem älteren Protokoll, das Unicode nicht unterstützt.

 

Viele nls-Funktionen (National Language Support), wie z. b. [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), haben bestimmte ANSI-Versionen, in diesem Fall **getlocaleinfoa** bzw. **getcalendarinfoa**. Wenn Ihre Anwendung die ANSI-Version einer Funktion mit einem Unicode-basierten Betriebssystem verwendet, z. b. Windows NT, Windows 2000, Windows XP oder Windows Vista, kann die Funktion fehlschlagen oder nicht definierte Ergebnisse erzeugen. Wenn Sie einen überzeugenden Grund für die Verwendung von ANSI-Funktionen mit einem solchen Betriebssystem haben, stellen Sie sicher, dass die von der Anwendung über gebenden Daten für ANSI gültig sind.

## <a name="security-considerations-for-unicode-normalization"></a>Sicherheitsüberlegungen für die Unicode-Normalisierung

Da die Unicode-Normalisierung die Form einer Zeichenfolge ändern kann, sollten Sicherheitsmechanismen oder Zeichen Validierungs Algorithmen in der Regel nach der Normalisierung implementiert werden. Angenommen, eine Anwendung mit einer Weboberfläche akzeptiert einen Dateinamen, akzeptiert aber keinen Pfadnamen. Eine Breite von u + FF43 u + FF1A u + FF3C u + FF57 u + FF49 u + FF4E u + FF44 u + FF4F u + FF57 u + FF53 `(c : \ w i n d o w s)` ändert sich in u + 0063 u + 001A u + 003c u + 0077 u + 0069 u + 006e u + 0064 u + 006f U + 0077 u + 0073 `(c:\windows)` with Form KC Normalisierung. Wenn eine Anwendung auf das vorhanden sein des Doppelpunkts und umgekehrter Schrägstriche prüft, bevor Sie Normalisierungen implementiert, kann das Ergebnis unbeabsichtigter Dateizugriff sein.

Obwohl die Unicode-Normalisierung ein Element bei der Sicherheit von Betriebssystemen ist, sollten Sie Bedenken, dass die Normalisierung keine Ersetzung für eine umfassende Sicherheitsrichtlinie ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In Dateinamen verwendete Zeichensätze](character-sets-used-in-file-names.md)
</dt> <dt>

[Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)
</dt> <dt>

[Behandeln von Sortierungen in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[Umgang mit internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
