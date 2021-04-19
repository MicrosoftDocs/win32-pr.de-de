---
title: Rich-Edit-Funktionen
description: Rich-Edit-Funktionen
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373456"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="64316-103">Rich-Edit-Funktionen</span><span class="sxs-lookup"><span data-stu-id="64316-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64316-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="64316-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64316-105">Thema</span><span class="sxs-lookup"><span data-stu-id="64316-105">Topic</span></span></th>
<th><span data-ttu-id="64316-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64316-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64316-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>Autocorrectproc</em></a></span><span class="sxs-lookup"><span data-stu-id="64316-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="64316-108">Die <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>autocorrectproc</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64316-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64316-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>Editstreamcallback</em></a></span><span class="sxs-lookup"><span data-stu-id="64316-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="64316-110">Die <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>editstreamcallback</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit den <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> -und <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> -Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64316-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="64316-111">Es wird verwendet, um einen Datenstrom in ein oder aus einem Rich-Edit-Steuerelement zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="64316-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="64316-112">Der <strong>editstreamcallback</strong> -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="64316-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="64316-113"><em>Editstreamcallback</em> ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="64316-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64316-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>Editwordbreakprocex</em></a></span><span class="sxs-lookup"><span data-stu-id="64316-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="64316-115">Die <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>editwordbreakprocex</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64316-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="64316-116">Er bestimmt den Zeichen Index der Wort Umbruch-oder Zeichenklassen-und Wort Umbruch Kennzeichen der Zeichen im angegebenen Text.</span><span class="sxs-lookup"><span data-stu-id="64316-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="64316-117">Der <strong>editwordbreakprocex</strong> -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="64316-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="64316-118"><em>Editwordbreakprocex</em> ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="64316-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64316-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>Getmathalpha numerisch</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-120">Ruft das alphanumerische Unicode-Transformations Format (UTF)-32-alphanumerische Zeichen ab, das dem angegebenen grundlegenden Zeichen für die mehrsprachige Ebene (BMP) und dem mathematischen Stil entspricht.</span><span class="sxs-lookup"><span data-stu-id="64316-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64316-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>Getmathalpha annumerischer Code</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-122">Ruft den mathematischen Stil und den Zeichencode der "Upright Basic-mehrsprachige Ebene (BMP)" ab, der dem angegebenen nachfolgenden Byte eines mathematischen Ersatz Zeichen Paars entspricht.</span><span class="sxs-lookup"><span data-stu-id="64316-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64316-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>Hyphenateproc</em></a></span><span class="sxs-lookup"><span data-stu-id="64316-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="64316-124">Die <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>hyphenateproc</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64316-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="64316-125">Es bestimmt, wie die Bindestriche in einem Rich-Edit-Steuerelement von Microsoft ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64316-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64316-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>Mathbuilddown</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-127">Übersetzt die integrierten mathematischen, Ruby-und anderen Inline Objekte im angegebenen Bereich in eine lineare Form.</span><span class="sxs-lookup"><span data-stu-id="64316-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64316-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>Mathbuildup</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-129">Konvertiert die mathematische lineare Formatierung in einem Bereich in ein integriertes Formular oder ändert das aktuelle integrierte Formular.</span><span class="sxs-lookup"><span data-stu-id="64316-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64316-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>Mathtranslation</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-131">Übersetzt die mathematischen Zeichen im angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="64316-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64316-132"><a href="reextendedregisterclass.md"><strong>Reextendedregisterclass</strong></a></span><span class="sxs-lookup"><span data-stu-id="64316-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="64316-133">Registriert die beiden Klassennamen REListBox20W und RECombobox20W, die verwendet werden können, um ein umfangreiches Bearbeitungs Listenfeld oder ComboBox-Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64316-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="64316-134">Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="64316-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="64316-135">Diese Funktion wird in zukünftigen Versionen möglicherweise nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64316-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

