---
description: Unicode ist ein weltweiter Zeichencodierungsstandard. Das System verwendet Unicode ausschließlich für die Zeichen- und Zeichenfolgenbearbeitung. Eine ausführliche Beschreibung aller Aspekte von Unicode finden Sie unter Der Unicode-Standard.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99a7af4d4fbb6b7783f97ceba37b1bf6b0bf54811beaf9c7c2348ec0125c73b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764770"
---
# <a name="unicode"></a>Unicode

Unicode ist ein weltweiter Zeichencodierungsstandard. Das System verwendet Unicode ausschließlich für die Zeichen- und Zeichenfolgenbearbeitung. Eine ausführliche Beschreibung aller Aspekte von Unicode finden Sie unter [Der Unicode-Standard.](https://www.unicode.org/standard/standard.html)

Im Vergleich zu älteren Mechanismen für die Behandlung von Zeichen- und Zeichenfolgendaten vereinfacht Unicode die Softwarelokalisierung und verbessert die mehrsprachige Textverarbeitung. Indem Sie Unicode verwenden, um Zeichen- und Zeichenfolgendaten in Ihren Anwendungen darzustellen, können Sie universelle Datenaustauschfunktionen für globales Marketing aktivieren, indem Sie eine einzelne Binärdatei für jeden möglichen Zeichencode verwenden. Unicode führt folgende Schritte aus:

-   Ermöglicht, dass jede Kombination von Zeichen, die aus einer beliebigen Kombination von Skripts und Sprachen gezeichnet werden, in einem einzigen Dokument nebeneinander vorhanden ist.
-   Definiert Semantik für jedes Zeichen.
-   Standardisiert das Skriptverhalten.
-   Stellt einen Standardalgorithmus für bidirektionalen Text bereit.
-   Definiert Kreuzzuordnungen zu anderen Standards.
-   Definiert mehrere Codierungen des einzelnen Zeichensatzes: UTF-7, UTF-8, UTF-16 und UTF-32. Die Konvertierung von Daten zwischen diesen Codierungen ist verlustfrei.

Unicode unterstützt zahlreiche Skripts, die von Sprachen auf der ganzen Welt verwendet werden, sowie eine große Anzahl von technischen Symbolen und Sonderzeichen, die bei der Veröffentlichung verwendet werden. Zu den unterstützten Skripts zählen unter anderem Lateinisch, Griechisch, Kyrillisch, Hebräisch, Arabisch, Devanagari, Thai, Han, Hangul, Hiragana und Katakana. Unterstützte Sprachen sind u. a. Deutsch, Französisch, Englisch, Griechisch, Russisch, Hebräisch, Arabisch, Hindi, Thai, Chinesisch, Koreanisch und Japanisch. Unicode kann derzeit die große Mehrheit der Zeichen in der modernen Computerverwendung auf der ganzen Welt darstellen und wird weiterhin aktualisiert, um sie noch vollständiger zu gestalten.

Unicode-fähige Funktionen werden unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)beschrieben. Diese Funktionen verwenden die UTF-16-Codierung (Breitzeichen), die die gängigste Codierung von Unicode und die für die native Unicode-Codierung auf Windows Betriebssystemen verwendet wird. Jeder Codewert ist 16 Bit breit, im Gegensatz zum älteren [Codepageansatz](code-pages.md) für Zeichen- und Zeichenfolgendaten, der 8-Bit-Codewerte verwendet. Die Verwendung von 16 Bits ermöglicht die direkte Codierung von 65.536 Zeichen. Tatsächlich ist das Universe der Symbole, die zum Transkribieren von menschlichen Sprachen verwendet werden, noch größer, und UTF-16-Codepunkte im Bereich U+D800 bis U+DFFF werden verwendet, um Ersatzzeichenpaare zu bilden, die 32-Bit-Codierungen ergänzender Zeichen bilden. Weitere Informationen finden Sie unter [Ersatzzeichen und ergänzende Zeichen.](surrogates-and-supplementary-characters.md)

Der Unicode-Zeichensatz enthält zahlreiche Kombinationszeichen, z.B. U+0308 ("oa"), eine kombinationsende Dieresis oder umlaut. Unicode kann häufig das gleiche Symbol entweder in einer Form "'composed'" oder ''decomposed'' darstellen: Die zusammengesetzte Form von "Ä" ist beispielsweise der einzelne Unicode-Codepunkt "Ä" (U+00C4), während die zerlegte Form "A" + " sstelle" (U+0041 U+0308) ist. Unicode definiert kein zusammengesetztes Formular für jedes Glyphen. Beispielsweise wird der "o"-Kleinbuchstabe "o" mit "umfangsflex" und tilde ("ỗ") durch U+006f U+0302 U+0303 (o + Klammer + Tilde) dargestellt. Weitere Informationen zum Kombinieren von Zeichen und verwandten Problemen finden Sie unter Verwenden der [Unicode-Normalisierung zum Darstellen von Zeichenfolgen.](using-unicode-normalization-to-represent-strings.md)

Zur Kompatibilität mit 8-Bit- und 7-Bit-Umgebungen kann Unicode auch als UTF-8 bzw. UTF-7 codiert werden. Unicode-fähige Funktionen in Windows UTF-16 verwenden, aber es ist auch möglich, mit In UTF-8 oder UTF-7 codierten Daten zu arbeiten, die in Windows als [Codepages](code-pages.md)mit Multibytezeichensatz unterstützt werden.

Neue Windows Anwendungen sollten UTF-16 als interne Datendarstellung verwenden. Windows bietet auch umfassende Unterstützung für Codepages, und eine gemischte Verwendung in derselben Anwendung ist möglich. Selbst neue Unicode-basierte Anwendungen müssen manchmal mit Codepages arbeiten. Die Gründe hierfür werden unter [Codepages](code-pages.md)erläutert.

Eine Anwendung kann die Funktionen [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um Zeichenfolgen basierend auf Codepages und Unicode-Zeichenfolgen zu konvertieren. Obwohl ihre Namen auf "MultiByte" verweisen, funktionieren diese Funktionen gleichermaßen gut mit [Einzelbyte-Zeichensatz (Single-Byte Character Set,](single-byte-character-sets.md) SBCS), [Doppelbyte-Zeichensatz (DOUBLE-Byte Character Set,](double-byte-character-sets.md) DBCS) und Multibyte-Zeichensatzcodepages (MBCS).

In der Regel sollte eine Windows Anwendung intern UTF-16 verwenden und nur als Teil einer "schlanken Schicht" über die Schnittstelle konvertieren, die ein anderes Format verwenden muss. Diese Technik schützt vor Datenverlust und -beschädigung. Jede Codepage unterstützt unterschiedliche Zeichen, aber keine von ihnen unterstützt das gesamte Spektrum von Zeichen, die von Unicode bereitgestellt werden. Die meisten Codepages unterstützen unterschiedliche Teilmengen, die unterschiedlich codiert sind. Die Codepages für UTF-8 und UTF-7 stellen eine Ausnahme dar, da sie den vollständigen Unicode-Zeichensatz unterstützen und die Konvertierung zwischen diesen Codierungen und UTF-16 verlustfrei ist.

Daten, die direkt aus der von einer Codepage verwendeten Codierung in die von einer anderen verwendete Codierung konvertiert werden, sind beschädigt, da der gleiche Datenwert auf verschiedenen Codepages ein anderes Zeichen codieren kann. Auch wenn Ihre Anwendung so nah wie möglich an der Schnittstelle konvertiert wird, sollten Sie sorgfältig über den zu behandelnden Datenbereich nachdenken.

Daten, die aus Unicode in eine Codepage konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes Zeichen darstellen kann, das in diesen bestimmten Unicode-Daten verwendet wird. Beachten Sie daher, dass [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) einige Daten verlieren kann, wenn die Zielcodepage nicht alle Zeichen in der Unicode-Zeichenfolge darstellen kann.

Bei der Modernisierung von codeseitenbasierten Legacyanwendungen für die Verwendung von Unicode können Sie generische Funktionen und das [**TEXT-Makro**](/windows/win32/api/Winnt/nf-winnt-text) verwenden, um einen einzelnen Satz von Quellen zu verwalten, aus denen zwei Versionen Ihrer Anwendung kompiliert werden können. Eine Version unterstützt Unicode, die andere funktioniert mit Windows Codepages. Mit diesem Mechanismus können Sie auch sehr große Anwendungen von Windows Codepages in Unicode konvertieren und gleichzeitig Anwendungsquellen beibehalten, die in allen Phasen der Konvertierung kompiliert, erstellt und getestet werden können. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen.](conventions-for-function-prototypes.md)

Unicode-Zeichen und -Zeichenfolgen verwenden Datentypen, die sich von denen für codepagebasierte Zeichen und Zeichenfolgen unterscheiden. Zusammen mit einer Reihe von Makros und Namenskonventionen minimiert diese Unterscheidung die Wahrscheinlichkeit, dass versehentlich die beiden Typen von Zeichendaten kombiniert werden. Sie erleichtert die Überprüfung des Compilertyps, um sicherzustellen, dass nur Unicode-Parameterwerte mit Funktionen verwendet werden, die Unicode-Zeichenfolgen erwarten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Sortierung](sorting.md)
</dt> <dt>

[Surrogate und ergänzende Zeichen](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



