---
description: Anwendungen können Unicode verwenden, um Zeichenfolgen in mehreren Formen zu darstellen.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c6d091548d924919a18fe05fb9d98d2b82b13792df2facfe96489be2d7ff2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822490"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Verwenden der Unicode-Normalisierung zum Darstellen von Zeichenfolgen

Anwendungen können Unicode verwenden, um Zeichenfolgen in mehreren Formen zu darstellen. Mit der immer größer werdenden Unicode-Akzeptanz , insbesondere über das Internet, ist es erforderlich geworden, nicht wesentliche Unterschiede in Unicode-Zeichenfolgen zu beseitigen. Mehrere Darstellungen für eine Kombination von Zeichen erschweren Software, z. B. wenn ein Webserver auf eine Seitenanforderung antwortet oder ein Linker einen bestimmten Bezeichner in einer Bibliothek sucht.

> [!Caution]  
> Unterschiedliche Unicode-Zeichenfolgen können visuell identisch sein, was Sicherheitsbedenken nach sich zieht. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

Als Reaktion auf diese Anforderung hat das Unicode-Konsortium einen Prozess namens "Normalisierung" definiert, der eine binäre Darstellung für eine der entsprechenden binären Darstellungen eines Zeichens erzeugt. Nach der Normalisierung sind zwei Zeichenfolgen nur dann gleichwertig, wenn sie identische binäre Darstellungen haben. Die Normalisierung beseitigt einige Unterschiede, behält jedoch die Case bei.

Um die Unicode-Normalisierung zu verwenden, kann eine Anwendung die [**Funktionen NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) und [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) für die Neuanordnung von Zeichenfolgen aufrufen, die Unicode 4.0 TR \# 15 anordnen. Die Normalisierung kann zur Verbesserung der Sicherheit beitragen, indem alternative Zeichenfolgendarstellungen reduziert werden, die dieselbe linguistische Bedeutung haben. Denken Sie jedoch daran, dass die Normalisierung alternative Darstellungen nicht vollständig beseitigen kann.

Eine ausführliche Beschreibung der Unicode-Standards für die Normalisierung finden Sie unter [Unicode Standard Anhang \# 15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \# 15).

> [!Caution]  
> Da die Normalisierung die Form einer Zeichenfolge ändern kann, sollten Sicherheitsmechanismen oder Zeichenvalidierungsalgorithmen in der Regel nach der Normalisierung implementiert werden. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Bereitstellen mehrerer Darstellungen derselben Zeichenfolge

In vielen Fällen lässt Unicode mehrere Darstellungen derselben Zeichenfolge zu. Beispiel:

-   Groß A mit Dieresis (umlaut) kann entweder als einzelner Unicode-Codepunkt "Ä" (U+00C4) oder als Kombination aus Groß A und dem kombinierenden Dieresis-Zeichen ("A" + " BZW. U+0041 U+0308) dargestellt werden. Ähnliche Überlegungen gelten für viele andere Zeichen mit diakritischen Markierungen.
-   Groß A selbst kann entweder auf die übliche Weise (lateinischer Großbuchstaben A, U+0041) oder durch den vollständigen lateinischen Großbuchstaben A (U+FF21) dargestellt werden. Ähnliche Überlegungen gelten für die anderen einfachen lateinischen Buchstaben (Groß- und Kleinbuchstaben) und für die katakana-Zeichen, die beim Schreiben von Japanisch verwendet werden.
-   Die Zeichenfolge "fi" kann entweder durch die Zeichen "f" und "i" (U+0066 U+0069) oder durch die Ligatur "fi" (U+FB01) dargestellt werden. Ähnliche Überlegungen gelten für viele andere Kombinationen von Zeichen, für die Unicode Ligaturen definiert.

## <a name="use-the-four-defined-normalization-forms"></a>Verwenden der vier definierten Normalisierungsformulare

Ihre Anwendungen können die Unicode-Normalisierung mithilfe mehrerer Algorithmen ausführen, die als "Normalisierungsformen" bezeichnet werden und unterschiedliche Regeln einhalten. Das Unicode-Konsortium hat vier Normalisierungsformen definiert: NFC (Form C), NFD (Form D), NFKC (Form KC) und NFKD (Form KD). Jedes Formular beseitigt einige Unterschiede, behält jedoch die Case bei. Win32 und die .NET Framework unterstützen alle vier Normalisierungsformen.

Der NLS-Enumerationstyp [**NORM \_ FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) unterstützt die vier standardmäßigen Unicode-Normalisierungsformen. Die Formulare C und D stellen kanonische Formulare für Zeichenfolgen zur Verfügung. Nicht kanonische Formen KC und KD bieten weitere Kompatibilität und können bestimmte semantische Äquivalenzen erkennen, die in den Formen C und D nicht offensichtlich sind. Dies erfolgt jedoch auf Kosten eines bestimmten Informationsverlusts und sollte im Allgemeinen nicht als kanonische Methode zum Speichern von Zeichenfolgen verwendet werden.

Von den beiden kanonischen Formen ist Form C eine "zusammengesetzte" Form, und Form D ist eine "zersetzte" Form. In Form C wird beispielsweise der einzelne Unicode-Codepunkt "Ä" (U+00C4) verwendet, während formular D verwendet ("A" + " 2", d. h. U+0041 U+0308). Diese werden identisch gerendert, da " GLEICH" (U+0308) ein kombinierende Zeichen ist. Formular D kann eine beliebige Anzahl von Codepunkten verwenden, um einen einzelnen Codepunkt zu darstellen, der von Formular C verwendet wird.

Wenn zwei Zeichenfolgen in Form C oder Formular D identisch sind, sind sie in der anderen Form identisch. Darüber hinaus werden sie, wenn sie ordnungsgemäß gerendert werden, ununterscheidbar voneinander und von der ursprünglichen nicht normalisierten Zeichenfolge angezeigt.

Nach der Normalisierung können Zeichenfolgen nicht konsistent an ihre ursprüngliche Darstellung zurückgegeben werden. Wenn beispielsweise eine Zeichenfolge mit einer Mischung aus zusammengesetzten und zersetzten Zeichendarstellungen in eine normalisierte Form konvertiert wird, gibt es keine Möglichkeit, sie in die ursprüngliche gemischte Zeichenfolge zu normalisieren. Wenn eine Anwendung daher die ursprüngliche Darstellung der Zeichenfolge erfordert, muss sie diese Darstellung explizit speichern. Die Konvertierung zwischen den beiden kanonischen Formen ist jedoch umkehrbar. Eine Zeichenfolge im Formular C kann in Form von D und dann zurück in Form C konvertiert werden, und das Ergebnis ist mit der ursprünglichen Form C-Zeichenfolge identisch.

Die Formulare KC und KD ähneln den Formularen C bzw. D, aber diese "Kompatibilitätsformulare" verfügen über zusätzliche Zuordnungen kompatibler Zeichen zur Basisform jedes Zeichens. Solche Zuordnungen können dazu führen, dass kleinere Zeichenvariationen verloren gehen. Sie kombinieren bestimmte Zeichen, die visuell unterschiedlich sind. Sie kombinieren z. B. Zeichen mit voller Breite und halber Breite mit der gleichen semantischen Bedeutung oder verschiedenen Formen desselben arabischen Buchstabens oder der Ligatur "fi" (U+FB01) und dem Zeichenpaar "fi" (U+0066 U+0069). Sie kombinieren auch einige Zeichen, die manchmal eine andere semantische Bedeutung haben können, z. B. eine Als Hochgestellte, als Inskript oder in einen Kreis eingeschlossene Ziffer. Aufgrund dieses Informationsverlusts sollten Formulare KC und KD im Allgemeinen nicht als kanonische Formen von Zeichenfolgen verwendet werden, aber sie sind für bestimmte Anwendungen nützlich.

Form KC ist ein zusammengesetztes Formular, und form KD ist ein zersetztes Formular. Die Anwendung kann zwischen den Formularen KC und KD hin und her wechseln, aber es gibt keine konsistente Möglichkeit, vom Formular KC oder KD zurück zur ursprünglichen Zeichenfolge zu wechseln, auch wenn die ursprüngliche Zeichenfolge in Form von C oder D vor liegt.

Windows, Microsoft-Anwendungen und die .NET Framework in der Regel Zeichen in Form von C mithilfe normaler Eingabemethoden generieren. Für die meisten Zwecke Windows Formular C das bevorzugte Formular. Beispielsweise werden Zeichen in Form C von der Tastatureingabe Windows erzeugt. Aus dem Web und anderen Plattformen importierte Zeichen können jedoch andere Normalisierungsformen in den Datenstrom einführen.

Die folgenden Beispiele werden aus UAX 15 gezeichnet und veranschaulichen die Unterschiede zwischen \# den vier Normalisierungsformen.



<table>
<thead>
<tr class="header">
<th>Ursprünglich</th>
<th>Formular D</th>
<th>Formular C</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Der ffi_ligature (U+FB03) wird nicht zersetzt, da er über eine Kompatibilitätszuordnung verfügt, nicht über eine kanonische Zuordnung.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä\uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä\uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Iv.&quot;</td>
<td>&quot;Iv.&quot;</td>
<td>&quot;Iv.&quot;</td>
<td rowspan="2">Der ROMAN NUMERAL IV (U+2163) ist nicht zersetzt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Gegen \u2163&quot;</td>
<td>&quot;Gegen \u2163&quot;</td>
<td>&quot;Gegen \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +ten</td>
<td>ga</td>
<td rowspan="5">Unterschiedliche Kompatibilitätsentsprechungen eines einzelnen japanischen Zeichens führen nicht zu derselben Zeichenfolge im Format C.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +ten</td>
<td>ka +ten</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka +10</td>
<td>hw_ka +10</td>
<td>hw_ka +10</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>Hangul-Silben werden unter Normalisierung beibehalten.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Ursprünglich</th>
<th>Formular-KD</th>
<th>Formular-KC</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Die ffi_ligature (U+FB03) wird in Form KC, jedoch nicht in Form C.${REMOVE}$ zerlegt.<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä\uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Iv. Iv.&quot;</td>
<td>&quot;Iv. Iv.&quot;</td>
<td>&quot;Iv. Iv.&quot;</td>
<td rowspan="2">Die hier resultierenden Zeichenfolgen sind im Format KC.${REMOVE}$ identisch.<br />
</td>
</tr>
<tr class="even">
<td>&quot;Verzeichnis \u2163&quot;</td>
<td>&quot;Iv. Iv.&quot;</td>
<td>&quot;Iv. Iv.&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +zehn</td>
<td>ga</td>
<td rowspan="5">Unterschiedliche Kompatibilitätsentsprechungen eines einzelnen japanischen Zeichens führen zu derselben Zeichenfolge im Format KC.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +zehn</td>
<td>ka +zehn</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>ka +zehn</td>
<td>ga</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +zehn</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +10</td>
<td>ka +zehn</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>Hangul-Silbe werden unter Normalisierung beibehalten. In früheren Unicode-Versionen hatten Jamo-Zeichen wie ks <sub>f</sub> Kompatibilitätszuordnungen zu k <sub>f</sub> + s <sub>f</sub>. Diese Zuordnungen wurden in Unicode 2.1.9 entfernt, um sicherzustellen, dass Hangul-Silbe beibehalten werden.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Die beiden obigen Tabellen haben ein Copyright von © 1998-2006 Unicode, Inc. Alle Rechte vorbehalten.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Verwenden zusammengesetzter Formulare für einzelne Glyphen

Viele Zeichensequenzen, die einem einzelnen Glyphen entsprechen, verfügen nicht über zusammengesetzte Formen. Selbst bei normalisierter Form C kann ein einzelnes visuelles Glyphenelement oder logisches Textelement aus mehreren Unicode-Codepunkten bestehen. So weisen beispielsweise mehrere Zeichen, die beim Schreiben von "Litiv" verwendet werden, doppelte diakritische Zeichen auf, da sie nur zerlegte Formulare aufweisen. Ein Beispiel hierfür ist U in Kleinbuchstaben mit Makron und Tilde ("sstelle", U+016b U+0303, wobei der erste Codepunkt ein Kleinbuchstaben-U mit Makron und der zweite ein kombinierender Akzent ist).

## <a name="example"></a>Beispiel

Ein relevantes Beispiel finden Sie unter [NLS: Unicode-Normalisierungsbeispiel.](nls--unicode-normalization-sample.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprachen](using-national-language-support.md)
</dt> <dt>

[Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




