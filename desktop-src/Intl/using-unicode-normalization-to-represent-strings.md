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
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="1a4bd-103">Verwenden der Unicode-Normalisierung zur Darstellung von Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="1a4bd-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="1a4bd-104">Anwendungen können mit Unicode Zeichen folgen in mehreren Formularen darstellen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="1a4bd-105">Wenn die Unicode-Akzeptanz, insbesondere über das Internet, zugenommen hat, ist die Notwendigkeit entstanden, nicht wesentliche Unterschiede in Unicode-Zeichen folgen auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="1a4bd-106">Mehrere Darstellungen für eine Kombination von Zeichen erschweren Software, z. b. Wenn ein Webserver auf eine Seiten Anforderung antwortet oder ein linker einen bestimmten Bezeichner in einer Bibliothek sucht.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="1a4bd-107">Unterschiedliche Unicode-Zeichen folgen können visuell identisch sein und Sicherheitsbedenken aufwerfen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="1a4bd-108">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="1a4bd-109">Als Antwort auf diese Anforderung hat das Unicode-Konsortium einen Prozess namens "Normalisierung" definiert, der eine binäre Darstellung für jede der äquivalenten binären Darstellungen eines Zeichens erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="1a4bd-110">Nach der Normalisierung sind zwei Zeichen folgen nur dann äquivalent, wenn Sie identische binäre Darstellungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="1a4bd-111">Bei der Normalisierung werden einige Unterschiede beseitigt</span><span class="sxs-lookup"><span data-stu-id="1a4bd-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="1a4bd-112">Um die Unicode-Normalisierung zu verwenden, kann eine Anwendung die [**normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) -und [**isnormalizedstring**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) -Funktionen für die Neuanordnung von Zeichen folgen aufrufen, die auf Unicode 4,0 TR \# 15 zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="1a4bd-113">Die Normalisierung kann zur Verbesserung der Sicherheit beitragen, indem alternative Zeichen folgen Darstellungen reduziert werden, die dieselbe sprachliche Bedeutung haben.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="1a4bd-114">Beachten Sie jedoch, dass bei der Normalisierung keine alternativen Darstellungen vollständig ausgeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="1a4bd-115">Eine ausführliche Beschreibung der Unicode-Standards für die Normalisierung finden Sie unter [Unicode-Standard Anhang \# 15: Unicode-normalisierungs Formulare](https://www.unicode.org/reports/tr15) (uax \# 15).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="1a4bd-116">Da bei der Normalisierung die Form einer Zeichenfolge geändert werden kann, sollten Sicherheitsmechanismen oder Zeichen Validierungs Algorithmen in der Regel nach der Normalisierung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="1a4bd-117">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="1a4bd-118">Mehrere Darstellungen derselben Zeichenfolge bereitstellen</span><span class="sxs-lookup"><span data-stu-id="1a4bd-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="1a4bd-119">In vielen Fällen lässt Unicode mehrere Darstellungen von linguistisch und derselben Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="1a4bd-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1a4bd-120">For example:</span></span>

-   <span data-ttu-id="1a4bd-121">Großbuchstabe a mit "Dieresis" (Umkehr) kann entweder als einzelner Unicode-Codepunkt "Ä" (u + 00c4) oder als Kombination aus Großbuchstaben a und dem kombinierten Dieresis-Zeichen ("A" + "", d. h. u + 0041 U + 0308) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="1a4bd-122">Ähnliche Überlegungen gelten für viele andere Zeichen mit diakritischen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="1a4bd-123">Das Kapital a selbst kann entweder auf die übliche Weise (lateinische Großbuchstabe a, u + 0041) oder durch den lateinischen Großbuchstaben a (u + FF21) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="1a4bd-124">Ähnliche Überlegungen gelten für die anderen einfachen lateinischen Buchstaben (sowohl groß-als auch Kleinbuchstaben) und für die Katakana-Zeichen, die beim Schreiben von Japanisch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="1a4bd-125">Die Zeichenfolge "Fi" kann entweder durch die Zeichen "f" und "i" (u + 0066 U + 0069) oder durch die Ligaturen "Fi" (u + FB01) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="1a4bd-126">Ähnliche Überlegungen gelten für viele andere Zeichenkombinationen, bei denen Unicode Ligaturen definiert.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="1a4bd-127">Verwenden der vier definierten normalisierungs Formulare</span><span class="sxs-lookup"><span data-stu-id="1a4bd-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="1a4bd-128">Ihre Anwendungen können die Unicode-Normalisierung mithilfe verschiedener Algorithmen ("normalisierungs Formulare") ausführen, die unterschiedliche Regeln einhalten.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="1a4bd-129">Das Unicode-Konsortium hat vier normalisierungs Formulare definiert: NFC (Form C), NFD (Form D), nbkc (Formular KC) und NF KD (Formular KD).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="1a4bd-130">Jedes Formular entfernt einige Unterschiede, behält jedoch den Fall bei</span><span class="sxs-lookup"><span data-stu-id="1a4bd-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="1a4bd-131">Win32 und der .NET Framework unterstützen alle vier Normalisierungsformen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="1a4bd-132">Der NLS-Enumerationstyp " [**Norm \_**](/windows/desktop/api/Winnls/ne-winnls-norm_form) " unterstützt die vier standardmäßigen Unicode-Normalisierungsformen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="1a4bd-133">Die Formulare C und D stellen kanonische Formen für Zeichen folgen bereit.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="1a4bd-134">Nicht kanonische Formulare (KC und KD) bieten weitere Kompatibilität und können bestimmte semantische Äquivalente in den Formularen C und D offenlegen. Dies geschieht jedoch auf Kosten eines bestimmten Informations Verlusts und sollte in der Regel nicht als kanonische Methode zum Speichern von Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="1a4bd-135">In den beiden kanonischen Formularen ist Form C eine "zusammengesetzte" Form, und die Form "D" ist eine "aufgesetzte" Form.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="1a4bd-136">Beispielsweise verwendet das Formular C den einzelnen Unicode-Codepunkt "Ä" (u + 00c4), während die Form "D" ("A" + "", D. h. u + 0041 u + 0308) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="1a4bd-137">Diese werden identisch dargestellt, da "" "" "" "" "" "" "" "" "", ""</span><span class="sxs-lookup"><span data-stu-id="1a4bd-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="1a4bd-138">Das Formular D kann eine beliebige Anzahl von Code Punkten zur Darstellung eines einzelnen Codepunkts verwenden, der von der Form C verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="1a4bd-139">Wenn zwei Zeichen folgen in Form C oder Form D identisch sind, sind Sie in der anderen Form identisch.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="1a4bd-140">Außerdem werden Sie, wenn Sie ordnungsgemäß gerendert werden, nicht voneinander und von der ursprünglichen nicht normalisierten Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="1a4bd-141">Nach der Normalisierung können Zeichen folgen nicht konsistent in ihre ursprüngliche Darstellung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="1a4bd-142">Wenn z. b. eine Zeichenfolge mit einer Mischung aus zusammengesetzten und aufgesetzten Zeichen Darstellungen in eine normalisierte Form konvertiert wird, gibt es keine Möglichkeit, Sie in die ursprüngliche gemischte Zeichenfolge zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="1a4bd-143">Wenn eine Anwendung daher die ursprüngliche Darstellung der Zeichenfolge erfordert, muss Sie diese Darstellung explizit speichern.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="1a4bd-144">Allerdings ist die zwischen den beiden kanonischen Formen nicht umkehrbar.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="1a4bd-145">Eine Zeichenfolge in der Form c kann in die Form D und dann zurück in die Form c konvertiert werden, und das Ergebnis ist mit der ursprünglichen Form c-Zeichenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="1a4bd-146">Die Formulare "KC" und "KD" ähneln den Formularen C bzw. D, aber diese "Kompatibilitäts Formulare" verfügen über zusätzliche Zuordnungen kompatibler Zeichen in der Basis Form der einzelnen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="1a4bd-147">Solche Zuordnungen können dazu führen, dass kleinere Zeichen Variationen verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="1a4bd-148">Sie kombinieren bestimmte Zeichen, die sich visuell unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="1a4bd-149">Sie kombinieren z. b. Zeichen mit voller Breite und halber Breite mit derselben Semantik Bedeutung oder anderen Formen desselben arabischen Buchstabens oder der Ligaturen "Fi" (u + FB01) und dem Zeichenpaar "Fi" (u + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="1a4bd-150">Sie kombinieren auch einige Zeichen, die manchmal eine andere semantische Bedeutung haben, z. b. eine Ziffer, die als superskript, als Index oder in einen Kreis geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="1a4bd-151">Aufgrund dieser Informationsverluste sollten die Formulare und KD in der Regel nicht als kanonische Formen von Zeichen folgen verwendet werden, Sie sind jedoch für bestimmte Anwendungen nützlich.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="1a4bd-152">Das Formular KC ist ein zusammengesetztes Formular, und die Form KD ist eine zusammengesetzte Form.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="1a4bd-153">Die Anwendung kann zwischen den Formaten KC und KD hin und her wechseln, aber es gibt keine konsistente Möglichkeit, von der Form "KC" oder "KD" zurück zur ursprünglichen Zeichenfolge zu wechseln, auch wenn die ursprüngliche Zeichenfolge in der Form "C" oder "D" vorliegt.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="1a4bd-154">Windows, Microsoft-Anwendungen und die .NET Framework generieren im allgemeinen Zeichen in Form C mithilfe normaler Eingabemethoden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="1a4bd-155">In den meisten Fällen ist die Form C die bevorzugte Form.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="1a4bd-156">Beispielsweise werden Zeichen in der Form C von der Windows-Tastatureingabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="1a4bd-157">Zeichen, die aus dem Web und anderen Plattformen importiert werden, können jedoch andere Normalisierungsformen in den Datenstrom einführen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="1a4bd-158">Die folgenden Beispiele werden von uax \# 15 gezeichnet und veranschaulichen die Unterschiede zwischen den vier normalisierungs Formularen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a4bd-159">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="1a4bd-159">Original</span></span></th>
<th><span data-ttu-id="1a4bd-160">Formular D</span><span class="sxs-lookup"><span data-stu-id="1a4bd-160">Form D</span></span></th>
<th><span data-ttu-id="1a4bd-161">Form C</span><span class="sxs-lookup"><span data-stu-id="1a4bd-161">Form C</span></span></th>
<th><span data-ttu-id="1a4bd-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a4bd-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a4bd-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="1a4bd-166">Die ffi_ligature (U + FB03) wird nicht zerlegt, da Sie über eine Kompatibilitäts Zuordnung verfügt, nicht über eine kanonische Zuordnung. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a4bd-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-168">&quot;A\u0308\ub03n&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="1a4bd-173">Die römische Ziffer IV (U + 2163) wird nicht zerlegt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a4bd-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-177">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-177">ga</span></span></td>
<td><span data-ttu-id="1a4bd-178">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-178">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-179">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="1a4bd-180">Verschiedene Kompatibilitäts Entsprechungen eines einzelnen japanischen Zeichens führen nicht zur gleichen Zeichenfolge in der Form C. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a4bd-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-181">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-181">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-182">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-182">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-183">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-187">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-188">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-189">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-190">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="1a4bd-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-191">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="1a4bd-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-192">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="1a4bd-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-193">KAKS</span><span class="sxs-lookup"><span data-stu-id="1a4bd-193">kaks</span></span></td>
<td><span data-ttu-id="1a4bd-194">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="1a4bd-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="1a4bd-195">KAKS</span><span class="sxs-lookup"><span data-stu-id="1a4bd-195">kaks</span></span></td>
<td><span data-ttu-id="1a4bd-196">Hangul-Silben werden unter Normalisierung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a4bd-197">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="1a4bd-197">Original</span></span></th>
<th><span data-ttu-id="1a4bd-198">Form KD</span><span class="sxs-lookup"><span data-stu-id="1a4bd-198">Form KD</span></span></th>
<th><span data-ttu-id="1a4bd-199">Formular-KC</span><span class="sxs-lookup"><span data-stu-id="1a4bd-199">Form KC</span></span></th>
<th><span data-ttu-id="1a4bd-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a4bd-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a4bd-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="1a4bd-204">Die ffi_ligature (U + FB03) wird in der Form "KC", aber nicht in der Form "C. $ {Remove} $" zerlegt.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="1a4bd-211">Die resultierenden Zeichen folgen sind in der Form "KC. $ {Remove} $" identisch.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="1a4bd-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="1a4bd-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-215">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-215">ga</span></span></td>
<td><span data-ttu-id="1a4bd-216">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-216">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-217">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="1a4bd-218">Verschiedene Kompatibilitäts Entsprechungen eines einzelnen japanischen Zeichens führen zu derselben Zeichenfolge in der Form "KC. $ {Remove} $".</span><span class="sxs-lookup"><span data-stu-id="1a4bd-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-219">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-219">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-220">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-220">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-221">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-223">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-223">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-224">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-225">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="1a4bd-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="1a4bd-226">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-226">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-227">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a4bd-228">hw_ka + 10</span><span class="sxs-lookup"><span data-stu-id="1a4bd-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-229">Ka + zehn</span><span class="sxs-lookup"><span data-stu-id="1a4bd-229">ka +ten</span></span></td>
<td><span data-ttu-id="1a4bd-230">ga</span><span class="sxs-lookup"><span data-stu-id="1a4bd-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1a4bd-231">KAKS</span><span class="sxs-lookup"><span data-stu-id="1a4bd-231">kaks</span></span></td>
<td><span data-ttu-id="1a4bd-232">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="1a4bd-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="1a4bd-233">KAKS</span><span class="sxs-lookup"><span data-stu-id="1a4bd-233">kaks</span></span></td>
<td><span data-ttu-id="1a4bd-234">Hangul-Silben werden unter Normalisierung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="1a4bd-235">In früheren Unicode-Versionen verfügten Jamo-Zeichen wie KS <sub>f</sub> über Kompatibilitäts Zuordnungen zu k <sub>f</sub> + s <sub>f</sub>.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="1a4bd-236">Diese Zuordnungen wurden in Unicode-2.1.9 entfernt, um sicherzustellen, dass Hangul-Silben beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="1a4bd-237">Die beiden obigen Tabellen haben das Copyright von © 1998-2006 Unicode, Inc. Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="1a4bd-238">Verwenden von zusammengesetzten Formularen für einzelne Symbole</span><span class="sxs-lookup"><span data-stu-id="1a4bd-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="1a4bd-239">Viele Zeichensequenzen, die einem einzelnen Symbol entsprechen, haben keine zusammengesetzten Formulare.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="1a4bd-240">Selbst bei der Normalisierung durch die Form C kann ein einzelnes visuelles Symbol oder logisches Textelement aus mehreren Unicode-Code Punkten bestehen.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="1a4bd-241">Beispielsweise haben mehrere Zeichen, die beim Schreiben von Litauisch verwendet werden, eine doppelte Diakritik, da Sie nur zusammengesetzte Formulare enthalten.</span><span class="sxs-lookup"><span data-stu-id="1a4bd-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="1a4bd-242">Ein Beispiel hierfür ist "Kleinbuchstabe u" mit "Macron" und "Tilde" ("...", u + 016b u + 0303, wobei der erste Codepunkt ein Kleinbuchstabe "u" mit "Macron" und der zweite ein kombinierter geschrider Buchstabe ist)</span><span class="sxs-lookup"><span data-stu-id="1a4bd-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="1a4bd-243">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1a4bd-243">Example</span></span>

<span data-ttu-id="1a4bd-244">Ein relevantes Beispiel finden Sie im Beispiel [nls: Unicode-Normalisierung](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1a4bd-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a4bd-245">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a4bd-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a4bd-246">Verwenden der Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="1a4bd-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="1a4bd-247">Überlegungen zur Sicherheit: Internationale Features</span><span class="sxs-lookup"><span data-stu-id="1a4bd-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="1a4bd-248">**Isnormalizedstring**</span><span class="sxs-lookup"><span data-stu-id="1a4bd-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="1a4bd-249">**Normalizestring**</span><span class="sxs-lookup"><span data-stu-id="1a4bd-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




