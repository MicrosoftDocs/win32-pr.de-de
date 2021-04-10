---
description: Für eine Anwendung, die unformatierten Text behandelt, stellt uniscridie scriptstring- \* Funktionen bereit.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Verwenden der scriptstring-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039800"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="c1265-103">Verwenden der scriptstring-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c1265-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="c1265-104">Für eine Anwendung, die unformatierten Text behandelt, stellt uniscridie **scriptstring \*** -Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c1265-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="c1265-105">Diese Funktionen ähneln " [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)", "DrawText" und " [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent)", bieten jedoch eine vollständige komplexe Skriptunterstützung, einschließlich der Platzierung von [**Caretzeichen**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="c1265-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="c1265-106">Diese Funktionen ähneln den anderen uniscriefunktionen, sind aber auf die einfacheren Anforderungen der nur-Text-Verarbeitung zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="c1265-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="c1265-107">In der folgenden Tabelle werden die **scriptstring \*** -Funktionen und alle Entsprechungen in den anderen uniscriefunktionen ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1265-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c1265-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="c1265-108">Function</span></span></th>
<th><span data-ttu-id="c1265-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1265-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1265-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>Scriptstringanalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="c1265-111">Analysiert nur-Text.</span><span class="sxs-lookup"><span data-stu-id="c1265-111">Analyzes plain text.</span></span> <span data-ttu-id="c1265-112">Diese Funktion entspricht den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c1265-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="c1265-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>Scriptitemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="c1265-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>Scriptshape</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="c1265-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>Scriptplace</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="c1265-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>Scriptbreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="c1265-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>Scriptgetcmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="c1265-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>Scriptrecht</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="c1265-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>Scriptlayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1265-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>Scriptstringcptox</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="c1265-121">Ruft die x-Koordinate für eine Zeichenposition ab.</span><span class="sxs-lookup"><span data-stu-id="c1265-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="c1265-122">Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>scriptcptox</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c1265-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1265-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>Scriptstringfree</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="c1265-124">Gibt eine <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="c1265-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1265-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>Scriptstringgetlogicalbreiten</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="c1265-126">Konvertiert visuelle breiten in logische breiten.</span><span class="sxs-lookup"><span data-stu-id="c1265-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="c1265-127">Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>scriptgetlogicalbreiten</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c1265-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1265-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>Scriptstringgetor</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="c1265-129">Ordnet Zeichen Symbol Positionen auf ähnliche Weise wie <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">getcharakteriplacement</a>zu, nur für ältere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c1265-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="c1265-130">Diese Funktion funktioniert nicht gut mit Skripts, die mehrere Symbole pro Codepunkt generieren.</span><span class="sxs-lookup"><span data-stu-id="c1265-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1265-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>Scriptstringout</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="c1265-132">Zeigt nur-Text an.</span><span class="sxs-lookup"><span data-stu-id="c1265-132">Displays plain text.</span></span> <span data-ttu-id="c1265-133">Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>scripttextout</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c1265-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1265-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="c1265-135">Gibt einen Zeiger auf die Länge einer abgeschnittenen nur-Text-Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c1265-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1265-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="c1265-137">Gibt einen Zeiger auf den logischen Attribut Puffer für eine analysierte nur-Text-Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c1265-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1265-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="c1265-139">Gibt einen Zeiger auf die Größe (Breite und Höhe) für eine analysierte nur-Text-Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c1265-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1265-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>Scriptstringvalidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="c1265-141">Identifiziert Code Punkt Sequenzen, die im angegebenen Skript nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c1265-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="c1265-142">Diese Funktion unterscheidet sich von <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>scriptgetcmap</strong></a>, wodurch Code Punkte identifiziert werden, die nicht in einer Schriftart vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c1265-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1265-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>Scriptstringxtcp</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1265-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="c1265-144">Konvertiert eine x-Koordinate in eine Zeichenposition.</span><span class="sxs-lookup"><span data-stu-id="c1265-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="c1265-145">Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>scriptxtcp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c1265-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1265-146">Um nur nur-Text ohne Änderungen anzuzeigen, sollte eine Anwendung [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**scriptstringout**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)und dann [**scriptstringfree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1265-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="c1265-147">Die anderen Funktionen werden verwendet, um den nur-Text vor der Anzeige zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c1265-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1265-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1265-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1265-149">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="c1265-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
