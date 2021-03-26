---
description: In diesem Abschnitt werden die Funktionen der Zeichen folgen Behandlung in Windows Shell beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Verarbeitungsfunktionen für shellzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960584"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="fda89-104">Verarbeitungsfunktionen für shellzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="fda89-104">Shell String Handling Functions</span></span>

<span data-ttu-id="fda89-105">In diesem Abschnitt werden die Funktionen der Zeichen folgen Behandlung in Windows Shell beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fda89-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="fda89-106">Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.</span><span class="sxs-lookup"><span data-stu-id="fda89-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fda89-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fda89-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fda89-108">Thema</span><span class="sxs-lookup"><span data-stu-id="fda89-108">Topic</span></span></th>
<th><span data-ttu-id="fda89-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fda89-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fda89-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>Chrcmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-111">Führt einen Vergleich zwischen zwei Zeichen aus.</span><span class="sxs-lookup"><span data-stu-id="fda89-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="fda89-112">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>Getakzeptlanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-114">Ruft beim Angeben von Spracheinstellungen eine Zeichenfolge ab, die mit Websites verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fda89-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>Intlstreqn</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-116">Führt einen Vergleich der angegebenen Anzahl von Zeichen ab dem Anfang von zwei lokalisierten Zeichen folgen unter Beachtung der Groß-und Kleinschreibung durch.</span><span class="sxs-lookup"><span data-stu-id="fda89-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>Intlstreqni</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-118">Führt einen Vergleich der angegebenen Anzahl von Zeichen vom Anfang zweier lokalisierter Zeichen folgen ohne Beachtung der Groß-/Kleinschreibung aus.</span><span class="sxs-lookup"><span data-stu-id="fda89-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>Intlstreqworker</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-120">Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier lokalisierter Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fda89-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>Ischarspace</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-122">Bestimmt, ob ein Zeichen ein Leerzeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="fda89-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>Shloadderetstring</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-124">Extrahiert eine angegebene Text Ressource, wenn diese Ressource in Form einer indirekten Zeichenfolge angegeben wird (eine Zeichenfolge, die mit dem Symbol "@" beginnt).</span><span class="sxs-lookup"><span data-stu-id="fda89-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>Shstraudup</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-126">Erstellt eine Kopie einer Zeichenfolge in neu zugewiesener Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fda89-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-128">Fügt eine Zeichenfolge an eine andere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fda89-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-129">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fda89-129">Do not use.</span></span> <span data-ttu-id="fda89-130">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>Strauch</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-132">Kopiert Zeichen aus einer Zeichenfolge und fügt Sie an das Ende einer anderen Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fda89-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-133">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fda89-133">Do not use.</span></span> <span data-ttu-id="fda89-134">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>"Erw"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-136">Verkettet zwei Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fda89-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="fda89-137">Wird verwendet, wenn wiederholte Verkettungen desselben Puffers erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-139">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das mit dem angegebenen Zeichen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fda89-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="fda89-140">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>Strauch</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-142">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines Zeichens, das mit dem angegebenen Zeichen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fda89-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="fda89-143">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-145">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fda89-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="fda89-146">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>"Strauchrnw"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-148">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fda89-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="fda89-149">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-151">Vergleicht zwei Zeichen folgen, um zu bestimmen, ob Sie identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="fda89-152">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-154">Vergleicht Zeichen folgen mithilfe von C-Lauf Zeit Sortierregeln (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fda89-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fda89-155">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-157">Vergleicht zwei Zeichen folgen, um zu bestimmen, ob Sie identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="fda89-158">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>"Straucmpic"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-160">Vergleicht zwei Zeichen folgen mithilfe von C-Lauf Zeit Sortierregeln (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fda89-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fda89-161">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>"Straucmplogicalw"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-163">Vergleicht zwei Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fda89-163">Compares two Unicode strings.</span></span> <span data-ttu-id="fda89-164">Ziffern in den Zeichen folgen werden als numerischer Inhalt anstelle von Text betrachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="fda89-165">Bei diesem Test wird keine Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>"Straun"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-167">Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob diese identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="fda89-168">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="fda89-169">Das " <strong>strinncmp</strong> "-Makro unterscheidet sich nur in "Name".</span><span class="sxs-lookup"><span data-stu-id="fda89-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>"Strauch"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-171">Vergleicht eine angegebene Anzahl von Zeichen ab dem Anfang von zwei Zeichen folgen mithilfe von C-Lauf Zeit Regeln (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fda89-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fda89-172">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>"Straucmpni"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-174">Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob diese identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="fda89-175">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="fda89-176">Das " <strong>strauncmpi</strong> "-Makro unterscheidet sich nur in "Name".</span><span class="sxs-lookup"><span data-stu-id="fda89-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>"Straucmpnic"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-178">Vergleicht eine angegebene Anzahl von Zeichen ab dem Anfang von zwei Zeichen folgen mithilfe von C-Lauf Zeit Regeln (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fda89-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fda89-179">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-181">Kopiert eine Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="fda89-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-182">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fda89-182">Do not use.</span></span> <span data-ttu-id="fda89-183">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>"Straucpyn"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-185">Kopiert eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="fda89-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-186">Verwenden Sie diese Funktion oder das " <strong>strinncpy</strong> "-Makro nicht.</span><span class="sxs-lookup"><span data-stu-id="fda89-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="fda89-187">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-189">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer beliebigen Gruppe von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fda89-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="fda89-190">Bei der Suchmethode wird die Groß-/Kleinschreibung beachtet, und das abschließende <strong>null</strong> -Zeichen ist innerhalb der Suchmuster Übereinstimmung enthalten.</span><span class="sxs-lookup"><span data-stu-id="fda89-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>"Straucspni"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-192">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen einer beliebigen Gruppe von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fda89-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="fda89-193">Bei der Suchmethode wird die Groß-/Kleinschreibung nicht beachtet, und das abschließende <strong>null</strong> -Zeichen ist innerhalb der Suchmuster Übereinstimmung enthalten.</span><span class="sxs-lookup"><span data-stu-id="fda89-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-195">Dupliziert eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-197">Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="fda89-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-199">Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="fda89-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fda89-200">Unterscheidet sich von " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>stuformatbytesizew</strong></a> " in einem Parametertyp.</span><span class="sxs-lookup"><span data-stu-id="fda89-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-202">Konvertiert einen numerischen Wert abhängig von der Größe in eine Zeichenfolge, die die Zahl in Byte, Kilobyte, Megabyte oder Gigabyte darstellt.</span><span class="sxs-lookup"><span data-stu-id="fda89-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fda89-203">Erweitert <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>strformatbytesizew</strong></a> durch die Option zum Runden auf die nächste angezeigte Ziffer oder zum verwerfen nicht angezeigter Ziffern.</span><span class="sxs-lookup"><span data-stu-id="fda89-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>"Strintesizew"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-205">Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die je nach Größe in Byte, Kilobyte, Megabyte oder Gigabyte als Größen Wert ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="fda89-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fda89-206">Unterscheidet sich von " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>stuformatbytesizea</strong></a> " in einem Parametertyp.</span><span class="sxs-lookup"><span data-stu-id="fda89-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>"Straubgröße"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-208">Konvertiert einen numerischen Wert in eine Zeichenfolge, die die Zahl darstellt, die in Kilobyte als Größen Wert ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="fda89-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>"Strauch"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-210">Konvertiert ein Zeitintervall, das in Millisekunden angegeben ist, in eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>Strisintlequal</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-212">Vergleicht eine angegebene Anzahl von Zeichen vom Anfang zweier Zeichen folgen, um zu bestimmen, ob Sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-214">Fügt eine angegebene Anzahl von Zeichen vom Anfang einer Zeichenfolge an das Ende einer anderen Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fda89-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-215">Verwenden Sie diese Funktion oder das- <strong>Makro nicht</strong> .</span><span class="sxs-lookup"><span data-stu-id="fda89-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="fda89-216">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-218">Durchsucht eine Zeichenfolge nach dem ersten Vorkommen eines in einem angegebenen Puffer enthaltenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fda89-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="fda89-219">Diese Suche umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fda89-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-221">Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fda89-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="fda89-222">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>"Strinrchri"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-224">Durchsucht eine Zeichenfolge nach dem letzten Vorkommen eines angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fda89-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="fda89-225">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>"Straurbstr"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-227">Akzeptiert eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>-Struktur, die eine Zeichen</strong></a> Folge enthält, oder verweist auf eine Zeichenfolge und gibt diese Zeichenfolge als <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="fda89-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>"Stringebuf"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-229">Konvertiert eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strauch</strong></a> Struktur in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="fda89-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>"Strauch"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-231">Nimmt eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> zurückgegebene " <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>strinret</strong></a> "-Struktur an und gibt einen Zeiger auf eine zugeordnete Zeichenfolge zurück, die den anzeigen Amen enthält.</span><span class="sxs-lookup"><span data-stu-id="fda89-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-232"><a href="strrettostrn.md"><strong>"Strauch"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-233">Nimmt eine von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>zurückgegebene " <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>strinret</strong></a> "-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="fda89-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>"Straurstri"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-235">Sucht nach dem letzten Vorkommen einer angegebenen Teil Zeichenfolge innerhalb einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="fda89-236">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-238">Ruft die Länge einer Teil Zeichenfolge innerhalb einer Zeichenfolge ab, die vollständig aus Zeichen besteht, die in einem angegebenen Puffer enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fda89-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-240">Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="fda89-241">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="fda89-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-243">Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="fda89-244">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fda89-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>"Stringeint"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-246">Konvertiert eine Zeichenfolge, die einen Dezimalwert darstellt, in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fda89-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="fda89-247">Das " <strong>strautolong</strong> "-Makro ist mit dieser Funktion identisch.</span><span class="sxs-lookup"><span data-stu-id="fda89-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-249">Konvertiert eine Zeichenfolge, die einen Dezimal-oder Hexadezimalwert darstellt, in eine ganze Zahl mit 64 Bit.</span><span class="sxs-lookup"><span data-stu-id="fda89-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-251">Konvertiert eine Zeichenfolge, die eine Dezimal-oder hexadezimal Zahl darstellt, in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fda89-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>"Straume"</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-253">Entfernt die angegebenen führenden und nachfolgenden Zeichen aus einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fda89-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fda89-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-255">Nimmt eine Argumentliste variabler Länge an und gibt die Werte der Argumente als Format Zeichenfolge im <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="fda89-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-256">Verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="fda89-256">Do not use this function.</span></span> <span data-ttu-id="fda89-257">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fda89-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="fda89-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fda89-259">Nimmt eine Liste von Argumenten an und gibt die Werte der Argumente als eine im <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>formatierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="fda89-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fda89-260">Verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="fda89-260">Do not use this function.</span></span> <span data-ttu-id="fda89-261">Weitere Informationen finden Sie unter Hinweise zu alternativen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fda89-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
