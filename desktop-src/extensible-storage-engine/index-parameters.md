---
description: 'Weitere Informationen finden Sie hier: Index Parameter'
title: Indexparameter
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050540"
---
# <a name="index-parameters"></a><span data-ttu-id="89448-103">Indexparameter</span><span class="sxs-lookup"><span data-stu-id="89448-103">Index Parameters</span></span>


<span data-ttu-id="89448-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="89448-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="89448-105">Indexparameter</span><span class="sxs-lookup"><span data-stu-id="89448-105">Index Parameters</span></span>

<span data-ttu-id="89448-106">Dieses Thema enthält Parameter, die für den Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89448-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="89448-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="89448-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="89448-108">132</span><span class="sxs-lookup"><span data-stu-id="89448-108">132</span></span>  

<span data-ttu-id="89448-109">Dieser Parameter gibt den Standardwert für das Offset Inkrement an, mit dem der Wert der Quell Spalte durchlaufen wird, während jedes Tupel erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="89448-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="89448-110">Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="89448-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-111">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-112">1</span><span class="sxs-lookup"><span data-stu-id="89448-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-114">Integer</span><span class="sxs-lookup"><span data-stu-id="89448-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-115">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="89448-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-117">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-118">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-119">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-120">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-121">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-122">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-123">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-124">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-125">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-126">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-127">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-128">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-129">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-130">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-131">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-132">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="89448-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89448-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="89448-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="89448-134">133</span><span class="sxs-lookup"><span data-stu-id="89448-134">133</span></span>  

<span data-ttu-id="89448-135">Dieser Parameter gibt den Standardwert für den Offset in dem Wert der Quell Spalte an, ab dem die tupelgenerierung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="89448-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="89448-136">Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="89448-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-137">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-138">0</span><span class="sxs-lookup"><span data-stu-id="89448-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-139">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-140">Integer</span><span class="sxs-lookup"><span data-stu-id="89448-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-141">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="89448-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-143">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-144">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-145">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-146">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-147">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-148">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-149">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-150">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-151">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-152">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-153">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-154">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-155">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-156">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-157">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-158">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="89448-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89448-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="89448-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="89448-160">111</span><span class="sxs-lookup"><span data-stu-id="89448-160">111</span></span>  

<span data-ttu-id="89448-161">Dieser Parameter gibt den Standardwert für die maximale tupellänge in einem Tupelindex an.</span><span class="sxs-lookup"><span data-stu-id="89448-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="89448-162">Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="89448-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="89448-163">**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="89448-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89448-164">Für Windows Vista wird dies nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89448-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-165">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-166">10</span><span class="sxs-lookup"><span data-stu-id="89448-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-167">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-168">Integer</span><span class="sxs-lookup"><span data-stu-id="89448-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-169">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-170"><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="89448-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="89448-171"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="89448-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-172">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-173">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-174">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-175">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-176">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-177">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-178">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-179">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-180">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-181">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-182">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-183">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-184">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-185">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-186">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-187">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="89448-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89448-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="89448-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="89448-189">110</span><span class="sxs-lookup"><span data-stu-id="89448-189">110</span></span>  

<span data-ttu-id="89448-190">Dieser Parameter gibt den Standardwert für die minimale tupellänge in einem Tupelindex an.</span><span class="sxs-lookup"><span data-stu-id="89448-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="89448-191">Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89448-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="89448-192">**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="89448-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89448-193">Für Windows Vista wird dies nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89448-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-194">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-195">3</span><span class="sxs-lookup"><span data-stu-id="89448-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-196">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-197">Integer</span><span class="sxs-lookup"><span data-stu-id="89448-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-198">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-199"><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="89448-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="89448-200"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="89448-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-201">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-202">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-203">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-204">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-205">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-206">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-207">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-208">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-209">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-210">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-211">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-212">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-213">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-214">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-215">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-216">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="89448-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89448-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="89448-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="89448-218">112</span><span class="sxs-lookup"><span data-stu-id="89448-218">112</span></span>  

<span data-ttu-id="89448-219">Dieser Parameter gibt den Standardwert für die maximale Länge einer Quell Zeichenfolge an, um für einen Tupelindex in Tupel zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="89448-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="89448-220">Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89448-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="89448-221">**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="89448-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89448-222">Für Windows Vista wird dies nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89448-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-223">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-224">32767</span><span class="sxs-lookup"><span data-stu-id="89448-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-225">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-226">Integer</span><span class="sxs-lookup"><span data-stu-id="89448-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-227">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-228"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="89448-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="89448-229"><strong>Windows Vista:</strong>  1 – 32767</span><span class="sxs-lookup"><span data-stu-id="89448-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-230">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-231">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-232">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-233">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-234">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-235">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-236">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-237">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-238">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-239">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-240">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-241">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-242">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-243">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-244">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-245">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="89448-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89448-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="89448-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="89448-247">72</span><span class="sxs-lookup"><span data-stu-id="89448-247">72</span></span>  

<span data-ttu-id="89448-248">Dieser Parameter steuert die Unicode-Standardparameter, die von einem beliebigen Index für eine Unicode-Schlüssel Spalte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89448-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="89448-249">Der Typ dieses Parameters ist [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) und wird tatsächlich mithilfe eines Puffer Zeigers übergeben, der im Integer-Parameter von [jetgetsystemparameter](./jetgetsystemparameter-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md)gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="89448-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="89448-250">Die Größe des Puffers muss der Größe des [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) entsprechen und mithilfe des Parameters für die Zeichen folgen Puffergröße an [jetgetsystemparameter](./jetgetsystemparameter-function.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="89448-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="89448-251">Dies ist eindeutig inkonsistent, aber das Verhalten dieses Parameters.</span><span class="sxs-lookup"><span data-stu-id="89448-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="89448-252">Der Standardwert dieses Parameters enthält eine LCID für das US-englische Gebiets Schema und die folgenden [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="89448-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="89448-253">**Windows 2000:**  Die Element-ID in der LCID wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="89448-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="89448-254">Eine Element-ID von SORT_DEFAULT wird immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="89448-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="89448-255">**Windows 2000:**  Die [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) -Flags müssen die folgenden Flags enthalten: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="89448-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="89448-256">Außerdem können die [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags die folgenden Flags enthalten: NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="89448-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="89448-257">**Hinweis**  Wenn Ihre Anwendung Unicode-Daten speichern möchte, wird dringend empfohlen, nicht auf die standardmäßigen Unicode-Parameter für die Indizes zu vertrauen.</span><span class="sxs-lookup"><span data-stu-id="89448-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="89448-258">Die Verwendung von US-Englisch ist gleichbedeutend mit der Verwendung des invarianten Gebiets Schemas, und die standardmäßigen [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags sind bekannt, dass einige Sprachen ernsthaft beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="89448-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="89448-259">Sie sollten mit [JET_INDEXCREATE](./jet-indexcreate-structure.md)immer eigene Einstellungen für die Unicode-Parameter für JetCreateIndex2 angeben.</span><span class="sxs-lookup"><span data-stu-id="89448-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-260">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="89448-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89448-261">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="89448-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-262">Typ:</span><span class="sxs-lookup"><span data-stu-id="89448-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="89448-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="89448-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-264">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="89448-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89448-265">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="89448-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-266">Umfang:</span><span class="sxs-lookup"><span data-stu-id="89448-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89448-267">Instanz</span><span class="sxs-lookup"><span data-stu-id="89448-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-268">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-269">Ja</span><span class="sxs-lookup"><span data-stu-id="89448-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-270">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="89448-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89448-271">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-272">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="89448-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89448-273">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-274">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89448-275">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-276">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="89448-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89448-277">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-278">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="89448-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89448-279">Nein</span><span class="sxs-lookup"><span data-stu-id="89448-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-280">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="89448-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89448-281">Alle</span><span class="sxs-lookup"><span data-stu-id="89448-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="89448-282">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89448-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89448-283"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="89448-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89448-284">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="89448-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89448-285"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="89448-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89448-286">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="89448-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89448-287"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="89448-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89448-288">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="89448-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="89448-289">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="89448-289">See Also</span></span>

[<span data-ttu-id="89448-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="89448-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="89448-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="89448-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="89448-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="89448-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="89448-293">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="89448-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="89448-294">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="89448-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="89448-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="89448-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="89448-296">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="89448-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
