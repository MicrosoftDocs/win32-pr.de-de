---
description: Gebiets Schema \_ Rückgabe \* Konstanten
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217804"
---
# <a name="locale_return-constants"></a><span data-ttu-id="9f566-103">Gebiets Schema \_ Rückgabe \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="9f566-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="9f566-104">In diesem Thema werden die \_ \* von NLS verwendeten Gebiets Schema Rückgabe Konstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="9f566-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f566-105">Wert</span><span class="sxs-lookup"><span data-stu-id="9f566-105">Value</span></span></th>
<th><span data-ttu-id="9f566-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f566-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f566-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="9f566-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="9f566-108"><strong>Windows 7 und höher:</strong> Rufen Sie die Namen von Monaten ab, bei denen es sich um die Namen handelt, die verwendet werden, wenn die Monatsnamen mit anderen Elementen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9f566-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="9f566-109">Beispielsweise wird in Ukrainisch die Entsprechung von Januar geschrieben, &quot; &quot; Wenn der Monat allein benannt wird.</span><span class="sxs-lookup"><span data-stu-id="9f566-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="9f566-110">Wenn jedoch der Monats Name in Kombination verwendet wird, z. b. in einem Datum wie dem 5. Januar 2003, wird das Format des Namens verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f566-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="9f566-111">Im Beispiel "Ukrainisch" wird der Name des "Genitive Month" als &quot; 2003 5 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9f566-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="9f566-112">Die Liste mit den Namen der Namen des Genies beginnt mit Januar und ist durch Semikolon getrennt.</span><span class="sxs-lookup"><span data-stu-id="9f566-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="9f566-113">Wenn kein 13. Monat vorhanden ist, verwenden Sie ein Semikolon am Ende der Liste.</span><span class="sxs-lookup"><span data-stu-id="9f566-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f566-114">In allen Sprachen sind keine Namen für das audiotive Monats vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9f566-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f566-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="9f566-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="9f566-116"><strong>Windows Me/98, Windows NT 4,0 und höher:</strong> Ruft eine Zahl ab.</span><span class="sxs-lookup"><span data-stu-id="9f566-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="9f566-117">Diese Konstante bewirkt, dass <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>getlocaleingefo</strong></a> oder <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>getlocaleingefoex</strong></a> einen Wert als Zahl anstelle von als Zeichenfolge abruft.</span><span class="sxs-lookup"><span data-stu-id="9f566-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="9f566-118">Der Puffer, der den Wert empfängt, muss mindestens die Länge eines DWORD-Werts haben.</span><span class="sxs-lookup"><span data-stu-id="9f566-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="9f566-119">Diese Konstante kann mit einer beliebigen anderen Konstante mit einem Namen kombiniert werden, der mit &quot; LOCALE_I beginnt &quot; .</span><span class="sxs-lookup"><span data-stu-id="9f566-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




