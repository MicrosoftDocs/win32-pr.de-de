---
title: Zeichenfolgen
description: In diesem Abschnitt werden die Zeichen folgen Funktionen erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- Ressourcen, Zeichen folgen
- Zeichenfolgen
- Zeichenfolgenfunktionen (string-Funktionen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732097"
---
# <a name="strings"></a><span data-ttu-id="24f5d-106">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="24f5d-106">Strings</span></span>

<span data-ttu-id="24f5d-107">In diesem Abschnitt werden die Zeichen folgen Funktionen beschrieben und erläutert, wie Sie in Ihren Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24f5d-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="24f5d-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="24f5d-108">In This Section</span></span>



| <span data-ttu-id="24f5d-109">Name</span><span class="sxs-lookup"><span data-stu-id="24f5d-109">Name</span></span>                                     | <span data-ttu-id="24f5d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24f5d-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="24f5d-111">Informationen über Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="24f5d-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="24f5d-112">Erläutert die Zeichen folgen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="24f5d-113">Informationen zu "strausafe. h"</span><span class="sxs-lookup"><span data-stu-id="24f5d-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="24f5d-114">Erläutert die Zeichen folgen Funktionen in "strausafe. h".</span><span class="sxs-lookup"><span data-stu-id="24f5d-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="24f5d-115">Zeichen folgen Verweis</span><span class="sxs-lookup"><span data-stu-id="24f5d-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="24f5d-116">Enthält die API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="24f5d-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="24f5d-117">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="24f5d-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24f5d-118">Name</span><span class="sxs-lookup"><span data-stu-id="24f5d-118">Name</span></span></th>
<th><span data-ttu-id="24f5d-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24f5d-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24f5d-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>Charlower</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-121">Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="24f5d-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="24f5d-122">Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="24f5d-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>Charlowerbuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-124">Konvertiert Großbuchstaben in einem Puffer in Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="24f5d-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="24f5d-125">Die-Funktion konvertiert die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="24f5d-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>Charnext</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-127">Ruft einen Zeiger auf das nächste Zeichen in einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="24f5d-128">Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>Charnextexa</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-130">Ruft den Zeiger auf das nächste Zeichen in einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="24f5d-131">Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>Charprev</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-133">Ruft einen Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="24f5d-134">Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>Charprevexa</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-136">Ruft den Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="24f5d-137">Diese Funktion kann Zeichen folgen verarbeiten, die aus Einzel-oder Multibytezeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>Charper OEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-139">Übersetzt eine Zeichenfolge in den von OEM definierten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="24f5d-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>Chartoken</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-141">Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge in den von OEM definierten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="24f5d-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>Charupper</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-143">Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="24f5d-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="24f5d-144">Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="24f5d-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>Charupperbuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-146">Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="24f5d-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="24f5d-147">Die-Funktion konvertiert die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="24f5d-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-149">Vergleicht zwei Zeichen folgen unter Verwendung des angegebenen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="24f5d-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="24f5d-150">Verwenden Sie für die Kompatibilität mit Unicode <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>comparestringex</strong></a> oder die Unicode-Version von <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="24f5d-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>Comparestringex</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-152">Vergleicht zwei Unicode-Zeichen folgen (breit Zeichen) unter Verwendung des angegebenen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="24f5d-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-154">Ordnet eine Zeichenfolge einer anderen zu, wobei eine angegebene Transformations Option durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24f5d-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>Getstringtypea</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-156">Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="24f5d-157">Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="24f5d-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="24f5d-158">Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="24f5d-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>Getstringtypeex</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-160">Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="24f5d-161">Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="24f5d-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="24f5d-162">Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="24f5d-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="24f5d-163">Im Gegensatz zu seinen close-verwandten " <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>getstringtypea</strong></a> " und " <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>getstringtypew</strong></a>" zeigt <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>getstringtypeex</strong></a> das Standardverhalten durch die Verwendung des Unicode-Schalters " <strong> # define</strong> ".</span><span class="sxs-lookup"><span data-stu-id="24f5d-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="24f5d-164">Dies ist die empfohlene Funktion.</span><span class="sxs-lookup"><span data-stu-id="24f5d-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>Getstringtypew</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-166">Ruft Zeichentyp Informationen für die Zeichen in der angegebenen Quell Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="24f5d-167">Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabe Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="24f5d-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="24f5d-168">Jedes Bit identifiziert einen angegebenen Zeichentyp, z. b. ob es sich um einen Buchstaben, eine Ziffer oder keines von beiden Zeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="24f5d-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>Ischaralpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-170">Bestimmt, ob ein Zeichen ein alphabetisches Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="24f5d-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="24f5d-171">Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="24f5d-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>Ischaralpha numerisch</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-173">Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="24f5d-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="24f5d-174">Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="24f5d-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>Ischarlower</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-176">Bestimmt, ob ein Zeichen klein geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="24f5d-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="24f5d-177">Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="24f5d-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>Ischarupper</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-179">Bestimmt, ob ein Zeichen in Großbuchstaben vorliegt.</span><span class="sxs-lookup"><span data-stu-id="24f5d-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="24f5d-180">Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="24f5d-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-182">Lädt eine Zeichen folgen Ressource aus der ausführbaren Datei, die einem angegebenen Modul zugeordnet ist, kopiert die Zeichenfolge in einen Puffer und fügt ein abschließendes NULL-Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="24f5d-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrincat</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-184">Fügt eine Zeichenfolge an eine andere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="24f5d-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstraucmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-186">Vergleicht zwei Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-186">Compares two character strings.</span></span> <span data-ttu-id="24f5d-187">Beim Vergleich wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="24f5d-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstraucmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-189">Vergleicht zwei Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-189">Compares two character strings.</span></span> <span data-ttu-id="24f5d-190">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="24f5d-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrincpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-192">Kopiert eine Zeichenfolge in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="24f5d-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrincpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-194">Kopiert eine angegebene Anzahl von Zeichen aus einer Quell Zeichenfolge in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="24f5d-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-196">Bestimmt die Länge der angegebenen Zeichenfolge (ohne das abschließende Null Zeichen).</span><span class="sxs-lookup"><span data-stu-id="24f5d-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>Oemto Char</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-198">Übersetzt eine Zeichenfolge aus dem OEM-definierten Zeichensatz in eine ANSI-oder Zeichenfolge mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>Oemzu charbuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-200">Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge aus dem OEM-definierten Zeichensatz in eine ANSI-oder eine Zeichenfolge mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="24f5d-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24f5d-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-202">Schreibt formatierte Daten in den angegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="24f5d-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24f5d-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>Wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="24f5d-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="24f5d-204">Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in den angegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="24f5d-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="24f5d-205">Strauchsichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="24f5d-205">Strsafe Functions</span></span>



| <span data-ttu-id="24f5d-206">Name</span><span class="sxs-lookup"><span data-stu-id="24f5d-206">Name</span></span>                                             | <span data-ttu-id="24f5d-207">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24f5d-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24f5d-208">**Stringcbcat**</span><span class="sxs-lookup"><span data-stu-id="24f5d-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="24f5d-209">Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="24f5d-210">**Stringcb-Ex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="24f5d-211">Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="24f5d-212">**Stringcb-n**</span><span class="sxs-lookup"><span data-stu-id="24f5d-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="24f5d-213">Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge zu einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="24f5d-214">**Stringcbcr-x**</span><span class="sxs-lookup"><span data-stu-id="24f5d-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="24f5d-215">Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge zu einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="24f5d-216">**Stringcbcopy**</span><span class="sxs-lookup"><span data-stu-id="24f5d-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="24f5d-217">Kopiert eine Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="24f5d-218">**Stringcbcopyex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="24f5d-219">Kopiert eine Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="24f5d-220">**Stringcbcopyn**</span><span class="sxs-lookup"><span data-stu-id="24f5d-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="24f5d-221">Kopiert die angegebene Anzahl von Bytes von einer Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="24f5d-222">**Stringcbcopynetx**</span><span class="sxs-lookup"><span data-stu-id="24f5d-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="24f5d-223">Kopiert die angegebene Anzahl von Bytes von einer Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="24f5d-224">**Stringcbgets**</span><span class="sxs-lookup"><span data-stu-id="24f5d-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="24f5d-225">Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="24f5d-226">**Stringcbgetsex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="24f5d-227">Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="24f5d-228">**Stringcblength**</span><span class="sxs-lookup"><span data-stu-id="24f5d-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="24f5d-229">Bestimmt, ob eine Zeichenfolge die angegebene Länge in Bytes überschreitet.</span><span class="sxs-lookup"><span data-stu-id="24f5d-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="24f5d-230">**Stringcbprintf**</span><span class="sxs-lookup"><span data-stu-id="24f5d-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="24f5d-231">Schreibt formatierte Daten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="24f5d-232">**Stringcbprintfex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="24f5d-233">Schreibt formatierte Daten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="24f5d-234">**Stringcbvprintf**</span><span class="sxs-lookup"><span data-stu-id="24f5d-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="24f5d-235">Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="24f5d-236">**Stringcbvprintfex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="24f5d-237">Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="24f5d-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="24f5d-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="24f5d-239">Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="24f5d-240">**Stringcch| Ex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="24f5d-241">Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="24f5d-242">**Stringcch.**</span><span class="sxs-lookup"><span data-stu-id="24f5d-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="24f5d-243">Verkettet die angegebene Anzahl von Zeichen aus einer Zeichenfolge zu einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="24f5d-244">**Stringcchcatcher**</span><span class="sxs-lookup"><span data-stu-id="24f5d-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="24f5d-245">Verkettet die angegebene Anzahl von Zeichen aus einer Zeichenfolge zu einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="24f5d-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="24f5d-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="24f5d-247">Kopiert eine Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="24f5d-248">**Stringcchcopyex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="24f5d-249">Kopiert eine Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="24f5d-250">**Stringcchcopyn**</span><span class="sxs-lookup"><span data-stu-id="24f5d-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="24f5d-251">Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="24f5d-252">**Stringcchcopynetx**</span><span class="sxs-lookup"><span data-stu-id="24f5d-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="24f5d-253">Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.</span><span class="sxs-lookup"><span data-stu-id="24f5d-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="24f5d-254">**Stringcchgets**</span><span class="sxs-lookup"><span data-stu-id="24f5d-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="24f5d-255">Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="24f5d-256">**Stringcchgetsex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="24f5d-257">Ruft eine Textzeile von stdin bis einschließlich des Zeilen einzeiligen Zeichens (' \\ n ') ab.</span><span class="sxs-lookup"><span data-stu-id="24f5d-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="24f5d-258">**Stringcchlength**</span><span class="sxs-lookup"><span data-stu-id="24f5d-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="24f5d-259">Bestimmt, ob eine Zeichenfolge die angegebene Länge in Zeichen überschreitet.</span><span class="sxs-lookup"><span data-stu-id="24f5d-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="24f5d-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="24f5d-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="24f5d-261">Schreibt formatierte Daten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="24f5d-262">**Stringcchprintfex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="24f5d-263">Schreibt formatierte Daten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="24f5d-264">**Stringcchvprintf**</span><span class="sxs-lookup"><span data-stu-id="24f5d-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="24f5d-265">Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="24f5d-266">**Stringcchvprintfex**</span><span class="sxs-lookup"><span data-stu-id="24f5d-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="24f5d-267">Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24f5d-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

