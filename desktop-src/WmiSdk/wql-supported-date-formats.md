---
description: Beschreibt Datumsformate, die für die Verwendung in der WQL WHERE-Klausel unterstützt werden.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported Datumsformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865652"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="56ac7-103">WQL-Supported Datumsformate</span><span class="sxs-lookup"><span data-stu-id="56ac7-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="56ac7-104">Zusätzlich zum WMI- **DateTime** -Format werden die folgenden Datumsformate für die Verwendung in der WQL- **Where** -Klausel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56ac7-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="56ac7-105">Das angezeigte Zeitformat unterscheidet sich für verschiedene Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="56ac7-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="56ac7-106">Bei Skripts, die eine Verbindung mit Remote Computern herstellen, muss die Zeit in dem für das Gebiets Schema des Ziel Computers geeigneten Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56ac7-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="56ac7-107">Beispielsweise ist das Datums-und Uhrzeit Format von USA mm-dd-yyyy.</span><span class="sxs-lookup"><span data-stu-id="56ac7-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="56ac7-108">Wenn ein Skript auf einem US-Computer eine Verbindung mit einem Zielcomputer in einem Gebiets Schema herstellt, bei dem das Format dd-mm-yyyy ist, werden Abfragen auf dem Zielcomputer als dd-mm-yyyy verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56ac7-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="56ac7-109">Um unterschiedliche Ergebnisse zwischen Gebiets Schemas zu vermeiden, verwenden Sie das [**DateTime**](datetime.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="56ac7-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="56ac7-110">Weitere Informationen finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="56ac7-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56ac7-111">Format</span><span class="sxs-lookup"><span data-stu-id="56ac7-111">Format</span></span></th>
<th><span data-ttu-id="56ac7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56ac7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56ac7-113">Mon [TH] DD [,] [yy] JJ</span><span class="sxs-lookup"><span data-stu-id="56ac7-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="56ac7-114">Monat (in drei Buchstaben geschrieben oder abgekürzt), Tag, optionales Komma und zwei oder vierstellige Jahres Angabe.</span><span class="sxs-lookup"><span data-stu-id="56ac7-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="56ac7-115">21. Januar 1932</span><span class="sxs-lookup"><span data-stu-id="56ac7-115">January 21, 1932</span></span><br />
<span data-ttu-id="56ac7-116">21. Januar 32</span><span class="sxs-lookup"><span data-stu-id="56ac7-116">January 21, 32</span></span><br />
<span data-ttu-id="56ac7-117">Jan 21 1932</span><span class="sxs-lookup"><span data-stu-id="56ac7-117">Jan 21 1932</span></span><br />
<span data-ttu-id="56ac7-118">Jan 21 32</span><span class="sxs-lookup"><span data-stu-id="56ac7-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-119">Mon [TH] [,] JJJJ</span><span class="sxs-lookup"><span data-stu-id="56ac7-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="56ac7-120">Monat (in drei Buchstaben geschrieben oder abgekürzt), optionales Komma und vierstellige Jahres Angabe.</span><span class="sxs-lookup"><span data-stu-id="56ac7-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="56ac7-121">1932. Januar</span><span class="sxs-lookup"><span data-stu-id="56ac7-121">January 1932</span></span><br />
<span data-ttu-id="56ac7-122">Jan 1932</span><span class="sxs-lookup"><span data-stu-id="56ac7-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-123">Mon [TH] [yy] JJ DD</span><span class="sxs-lookup"><span data-stu-id="56ac7-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="56ac7-124">Monat (in drei Buchstaben geschrieben oder abgekürzt), zwei oder vierstellige Jahres Angabe und Tag.</span><span class="sxs-lookup"><span data-stu-id="56ac7-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="56ac7-125">1932 21. Januar</span><span class="sxs-lookup"><span data-stu-id="56ac7-125">January 1932 21</span></span><br />
<span data-ttu-id="56ac7-126">Jan 32 21</span><span class="sxs-lookup"><span data-stu-id="56ac7-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-127">DD Mon [TH] [,] [] [yy] y</span><span class="sxs-lookup"><span data-stu-id="56ac7-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="56ac7-128">Tag des Monats, Monats (entweder in drei Buchstaben geschrieben oder abgekürzt), optionales Komma, optionaler Bereich und zwei oder vierstellige Jahres Angabe.</span><span class="sxs-lookup"><span data-stu-id="56ac7-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="56ac7-129">21. Januar 1932</span><span class="sxs-lookup"><span data-stu-id="56ac7-129">21 January, 1932</span></span><br />
<span data-ttu-id="56ac7-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="56ac7-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-131">DD [jj] yy Mon [TH]</span><span class="sxs-lookup"><span data-stu-id="56ac7-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="56ac7-132">Tag des Monats, zwei-oder vierstellige Jahres Angabe und Monat (entweder in drei Buchstaben ausgeloebener oder abgekürzt).</span><span class="sxs-lookup"><span data-stu-id="56ac7-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="56ac7-133">21 1932. Januar</span><span class="sxs-lookup"><span data-stu-id="56ac7-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-134">[jj] y [TH] DD</span><span class="sxs-lookup"><span data-stu-id="56ac7-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="56ac7-135">Zwei-oder vierstellige Jahres Angabe, Monat (entweder in drei Buchstaben eingeblendet oder abgekürzt) und Tag.</span><span class="sxs-lookup"><span data-stu-id="56ac7-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="56ac7-136">1932. Januar 21</span><span class="sxs-lookup"><span data-stu-id="56ac7-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-137">JJJJ Mon [TH]</span><span class="sxs-lookup"><span data-stu-id="56ac7-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="56ac7-138">Zwei-oder vierstellige Jahres-und Monats Angabe (in drei Buchstaben geschrieben oder abgekürzt).</span><span class="sxs-lookup"><span data-stu-id="56ac7-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="56ac7-139">1932. Januar</span><span class="sxs-lookup"><span data-stu-id="56ac7-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-140">JJJJ DD Mon [TH]</span><span class="sxs-lookup"><span data-stu-id="56ac7-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="56ac7-141">Zwei-oder vierstellige Jahres Angabe, Tag und Monat (entweder in drei Buchstaben eingeblendet oder abgekürzt).</span><span class="sxs-lookup"><span data-stu-id="56ac7-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="56ac7-142">1932 21. Januar</span><span class="sxs-lookup"><span data-stu-id="56ac7-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-143">800 M {/-.} DD {/-.} [jj] JJ</span><span class="sxs-lookup"><span data-stu-id="56ac7-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="56ac7-144">Monat, Tag und zwei oder vierstellige Jahres Angabe.</span><span class="sxs-lookup"><span data-stu-id="56ac7-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="56ac7-145">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-146">DD {/-.} 800 M {/-.} [jj] JJ</span><span class="sxs-lookup"><span data-stu-id="56ac7-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="56ac7-147">Tag des Monats, Monats und zwei oder vierstelligen Jahres Angabe.</span><span class="sxs-lookup"><span data-stu-id="56ac7-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="56ac7-148">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-149">800 M {/-.} [jj] JJ {/-.} benutzen</span><span class="sxs-lookup"><span data-stu-id="56ac7-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="56ac7-150">Monat, zwei oder vierstellige Jahres Angabe und Tag.</span><span class="sxs-lookup"><span data-stu-id="56ac7-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="56ac7-151">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-152">DD {/-.} [jj] JJ {/-.} 800 800</span><span class="sxs-lookup"><span data-stu-id="56ac7-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="56ac7-153">Tag des Monats, zwei oder vierstellige Jahres Angabe und Monat.</span><span class="sxs-lookup"><span data-stu-id="56ac7-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="56ac7-154">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-155">[jj] JJ {/-.} DD {/-.} 800 800</span><span class="sxs-lookup"><span data-stu-id="56ac7-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="56ac7-156">Zwei oder vierstellige Jahres Angabe, Tag und Monat.</span><span class="sxs-lookup"><span data-stu-id="56ac7-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="56ac7-157">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-158">[jj] JJ {/-.} 800 M {/-.} benutzen</span><span class="sxs-lookup"><span data-stu-id="56ac7-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="56ac7-159">Zwei oder vierstellige Ziffern (Jahr, Monat und Tag).</span><span class="sxs-lookup"><span data-stu-id="56ac7-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="56ac7-160">Beachten Sie, dass die Trennzeichen identisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56ac7-161">[jj] YYMMDD</span><span class="sxs-lookup"><span data-stu-id="56ac7-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="56ac7-162">Zwei-oder vierstellige Ziffern (Jahr, Monat und Tag) ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56ac7-163">yyyy [mm [DD]]</span><span class="sxs-lookup"><span data-stu-id="56ac7-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="56ac7-164">Zwei-oder vierstellige Jahres Angabe, optionaler Monat und optionaler Tag ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="56ac7-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="56ac7-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56ac7-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ac7-166">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="56ac7-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




