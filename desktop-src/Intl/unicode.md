---
description: Unicode ist ein weltweiter Zeichen Codierungsstandard. Das System verwendet Unicode exklusiv für Zeichen-und Zeichen folgen Bearbeitung. Eine ausführliche Beschreibung aller Aspekte von Unicode finden Sie unter Unicode-Standard.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88facae63fbb365fd6f38cb09464de735e0759b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354007"
---
# <a name="unicode"></a>Unicode

Unicode ist ein weltweiter Zeichen Codierungsstandard. Das System verwendet Unicode exklusiv für Zeichen-und Zeichen folgen Bearbeitung. Eine ausführliche Beschreibung aller Aspekte von Unicode finden Sie unter Unicode- [Standard](https://www.unicode.org/standard/standard.html).

Im Vergleich zu älteren Mechanismen für die Verarbeitung von Zeichen-und Zeichen folgen Daten vereinfacht Unicode die Softwarelokalisierung und verbessert die mehrsprachige Textverarbeitung. Wenn Sie Unicode zum Darstellen von Zeichen-und Zeichen folgen Daten in Ihren Anwendungen verwenden, können Sie universelle Datenaustauschfunktionen für globales Marketing aktivieren, indem Sie eine einzelne Binärdatei für jeden möglichen Zeichencode verwenden. Unicode führt folgende Aktionen aus:

-   Ermöglicht eine beliebige Kombination von Zeichen, die aus einer beliebigen Kombination von Skripts und Sprachen gezeichnet werden, in einem einzelnen Dokument nebeneinander.
-   Definiert die Semantik für jedes Zeichen.
-   Standardisiert das Skript Verhalten.
-   Stellt einen Standard Algorithmus für bidirektionalen Text bereit.
-   Definiert Zuordnungs übergreifende Zuordnungen zu anderen Standards.
-   Definiert mehrere Codierungen des einzelnen Zeichensatzes: UTF-7, UTF-8, UTF-16 und UTF-32. Die Konvertierung von Daten zwischen diesen Codierungen ist verlustfrei.

Unicode unterstützt zahlreiche Skripts, die von Sprachen weltweit verwendet werden, sowie eine große Anzahl von technischen Symbolen und Sonderzeichen, die bei der Veröffentlichung verwendet werden. Zu den unterstützten Skripts gehören die lateinischen, Greek, Kyrillisch, Hebräisch, Arabisch, der "de vanagari", "Thai", "Han", "Hangul", "Hiragana" und Katakana. Unterstützte Sprachen sind u. a. Deutsch, Französisch, Englisch, Griechisch, Russisch, Hebräisch, Arabisch, Hindi, Thailändisch, Chinesisch, Koreanisch und Japanisch. Unicode kann derzeit die große Mehrheit der Zeichen in der modernen Computer Verwendung auf der ganzen Welt darstellen und wird weiterhin aktualisiert, um den Vorgang noch besser abzuschließen.

Unicode-aktivierte Funktionen werden in [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)beschrieben. Diese Funktionen verwenden die UTF-16-Codierung (breit Zeichen), bei der es sich um die häufigste Codierung von Unicode handelt und die für die systemeigene Unicode-Codierung unter Windows-Betriebssystemen verwendet wird. Jeder Codewert ist 16 Bits breit, im Gegensatz zum älteren [Codepage](code-pages.md) -Ansatz für Zeichen-und Zeichen folgen Daten, die 8-Bit-Codewerte verwenden. Die Verwendung von 16 Bits ermöglicht die direkte Codierung von 65.536 Zeichen. Tatsächlich ist das Universum der Symbole, die zum transchreiben von Menschen Sprachen verwendet werden, noch größer als das, und UTF-16-Code Punkte im Bereich u + D800 und bis u + DFFF werden zum bilden von Ersatz Zeichen Paaren verwendet, die 32-Bit-Codierungen von ergänzenden Zeichen bilden. Weitere Erläuterungen finden Sie unter [Surrogates und ergänzende Zeichen](surrogates-and-supplementary-characters.md) .

Der Unicode-Zeichensatz umfasst zahlreiche Kombinations Zeichen, z. b. U + 0308 ("¤"), eine Kombination aus Dieresis oder "um". Unicode kann das gleiche Symbol häufig in einem ' ' zusammengesetzten ' ' oder einem ' ' aufgesetzten ' '-Formular darstellen: beispielsweise ist die zusammengesetzte Form von ' ä ' der einzige Unicode-Codepunkt "ä" (u + 00c4), während die zusammengesetzte Form "a" + "-" (u + 0041 U + 0308) ist. In Unicode wird kein zusammengesetztes Formular für jedes Symbol definiert. Beispielsweise wird der Vietnamese-"o" (Großbuchstaben "o") mit "umgeht" und "Tilde" ("ỗ") durch u + 006f u + 0302 U + 0303 (o + Umgehungs + Tilde) dargestellt. Weitere Informationen zum Kombinieren von Zeichen und verwandten Problemen finden [Sie unter Verwenden der Unicode-Normalisierung zur Darstellung](using-unicode-normalization-to-represent-strings.md)von Zeichen folgen.

Aus Kompatibilitätsgründen mit 8-Bit-und 7-Bit-Umgebungen kann Unicode auch als UTF-8-bzw. UTF-7-codiert werden. Obwohl Unicode-aktivierte Funktionen in Windows UTF-16 verwenden, ist es auch möglich, mit in UTF-8 oder UTF-7 codierten Daten zu arbeiten, die in Windows als Multibytezeichen-Zeichensatz- [Codepages](code-pages.md)unterstützt werden.

Neue Windows-Anwendungen sollten UTF-16 als interne Datendarstellung verwenden. Windows bietet auch umfangreiche Unterstützung für Codepages, und die gemischte Verwendung in der gleichen Anwendung ist möglich. Sogar neue Unicode-basierte Anwendungen müssen manchmal mit Codepages arbeiten. Gründe hierfür werden in [Codepages](code-pages.md)erläutert.

Eine Anwendung kann die Funktionen [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um Zeichen folgen auf der Grundlage von Codepages und Unicode-Zeichen folgen zu konvertieren. Obwohl ihre Namen auf "Multibytezeichen" verweisen, funktionieren diese Funktionen mit [einem Einzel Byte-Zeichensatz](single-byte-character-sets.md) (SBCS), einem [Doppelbyte-Zeichensatz](double-byte-character-sets.md) (DBCS) und MBCS-Codepages (Multibytezeichen-Zeichensatz) gleichermaßen gut.

In der Regel sollte eine Windows-Anwendung UTF-16 intern verwenden und nur als Teil einer "dünnen Schicht" über die Schnittstelle, die ein anderes Format verwenden muss, umrechnen. Diese Technik schützt vor Verlust und Beschädigung von Daten. Jede Codepage unterstützt unterschiedliche Zeichen, aber keine von Ihnen unterstützt das vollständige Zeichen Spektrum, das von Unicode bereitgestellt wird. Die meisten Codepages unterstützen unterschiedliche Teilmengen unterschiedlich codiert. Die Codepages für UTF-8 und UTF-7 stellen eine Ausnahme dar, da Sie den gesamten Unicode-Zeichensatz unterstützen und die Konvertierung zwischen diesen Codierungen und UTF-16 verlustfrei ist.

Daten, die direkt aus der von einer Codepage verwendeten Codierung in die von einer anderen verwendete Codierung konvertiert werden, unterliegen Beschädigungen, da der gleiche Datenwert auf unterschiedlichen Codepages ein anderes Zeichen codieren kann. Auch wenn Ihre Anwendung so nah wie möglich an der-Schnittstelle ist, sollten Sie sorgfältig über den zu behandelnden Datenbereich nachzudenken.

Daten, die aus Unicode in eine Codepage konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes in den einzelnen Unicode-Daten verwendete Zeichen darstellen kann. Beachten Sie daher, dass [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) möglicherweise einige Daten verliert, wenn die Ziel Codepage nicht alle Zeichen in der Unicode-Zeichenfolge darstellen kann.

Wenn Sie auf Code Page basierende Legacy Anwendungen für die Verwendung von Unicode modernisieren, können Sie generische Funktionen und das [**Text**](/windows/win32/api/Winnt/nf-winnt-text) Makro verwenden, um einen einzelnen Satz von Quellen zu verwalten, von denen zwei Versionen der Anwendung kompiliert werden sollen. Eine Version unterstützt Unicode, und die andere Version funktioniert mit Windows-Codepages. Mit diesem Mechanismus können Sie auch sehr große Anwendungen von Windows-Codepages in Unicode konvertieren, während Sie dabei Anwendungs Quellen verwalten, die in allen Phasen der Konvertierung kompiliert, erstellt und getestet werden können. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).

Unicode-Zeichen und-Zeichen folgen verwenden Datentypen, die sich von den für Code Page basierende Zeichen und Zeichen folgen unterscheiden. Zusammen mit einer Reihe von Makros und Benennungs Konventionen minimiert diese Unterscheidung die Wahrscheinlichkeit, dass die beiden Typen von Zeichendaten versehentlich gemischt werden. Es vereinfacht die Compilertypüberprüfung, um sicherzustellen, dass nur Unicode-Parameterwerte für Funktionen verwendet werden, die Unicode-Zeichen folgen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Sortierung](sorting.md)
</dt> <dt>

[Surrogate und ergänzende Zeichen](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Verwenden der Unicode-Normalisierung zur Darstellung von Zeichen folgen](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



