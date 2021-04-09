---
description: Anwendungen können mit Unicode Zeichen folgen in mehreren Formularen darstellen.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Verwenden der Unicode-Normalisierung zur Darstellung von Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869072"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Verwenden der Unicode-Normalisierung zur Darstellung von Zeichen folgen

Anwendungen können mit Unicode Zeichen folgen in mehreren Formularen darstellen. Wenn die Unicode-Akzeptanz, insbesondere über das Internet, zugenommen hat, ist die Notwendigkeit entstanden, nicht wesentliche Unterschiede in Unicode-Zeichen folgen auszuschließen. Mehrere Darstellungen für eine Kombination von Zeichen erschweren Software, z. b. Wenn ein Webserver auf eine Seiten Anforderung antwortet oder ein linker einen bestimmten Bezeichner in einer Bibliothek sucht.

> [!Caution]  
> Unterschiedliche Unicode-Zeichen folgen können visuell identisch sein und Sicherheitsbedenken aufwerfen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

Als Antwort auf diese Anforderung hat das Unicode-Konsortium einen Prozess namens "Normalisierung" definiert, der eine binäre Darstellung für jede der äquivalenten binären Darstellungen eines Zeichens erzeugt. Nach der Normalisierung sind zwei Zeichen folgen nur dann äquivalent, wenn Sie identische binäre Darstellungen aufweisen. Bei der Normalisierung werden einige Unterschiede beseitigt

Um die Unicode-Normalisierung zu verwenden, kann eine Anwendung die [**normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) -und [**isnormalizedstring**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) -Funktionen für die Neuanordnung von Zeichen folgen aufrufen, die auf Unicode 4,0 TR \# 15 zugreifen. Die Normalisierung kann zur Verbesserung der Sicherheit beitragen, indem alternative Zeichen folgen Darstellungen reduziert werden, die dieselbe sprachliche Bedeutung haben. Beachten Sie jedoch, dass bei der Normalisierung keine alternativen Darstellungen vollständig ausgeschlossen werden können.

Eine ausführliche Beschreibung der Unicode-Standards für die Normalisierung finden Sie unter [Unicode-Standard Anhang \# 15: Unicode-normalisierungs Formulare](https://www.unicode.org/reports/tr15) (uax \# 15).

> [!Caution]  
> Da bei der Normalisierung die Form einer Zeichenfolge geändert werden kann, sollten Sicherheitsmechanismen oder Zeichen Validierungs Algorithmen in der Regel nach der Normalisierung implementiert werden. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Mehrere Darstellungen derselben Zeichenfolge bereitstellen

In vielen Fällen lässt Unicode mehrere Darstellungen von linguistisch und derselben Zeichenfolge zu. Beispiel:

-   Großbuchstabe a mit "Dieresis" (Umkehr) kann entweder als einzelner Unicode-Codepunkt "Ä" (u + 00c4) oder als Kombination aus Großbuchstaben a und dem kombinierten Dieresis-Zeichen ("A" + "", d. h. u + 0041 U + 0308) dargestellt werden. Ähnliche Überlegungen gelten für viele andere Zeichen mit diakritischen Zeichen.
-   Das Kapital a selbst kann entweder auf die übliche Weise (lateinische Großbuchstabe a, u + 0041) oder durch den lateinischen Großbuchstaben a (u + FF21) dargestellt werden. Ähnliche Überlegungen gelten für die anderen einfachen lateinischen Buchstaben (sowohl groß-als auch Kleinbuchstaben) und für die Katakana-Zeichen, die beim Schreiben von Japanisch verwendet werden.
-   Die Zeichenfolge "Fi" kann entweder durch die Zeichen "f" und "i" (u + 0066 U + 0069) oder durch die Ligaturen "Fi" (u + FB01) dargestellt werden. Ähnliche Überlegungen gelten für viele andere Zeichenkombinationen, bei denen Unicode Ligaturen definiert.

## <a name="use-the-four-defined-normalization-forms"></a>Verwenden der vier definierten normalisierungs Formulare

Ihre Anwendungen können die Unicode-Normalisierung mithilfe verschiedener Algorithmen ("normalisierungs Formulare") ausführen, die unterschiedliche Regeln einhalten. Das Unicode-Konsortium hat vier normalisierungs Formulare definiert: NFC (Form C), NFD (Form D), nbkc (Formular KC) und NF KD (Formular KD). Jedes Formular entfernt einige Unterschiede, behält jedoch den Fall bei Win32 und der .NET Framework unterstützen alle vier Normalisierungsformen.

Der NLS-Enumerationstyp " [**Norm \_**](/windows/desktop/api/Winnls/ne-winnls-norm_form) " unterstützt die vier standardmäßigen Unicode-Normalisierungsformen. Die Formulare C und D stellen kanonische Formen für Zeichen folgen bereit. Nicht kanonische Formulare (KC und KD) bieten weitere Kompatibilität und können bestimmte semantische Äquivalente in den Formularen C und D offenlegen. Dies geschieht jedoch auf Kosten eines bestimmten Informations Verlusts und sollte in der Regel nicht als kanonische Methode zum Speichern von Zeichen folgen verwendet werden.

In den beiden kanonischen Formularen ist Form C eine "zusammengesetzte" Form, und die Form "D" ist eine "aufgesetzte" Form. Beispielsweise verwendet das Formular C den einzelnen Unicode-Codepunkt "Ä" (u + 00c4), während die Form "D" ("A" + "", D. h. u + 0041 u + 0308) verwendet wird. Diese werden identisch dargestellt, da "" "" "" "" "" "" "" "" "", "" Das Formular D kann eine beliebige Anzahl von Code Punkten zur Darstellung eines einzelnen Codepunkts verwenden, der von der Form C verwendet wird.

Wenn zwei Zeichen folgen in Form C oder Form D identisch sind, sind Sie in der anderen Form identisch. Außerdem werden Sie, wenn Sie ordnungsgemäß gerendert werden, nicht voneinander und von der ursprünglichen nicht normalisierten Zeichenfolge angezeigt.

Nach der Normalisierung können Zeichen folgen nicht konsistent in ihre ursprüngliche Darstellung zurückgegeben werden. Wenn z. b. eine Zeichenfolge mit einer Mischung aus zusammengesetzten und aufgesetzten Zeichen Darstellungen in eine normalisierte Form konvertiert wird, gibt es keine Möglichkeit, Sie in die ursprüngliche gemischte Zeichenfolge zu normalisieren. Wenn eine Anwendung daher die ursprüngliche Darstellung der Zeichenfolge erfordert, muss Sie diese Darstellung explizit speichern. Allerdings ist die zwischen den beiden kanonischen Formen nicht umkehrbar. Eine Zeichenfolge in der Form c kann in die Form D und dann zurück in die Form c konvertiert werden, und das Ergebnis ist mit der ursprünglichen Form c-Zeichenfolge identisch.

Die Formulare "KC" und "KD" ähneln den Formularen C bzw. D, aber diese "Kompatibilitäts Formulare" verfügen über zusätzliche Zuordnungen kompatibler Zeichen in der Basis Form der einzelnen Zeichen. Solche Zuordnungen können dazu führen, dass kleinere Zeichen Variationen verloren gehen. Sie kombinieren bestimmte Zeichen, die sich visuell unterscheiden. Sie kombinieren z. b. Zeichen mit voller Breite und halber Breite mit derselben Semantik Bedeutung oder anderen Formen desselben arabischen Buchstabens oder der Ligaturen "Fi" (u + FB01) und dem Zeichenpaar "Fi" (u + 0066 U + 0069). Sie kombinieren auch einige Zeichen, die manchmal eine andere semantische Bedeutung haben, z. b. eine Ziffer, die als superskript, als Index oder in einen Kreis geschrieben wurde. Aufgrund dieser Informationsverluste sollten die Formulare und KD in der Regel nicht als kanonische Formen von Zeichen folgen verwendet werden, Sie sind jedoch für bestimmte Anwendungen nützlich.

Das Formular KC ist ein zusammengesetztes Formular, und die Form KD ist eine zusammengesetzte Form. Die Anwendung kann zwischen den Formaten KC und KD hin und her wechseln, aber es gibt keine konsistente Möglichkeit, von der Form "KC" oder "KD" zurück zur ursprünglichen Zeichenfolge zu wechseln, auch wenn die ursprüngliche Zeichenfolge in der Form "C" oder "D" vorliegt.

Windows, Microsoft-Anwendungen und die .NET Framework generieren im allgemeinen Zeichen in Form C mithilfe normaler Eingabemethoden. In den meisten Fällen ist die Form C die bevorzugte Form. Beispielsweise werden Zeichen in der Form C von der Windows-Tastatureingabe erzeugt. Zeichen, die aus dem Web und anderen Plattformen importiert werden, können jedoch andere Normalisierungsformen in den Datenstrom einführen.

Die folgenden Beispiele werden von uax \# 15 gezeichnet und veranschaulichen die Unterschiede zwischen den vier normalisierungs Formularen.



<table>
<thead>
<tr class="header">
<th>Ursprünglich</th>
<th>Formular D</th>
<th>Form C</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Die ffi_ligature (U + FB03) wird nicht zerlegt, da Sie über eine Kompatibilitäts Zuordnung verfügt, nicht über eine kanonische Zuordnung. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\ub03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Die römische Ziffer IV (U + 2163) wird nicht zerlegt. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + zehn</td>
<td>ga</td>
<td rowspan="5">Verschiedene Kompatibilitäts Entsprechungen eines einzelnen japanischen Zeichens führen nicht zur gleichen Zeichenfolge in der Form C. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + zehn</td>
<td>Ka + zehn</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + 10</td>
<td>hw_ka + 10</td>
<td>hw_ka + 10</td>

</tr>
<tr class="even">
<td>KAKS</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>KAKS</td>
<td>Hangul-Silben werden unter Normalisierung beibehalten.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Ursprünglich</th>
<th>Form KD</th>
<th>Formular-KC</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Die ffi_ligature (U + FB03) wird in der Form "KC", aber nicht in der Form "C. $ {Remove} $" zerlegt.<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Die resultierenden Zeichen folgen sind in der Form "KC. $ {Remove} $" identisch.<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + zehn</td>
<td>ga</td>
<td rowspan="5">Verschiedene Kompatibilitäts Entsprechungen eines einzelnen japanischen Zeichens führen zu derselben Zeichenfolge in der Form "KC. $ {Remove} $".<br />
</td>
</tr>
<tr class="even">
<td>Ka + zehn</td>
<td>Ka + zehn</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>Ka + zehn</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + zehn</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + 10</td>
<td>Ka + zehn</td>
<td>ga</td>

</tr>
<tr class="even">
<td>KAKS</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>KAKS</td>
<td>Hangul-Silben werden unter Normalisierung beibehalten. In früheren Unicode-Versionen verfügten Jamo-Zeichen wie KS <sub>f</sub> über Kompatibilitäts Zuordnungen zu k <sub>f</sub> + s <sub>f</sub>. Diese Zuordnungen wurden in Unicode-2.1.9 entfernt, um sicherzustellen, dass Hangul-Silben beibehalten werden.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Die beiden obigen Tabellen haben das Copyright von © 1998-2006 Unicode, Inc. Alle Rechte vorbehalten.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Verwenden von zusammengesetzten Formularen für einzelne Symbole

Viele Zeichensequenzen, die einem einzelnen Symbol entsprechen, haben keine zusammengesetzten Formulare. Selbst bei der Normalisierung durch die Form C kann ein einzelnes visuelles Symbol oder logisches Textelement aus mehreren Unicode-Code Punkten bestehen. Beispielsweise haben mehrere Zeichen, die beim Schreiben von Litauisch verwendet werden, eine doppelte Diakritik, da Sie nur zusammengesetzte Formulare enthalten. Ein Beispiel hierfür ist "Kleinbuchstabe u" mit "Macron" und "Tilde" ("...", u + 016b u + 0303, wobei der erste Codepunkt ein Kleinbuchstabe "u" mit "Macron" und der zweite ein kombinierter geschrider Buchstabe ist)

## <a name="example"></a>Beispiel

Ein relevantes Beispiel finden Sie im Beispiel [nls: Unicode-Normalisierung](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Überlegungen zur Sicherheit: Internationale Features](security-considerations--international-features.md)
</dt> <dt>

[**Isnormalizedstring**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**Normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




