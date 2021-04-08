---
description: '\_Smonthname- \* Konstanten für locale'
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: LOCALE_SMONTHNAME *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752801"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="5ac99-103">\_Smonthname- \* Konstanten für locale</span><span class="sxs-lookup"><span data-stu-id="5ac99-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="5ac99-104">In diesem Thema werden die \_ von NLS verwendeten locale smonthname- \* Konstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="5ac99-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ac99-105">Wert</span><span class="sxs-lookup"><span data-stu-id="5ac99-105">Value</span></span></th>
<th><span data-ttu-id="5ac99-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5ac99-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ac99-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="5ac99-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="5ac99-108">Der Native lange Name für Januar.</span><span class="sxs-lookup"><span data-stu-id="5ac99-108">Native long name for January.</span></span> <span data-ttu-id="5ac99-109">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5ac99-110">Wenn Sie die <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> -Funktion oder die <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> -Funktion mit einer LOCALE_SMONTHNAME \*-Konstante aufrufen, wird die eigenständige oder nominative Form des Monats namens zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ac99-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="5ac99-111">Um die Form des Monats namens abzurufen, ruft die Anwendung <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">getDateFormat</a> oder <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> mit einem Datums Bild von ddmmmm auf und entfernt die beiden Ziffern am Anfang der abgerufenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ac99-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="5ac99-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="5ac99-113">Der Native lange Name für Februar.</span><span class="sxs-lookup"><span data-stu-id="5ac99-113">Native long name for February.</span></span> <span data-ttu-id="5ac99-114">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-115">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="5ac99-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="5ac99-117">Der Native lange Name für März.</span><span class="sxs-lookup"><span data-stu-id="5ac99-117">Native long name for March.</span></span> <span data-ttu-id="5ac99-118">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-119">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="5ac99-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="5ac99-121">Der Native lange Name für April.</span><span class="sxs-lookup"><span data-stu-id="5ac99-121">Native long name for April.</span></span> <span data-ttu-id="5ac99-122">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-123">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="5ac99-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="5ac99-125">Der Native lange Name für Mai.</span><span class="sxs-lookup"><span data-stu-id="5ac99-125">Native long name for May.</span></span> <span data-ttu-id="5ac99-126">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-127">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="5ac99-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="5ac99-129">Der Native lange Name für Juni.</span><span class="sxs-lookup"><span data-stu-id="5ac99-129">Native long name for June.</span></span> <span data-ttu-id="5ac99-130">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-131">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="5ac99-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="5ac99-133">Der Native lange Name für Juli.</span><span class="sxs-lookup"><span data-stu-id="5ac99-133">Native long name for July.</span></span> <span data-ttu-id="5ac99-134">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-135">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="5ac99-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="5ac99-137">Der Native lange Name für August.</span><span class="sxs-lookup"><span data-stu-id="5ac99-137">Native long name for August.</span></span> <span data-ttu-id="5ac99-138">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-139">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="5ac99-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="5ac99-141">Der Native lange Name für September.</span><span class="sxs-lookup"><span data-stu-id="5ac99-141">Native long name for September.</span></span> <span data-ttu-id="5ac99-142">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-143">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="5ac99-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="5ac99-145">Der Native lange Name für Oktober.</span><span class="sxs-lookup"><span data-stu-id="5ac99-145">Native long name for October.</span></span> <span data-ttu-id="5ac99-146">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-147">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="5ac99-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="5ac99-149">Der Native lange Name für November.</span><span class="sxs-lookup"><span data-stu-id="5ac99-149">Native long name for November.</span></span> <span data-ttu-id="5ac99-150">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-151">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ac99-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="5ac99-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="5ac99-153">Der Native lange Name für Dezember.</span><span class="sxs-lookup"><span data-stu-id="5ac99-153">Native long name for December.</span></span> <span data-ttu-id="5ac99-154">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-155">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ac99-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="5ac99-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="5ac99-157">Der Native Name für einen 13. Monat, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5ac99-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="5ac99-158">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ac99-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="5ac99-159">Weitere Informationen finden Sie unter LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="5ac99-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




