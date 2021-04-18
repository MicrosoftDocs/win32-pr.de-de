---
description: Eine Reihe von Faktoiden beschreibt Eingaben, die für alle sprach erkenungen gelten und keine unterschiedlichen Formate für verschiedene Sprachen aufweisen müssen. In der folgenden Tabelle sind die in allen Sprachen gemeinsamen Faktoide aufgeführt.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Sprachen übergreifende Facetten übergreifende Faktoide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343696"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="e22bf-104">Sprachen übergreifende Facetten übergreifende Faktoide</span><span class="sxs-lookup"><span data-stu-id="e22bf-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="e22bf-105">Eine Reihe von Faktoiden beschreibt Eingaben, die für alle sprach erkenungen gelten und keine unterschiedlichen Formate für verschiedene Sprachen aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="e22bf-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="e22bf-106">In der folgenden Tabelle sind die in allen Sprachen gemeinsamen Faktoide aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e22bf-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e22bf-107">Faktoid</span><span class="sxs-lookup"><span data-stu-id="e22bf-107">Factoid</span></span></th>
<th><span data-ttu-id="e22bf-108">Definition</span><span class="sxs-lookup"><span data-stu-id="e22bf-108">Definition</span></span></th>
<th><span data-ttu-id="e22bf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e22bf-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22bf-110"><strong>Mittleren</strong></span><span class="sxs-lookup"><span data-stu-id="e22bf-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="e22bf-111">Legt den Wert für eine einzelne Ziffer fest.</span><span class="sxs-lookup"><span data-stu-id="e22bf-111">Sets bias for a single digit.</span></span> <span data-ttu-id="e22bf-112">Die Erkennung ist darauf ausgerichtet, nur einzelne Ziffern zurückzugeben, wenn diese Faktoid festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e22bf-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="e22bf-113">0-9</span><span class="sxs-lookup"><span data-stu-id="e22bf-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22bf-114"><strong>E-Mail</strong></span><span class="sxs-lookup"><span data-stu-id="e22bf-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="e22bf-115">Legt einen Bias für eine e-Mail-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="e22bf-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e22bf-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="e22bf-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="e22bf-117">Legt die Abweichung für verschiedene URL-Formate fest.</span><span class="sxs-lookup"><span data-stu-id="e22bf-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e22bf-118">Die Standardeinstellungen für die Erkennung beinhalten das <strong>webfaktoid</strong> .</span><span class="sxs-lookup"><span data-stu-id="e22bf-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="e22bf-119">Daher bemerken Sie möglicherweise keinen großen Unterschied zwischen der <strong>webfaktoid</strong> und der Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="e22bf-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="e22bf-120">Die <strong>Web</strong> -ID unterstützt jedoch die Beseitigung von Leerzeichen zwischen Wörtern in einer URL.</span><span class="sxs-lookup"><span data-stu-id="e22bf-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e22bf-121">http: \\ Microsoft.net</span><span class="sxs-lookup"><span data-stu-id="e22bf-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="e22bf-122">https: \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="e22bf-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="e22bf-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="e22bf-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="e22bf-124">www.Microsoft.US </span><span class="sxs-lookup"><span data-stu-id="e22bf-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="e22bf-125">http: \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="e22bf-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="e22bf-126">http: \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="e22bf-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="e22bf-127">http: \\ www. Microsoft. com\meinedatei.ASP</span><span class="sxs-lookup"><span data-stu-id="e22bf-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="e22bf-128">http: \\ www.Microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="e22bf-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="e22bf-129">http: \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="e22bf-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="e22bf-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="e22bf-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22bf-131"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="e22bf-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="e22bf-132">Gibt die Erkennungsfunktion auf die Standardeinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="e22bf-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="e22bf-133">Die Standardeinstellung für Faktoide für westliche Sprachen umfasst das System Wörterbuch, das Benutzerwörterbuch, verschiedene interpunlierungen und die <strong>Web</strong> -und <strong>Number</strong> -Faktoide.</span><span class="sxs-lookup"><span data-stu-id="e22bf-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="e22bf-134">Die Standardeinstellung für Faktoide für ostasiatische Sprachen enthält alle Zeichen, die von der Erkennung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e22bf-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e22bf-135"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="e22bf-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="e22bf-136">Deaktiviert alle Faktoide, Wörterbücher und das Sprachmodell.</span><span class="sxs-lookup"><span data-stu-id="e22bf-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="e22bf-137">Diese Faktoid sollte nur verwendet werden, wenn Sie nicht möchten, dass die Erkennung Grammatikregeln oder-Wörterbücher verwendet, einschließlich des System Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="e22bf-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="e22bf-138">Diese Faktoid eignet sich für die Eingabe zufälliger Zeichen folgen, wie z. b. Produktcodes.</span><span class="sxs-lookup"><span data-stu-id="e22bf-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="e22bf-139">Verwenden Sie das coerce-Flag nicht mit diesem Faktoid.</span><span class="sxs-lookup"><span data-stu-id="e22bf-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




