---
description: 'Weitere Informationen finden Sie hier: Meta Parameters'
title: Meta-Parameter
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345675"
---
# <a name="meta-parameters"></a><span data-ttu-id="10f83-103">Meta-Parameter</span><span class="sxs-lookup"><span data-stu-id="10f83-103">Meta Parameters</span></span>


<span data-ttu-id="10f83-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="10f83-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="10f83-105">Meta-Parameter</span><span class="sxs-lookup"><span data-stu-id="10f83-105">Meta Parameters</span></span>

<span data-ttu-id="10f83-106">Dieses Thema enthält Parameter, die verwendet werden, um andere Parameter zu steuern.</span><span class="sxs-lookup"><span data-stu-id="10f83-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="10f83-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="10f83-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="10f83-108">129</span><span class="sxs-lookup"><span data-stu-id="10f83-108">129</span></span>  
<span data-ttu-id="10f83-109">Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10f83-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="10f83-110">Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="10f83-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="10f83-111">Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="10f83-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="10f83-112">Außerdem kann der Parameter selbst andere Auswirkungen auf das Verhalten der Datenbank-Engine haben.</span><span class="sxs-lookup"><span data-stu-id="10f83-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="10f83-113">Zurzeit werden zwei Konfigurationen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="10f83-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="10f83-114">Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.</span><span class="sxs-lookup"><span data-stu-id="10f83-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="10f83-115">Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="10f83-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="10f83-116">Bei der kleinen Konfiguration werden die Standardwerte der folgenden Systemparameter auf die angegebenen Werte geändert:</span><span class="sxs-lookup"><span data-stu-id="10f83-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10f83-117">System Parameter</span><span class="sxs-lookup"><span data-stu-id="10f83-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="10f83-118">Neuer Standardwert</span><span class="sxs-lookup"><span data-stu-id="10f83-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10f83-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="10f83-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="10f83-120">30.000</span><span class="sxs-lookup"><span data-stu-id="10f83-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="10f83-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="10f83-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="10f83-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="10f83-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="10f83-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="10f83-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="10f83-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="10f83-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="10f83-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="10f83-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="10f83-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="10f83-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="10f83-130">64</span><span class="sxs-lookup"><span data-stu-id="10f83-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="10f83-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="10f83-132">1</span><span class="sxs-lookup"><span data-stu-id="10f83-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="10f83-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="10f83-134">16</span><span class="sxs-lookup"><span data-stu-id="10f83-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="10f83-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="10f83-136">14</span><span class="sxs-lookup"><span data-stu-id="10f83-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="10f83-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="10f83-138">16</span><span class="sxs-lookup"><span data-stu-id="10f83-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="10f83-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="10f83-140">65536</span><span class="sxs-lookup"><span data-stu-id="10f83-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="10f83-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="10f83-142">10</span><span class="sxs-lookup"><span data-stu-id="10f83-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="10f83-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="10f83-144">16</span><span class="sxs-lookup"><span data-stu-id="10f83-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="10f83-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="10f83-146">1</span><span class="sxs-lookup"><span data-stu-id="10f83-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="10f83-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="10f83-148">2</span><span class="sxs-lookup"><span data-stu-id="10f83-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="10f83-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="10f83-150">1</span><span class="sxs-lookup"><span data-stu-id="10f83-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="10f83-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="10f83-152">16</span><span class="sxs-lookup"><span data-stu-id="10f83-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="10f83-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="10f83-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="10f83-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="10f83-156">0</span><span class="sxs-lookup"><span data-stu-id="10f83-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="10f83-158">1</span><span class="sxs-lookup"><span data-stu-id="10f83-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="10f83-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="10f83-160">32</span><span class="sxs-lookup"><span data-stu-id="10f83-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="10f83-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="10f83-162">1</span><span class="sxs-lookup"><span data-stu-id="10f83-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="10f83-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="10f83-164">1</span><span class="sxs-lookup"><span data-stu-id="10f83-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="10f83-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="10f83-166">1</span><span class="sxs-lookup"><span data-stu-id="10f83-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="10f83-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="10f83-168">1024</span><span class="sxs-lookup"><span data-stu-id="10f83-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="10f83-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="10f83-170">0</span><span class="sxs-lookup"><span data-stu-id="10f83-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="10f83-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="10f83-172">8</span><span class="sxs-lookup"><span data-stu-id="10f83-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10f83-173">Die kleine Konfiguration hat auch eine Reihe weiterer Auswirkungen auf die Datenbank-Engine, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="10f83-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="10f83-174">Alle durch Systemparameter verwalteten Ressourcen werden nach Bedarf aus dem Heap zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="10f83-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="10f83-175">Andere interne Ressourcen, die von der Datenbank-Engine verwendet werden, werden zentral herunterskaliert.</span><span class="sxs-lookup"><span data-stu-id="10f83-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="10f83-176">Verschiedene Wartungsaktivitäten werden wieder herunterskaliert, um Hintergrund Thread Aktivitäten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="10f83-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10f83-177">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="10f83-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="10f83-178">1 (Legacy)</span><span class="sxs-lookup"><span data-stu-id="10f83-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-179">Typ:</span><span class="sxs-lookup"><span data-stu-id="10f83-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="10f83-180">Integer</span><span class="sxs-lookup"><span data-stu-id="10f83-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-181">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="10f83-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="10f83-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="10f83-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-183">Umfang:</span><span class="sxs-lookup"><span data-stu-id="10f83-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="10f83-184">Instanz</span><span class="sxs-lookup"><span data-stu-id="10f83-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-185">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="10f83-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="10f83-186">Ja</span><span class="sxs-lookup"><span data-stu-id="10f83-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-187">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="10f83-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="10f83-188">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-189">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="10f83-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="10f83-190">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-191">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="10f83-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="10f83-192">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-193">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="10f83-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="10f83-194">Ja</span><span class="sxs-lookup"><span data-stu-id="10f83-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-195">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="10f83-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="10f83-196">Ja</span><span class="sxs-lookup"><span data-stu-id="10f83-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-197">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="10f83-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="10f83-198">Ab Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10f83-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10f83-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="10f83-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="10f83-200">130</span><span class="sxs-lookup"><span data-stu-id="10f83-200">130</span></span>  
<span data-ttu-id="10f83-201">Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="10f83-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="10f83-202">Dieser Parameter wird zusammen mit JET_paramConfiguration verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="10f83-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="10f83-203">Die folgenden Systemparameter werden vor der Festlegung geschützt, wenn dieser Parameter auf "false" festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="10f83-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="10f83-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="10f83-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="10f83-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="10f83-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="10f83-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="10f83-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="10f83-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="10f83-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="10f83-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="10f83-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="10f83-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="10f83-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="10f83-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="10f83-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="10f83-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="10f83-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="10f83-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="10f83-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="10f83-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="10f83-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="10f83-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="10f83-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="10f83-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="10f83-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="10f83-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="10f83-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="10f83-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="10f83-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="10f83-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="10f83-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="10f83-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="10f83-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="10f83-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="10f83-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="10f83-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="10f83-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="10f83-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="10f83-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="10f83-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="10f83-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="10f83-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="10f83-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="10f83-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="10f83-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="10f83-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="10f83-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="10f83-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="10f83-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="10f83-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="10f83-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="10f83-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="10f83-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="10f83-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="10f83-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="10f83-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="10f83-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="10f83-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="10f83-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="10f83-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="10f83-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="10f83-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="10f83-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="10f83-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="10f83-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="10f83-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="10f83-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="10f83-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="10f83-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="10f83-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="10f83-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="10f83-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="10f83-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="10f83-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="10f83-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="10f83-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="10f83-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="10f83-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="10f83-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10f83-244">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="10f83-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="10f83-245">Richtig</span><span class="sxs-lookup"><span data-stu-id="10f83-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-246">Typ:</span><span class="sxs-lookup"><span data-stu-id="10f83-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="10f83-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="10f83-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-248">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="10f83-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="10f83-249">False, True</span><span class="sxs-lookup"><span data-stu-id="10f83-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-250">Umfang:</span><span class="sxs-lookup"><span data-stu-id="10f83-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="10f83-251">Instanz</span><span class="sxs-lookup"><span data-stu-id="10f83-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-252">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="10f83-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="10f83-253">Ja</span><span class="sxs-lookup"><span data-stu-id="10f83-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-254">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="10f83-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="10f83-255">Ja</span><span class="sxs-lookup"><span data-stu-id="10f83-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-256">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="10f83-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="10f83-257">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-258">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="10f83-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="10f83-259">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-260">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="10f83-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="10f83-261">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-262">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="10f83-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="10f83-263">Nein</span><span class="sxs-lookup"><span data-stu-id="10f83-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-264">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="10f83-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="10f83-265">Ab Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10f83-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="10f83-266">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f83-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10f83-267"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="10f83-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="10f83-268">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10f83-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f83-269"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="10f83-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="10f83-270">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10f83-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f83-271"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="10f83-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="10f83-272">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="10f83-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="10f83-273">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="10f83-273">See Also</span></span>

[<span data-ttu-id="10f83-274">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="10f83-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="10f83-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="10f83-275">JetInit</span></span>](./jetinit-function.md)
