---
description: 'Weitere Informationen finden Sie hier: Informations Parameter'
title: Informations Parameter
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753320"
---
# <a name="informational-parameters"></a><span data-ttu-id="e478e-103">Informations Parameter</span><span class="sxs-lookup"><span data-stu-id="e478e-103">Informational Parameters</span></span>


<span data-ttu-id="e478e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e478e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="e478e-105">Informations Parameter</span><span class="sxs-lookup"><span data-stu-id="e478e-105">Informational Parameters</span></span>

<span data-ttu-id="e478e-106">Dieses Thema enthält Parameter, die verwendet werden, um Informationen über die Datenbank-Engine verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e478e-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="e478e-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="e478e-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="e478e-108">134</span><span class="sxs-lookup"><span data-stu-id="e478e-108">134</span></span>  

<span data-ttu-id="e478e-109">Dieser schreibgeschützte Parameter gibt die maximal zulässige Länge des Index Schlüssels an, die für die aktuelle Datenbankseiten Größe (wie von JET_paramDatabasePageSize konfiguriert) ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e478e-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e478e-110">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e478e-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e478e-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="e478e-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-112">Typ:</span><span class="sxs-lookup"><span data-stu-id="e478e-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="e478e-113">Integer</span><span class="sxs-lookup"><span data-stu-id="e478e-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-114">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e478e-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e478e-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="e478e-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-116">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e478e-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e478e-117">Global</span><span class="sxs-lookup"><span data-stu-id="e478e-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-118">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e478e-119">–</span><span class="sxs-lookup"><span data-stu-id="e478e-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-120">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e478e-121">–</span><span class="sxs-lookup"><span data-stu-id="e478e-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-122">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e478e-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e478e-123">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-124">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e478e-125">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-126">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e478e-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e478e-127">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-128">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e478e-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e478e-129">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-130">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e478e-131">Ab Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e478e-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e478e-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="e478e-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="e478e-133">131</span><span class="sxs-lookup"><span data-stu-id="e478e-133">131</span></span>  

<span data-ttu-id="e478e-134">Dieser Read Only-Parameter gibt den maximalen [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) für diese Version der Datenbank-Engine zurück.</span><span class="sxs-lookup"><span data-stu-id="e478e-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="e478e-135">Dieser Wert kann verwendet werden, um die Unterstützung einer bestimmten [JET_COLTYP](./jet-coltyp.md)zu testen.</span><span class="sxs-lookup"><span data-stu-id="e478e-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="e478e-136">Wenn eine angegebene [JET_COLTYP](./jet-coltyp.md) kleiner als der Wert dieses Parameters ist, wird Sie von der Datenbank-Engine unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e478e-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e478e-137">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e478e-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e478e-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="e478e-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-139">Typ:</span><span class="sxs-lookup"><span data-stu-id="e478e-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="e478e-140">Integer</span><span class="sxs-lookup"><span data-stu-id="e478e-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-141">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e478e-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e478e-142">0 – 255</span><span class="sxs-lookup"><span data-stu-id="e478e-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-143">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e478e-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e478e-144">Global</span><span class="sxs-lookup"><span data-stu-id="e478e-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-145">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e478e-146">–</span><span class="sxs-lookup"><span data-stu-id="e478e-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-147">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e478e-148">–</span><span class="sxs-lookup"><span data-stu-id="e478e-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-149">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e478e-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e478e-150">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-151">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e478e-152">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-153">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e478e-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e478e-154">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-155">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e478e-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e478e-156">Nein</span><span class="sxs-lookup"><span data-stu-id="e478e-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-157">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e478e-158">Ab Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e478e-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e478e-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="e478e-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="e478e-160">163</span><span class="sxs-lookup"><span data-stu-id="e478e-160">163</span></span>  

<span data-ttu-id="e478e-161">Schreib geschützter Parameter, der die Segmentgröße mit langem Wert basierend auf der konfigurierten Seitengröße zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e478e-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="e478e-162">Wenn ein langer Wert mit mehreren Jet {Set-, retrieve}-Spalten aufrufen gelesen oder geschrieben werden soll, ist die Verwendung eines Puffers, dessen Größe ein Vielfaches der Blockgröße ist, effizienter.</span><span class="sxs-lookup"><span data-stu-id="e478e-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e478e-163">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e478e-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e478e-164">2 KB Seite = 1966 bytes</span><span class="sxs-lookup"><span data-stu-id="e478e-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="e478e-165">4 KB Seite = 4014 bytes</span><span class="sxs-lookup"><span data-stu-id="e478e-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="e478e-166">8 KB Seite = 8110 bytes</span><span class="sxs-lookup"><span data-stu-id="e478e-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="e478e-167">16-KB-Seite = 4050 bytes</span><span class="sxs-lookup"><span data-stu-id="e478e-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="e478e-168">32 KB Seite = 8150 bytes</span><span class="sxs-lookup"><span data-stu-id="e478e-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-169">Typ:</span><span class="sxs-lookup"><span data-stu-id="e478e-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="e478e-170">Integer</span><span class="sxs-lookup"><span data-stu-id="e478e-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-171">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e478e-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e478e-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="e478e-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-173">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e478e-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-174">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-175">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e478e-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-176">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e478e-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-177">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-178">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e478e-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-179">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e478e-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-180">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e478e-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e478e-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e478e-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e478e-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e478e-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e478e-183">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e478e-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e478e-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e478e-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e478e-185">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e478e-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e478e-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e478e-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e478e-187">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e478e-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e478e-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e478e-188">See Also</span></span>

[<span data-ttu-id="e478e-189">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="e478e-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e478e-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="e478e-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="e478e-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e478e-191">JET_COLTYP</span></span>](./jet-coltyp.md)
