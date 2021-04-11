---
description: LOCALE \_ idigitsubstitution
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128117"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="635a7-103">LOCALE \_ idigitsubstitution</span><span class="sxs-lookup"><span data-stu-id="635a7-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="635a7-104">**Windows 2000:** Die Form der Ziffern.</span><span class="sxs-lookup"><span data-stu-id="635a7-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="635a7-105">Beispielsweise haben arabische, thailändische und indic-Ziffern klassische Formen, die sich von den europäischen Ziffern unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="635a7-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="635a7-106">Für Gebiets Schemas mit Gebiets [ \_ Schema-snativedigits](locale-snative-constants.md) , die als andere Werte als ASCII 0-9 angegeben werden, gibt dieser Wert an, ob die anderen Ziffern zu Anzeige Zwecken bevorzugt angegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="635a7-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="635a7-107">Wenn z. b. der Wert 2 ausgewählt wird, werden die von locale \_ snativedigits angegebenen Ziffern immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="635a7-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="635a7-108">Wenn 1 ausgewählt wird, werden die ASCII 0-9-Ziffern immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="635a7-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="635a7-109">Wenn 0 ausgewählt wird, wird in einigen Fällen ASCII verwendet, und die durch \_ das Gebiets Schema (snativedigits) angegebenen Ziffern werden je nach Kontext in anderen verwendet.</span><span class="sxs-lookup"><span data-stu-id="635a7-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="635a7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="635a7-110">Value</span></span></th>
<th><span data-ttu-id="635a7-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="635a7-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="635a7-112">0</span><span class="sxs-lookup"><span data-stu-id="635a7-112">0</span></span></td>
<td><span data-ttu-id="635a7-113">Kontextbasierte Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="635a7-113">Context-based substitution.</span></span> <span data-ttu-id="635a7-114">Ziffern werden basierend auf dem vorherigen Text in der gleichen Ausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="635a7-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="635a7-115">Europäische Ziffern folgen lateinischen Skripts, Arabic-Indic Ziffern auf arabischen Text, und andere nationale Ziffern folgen dem Text, der in verschiedenen anderen Skripts geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="635a7-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="635a7-116">Wenn kein vorheriger Text vorhanden ist, bestimmen das Gebiets Schema und die angezeigte Lesereihenfolge die Ziffern Ersetzung, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="635a7-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="635a7-117">Gebietsschema</span><span class="sxs-lookup"><span data-stu-id="635a7-117">Locale</span></span></th>
<th><span data-ttu-id="635a7-118">Lesereihenfolge</span><span class="sxs-lookup"><span data-stu-id="635a7-118">Reading order</span></span></th>
<th><span data-ttu-id="635a7-119">Verwendete Ziffern</span><span class="sxs-lookup"><span data-stu-id="635a7-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="635a7-120">Arabisch</span><span class="sxs-lookup"><span data-stu-id="635a7-120">Arabic</span></span></td>
<td><span data-ttu-id="635a7-121">Von rechts nach links</span><span class="sxs-lookup"><span data-stu-id="635a7-121">Right-to-left</span></span></td>
<td><span data-ttu-id="635a7-122">Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="635a7-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="635a7-123">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="635a7-123">Thai</span></span></td>
<td><span data-ttu-id="635a7-124">Von links nach rechts</span><span class="sxs-lookup"><span data-stu-id="635a7-124">Left-to-right</span></span></td>
<td><span data-ttu-id="635a7-125">Thailändische Ziffern</span><span class="sxs-lookup"><span data-stu-id="635a7-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="635a7-126">Alle anderen</span><span class="sxs-lookup"><span data-stu-id="635a7-126">All others</span></span></td>
<td><span data-ttu-id="635a7-127">Any</span><span class="sxs-lookup"><span data-stu-id="635a7-127">Any</span></span></td>
<td><span data-ttu-id="635a7-128">Keine Ersetzung verwendet</span><span class="sxs-lookup"><span data-stu-id="635a7-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="635a7-129">1</span><span class="sxs-lookup"><span data-stu-id="635a7-129">1</span></span></td>
<td><span data-ttu-id="635a7-130">Es wurde keine Ersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="635a7-130">No substitution used.</span></span> <span data-ttu-id="635a7-131">Vollständige Unicode-Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="635a7-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="635a7-132">2</span><span class="sxs-lookup"><span data-stu-id="635a7-132">2</span></span></td>
<td><span data-ttu-id="635a7-133">Native Ziffern Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="635a7-133">Native digit substitution.</span></span> <span data-ttu-id="635a7-134">Nationale Formen werden nach LOCALE_SNATIVEDIGITS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="635a7-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



