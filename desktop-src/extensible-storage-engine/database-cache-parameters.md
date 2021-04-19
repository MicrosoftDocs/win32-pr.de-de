---
description: Weitere Informationen finden Sie in den Daten Bank Cache Parametern.
title: Daten Bank Cache Parameter
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360101"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="e258e-103">Daten Bank Cache Parameter</span><span class="sxs-lookup"><span data-stu-id="e258e-103">Database Cache Parameters</span></span>


<span data-ttu-id="e258e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e258e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="e258e-105">Daten Bank Cache Parameter</span><span class="sxs-lookup"><span data-stu-id="e258e-105">Database Cache Parameters</span></span>

<span data-ttu-id="e258e-106">Dieses Thema enthält Parameter, die für den Daten Bank Cache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="e258e-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="e258e-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="e258e-108">22</span><span class="sxs-lookup"><span data-stu-id="e258e-108">22</span></span>  

<span data-ttu-id="e258e-109">Dieser Parameter steuert die Größe eines zusätzlichen Teils des Datenbankseiten Caches, der zum Simulieren von e/a-Punkt erfassten e/a-Vorgängen verwendet wird, wenn diese andernfalls nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e258e-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="e258e-110">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="e258e-110">The size is in database pages.</span></span>

<span data-ttu-id="e258e-111">**Windows XP und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="e258e-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-112">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-113">256</span><span class="sxs-lookup"><span data-stu-id="e258e-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-114">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-115">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-116">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-117">0, 2 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="e258e-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-118">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-119">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-120">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-121">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-122">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-123">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-124">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-125">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-126">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-127">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-128">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-129">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-130">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-131">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-132">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-133">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="e258e-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="e258e-135">41</span><span class="sxs-lookup"><span data-stu-id="e258e-135">41</span></span>  

<span data-ttu-id="e258e-136">Dieser Parameter kann verwendet werden, um die Größe des Datenbankseiten Caches zur Laufzeit zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e258e-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="e258e-137">Normalerweise wird die Größe des Caches automatisch als Funktion der Datenbank-und Computer Aktivitäts Ebenen optimiert.</span><span class="sxs-lookup"><span data-stu-id="e258e-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="e258e-138">Wenn die Anwendung diesen Parameter auf 0 (null) festlegt, wird auf diese Weise der Cache seine eigene Größe optimieren.</span><span class="sxs-lookup"><span data-stu-id="e258e-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="e258e-139">Wenn die Anwendung diesen Parameter jedoch auf einen Wert ungleich 0 (null) festlegt, wird der Cache an die Zielgröße (in Datenbankseiten) angepasst.</span><span class="sxs-lookup"><span data-stu-id="e258e-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="e258e-140">Der Cache speichert dann seine Größe an diesem Schwellenwert, bis eine neue Größe angegeben wird, oder bis er freigegeben wird, um seine eigene Größe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e258e-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="e258e-141">**Hinweis**  Die Cache Größe unterliegt weiterhin den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** vorgegebenen Grenzwerten.</span><span class="sxs-lookup"><span data-stu-id="e258e-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="e258e-142">Wenn dieser Parameter gelesen wird, wird die tatsächliche Größe des Caches in Datenbankseiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e258e-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="e258e-143">Diese Größe kann von der Anwendung als Eingabe verwendet werden, um die manuelle Anpassung der Cache Größe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e258e-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-144">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-145">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="e258e-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-146">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-147">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-148">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-149"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="e258e-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="e258e-150"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-151">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-152">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-153">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-154">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-155">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-156">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-157">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-158">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-159">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-160">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-161">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-162">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-163">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-164">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-165">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-166">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="e258e-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="e258e-168">60</span><span class="sxs-lookup"><span data-stu-id="e258e-168">60</span></span>  

<span data-ttu-id="e258e-169">Dieser Parameter konfiguriert die Mindestgröße des Datenbankseiten Caches.</span><span class="sxs-lookup"><span data-stu-id="e258e-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="e258e-170">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="e258e-170">The size is in database pages.</span></span>

<span data-ttu-id="e258e-171">Standardmäßig wird die Größe des Daten Bank Caches automatisch zwischen den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** festgelegten Grenzwerten angepasst.</span><span class="sxs-lookup"><span data-stu-id="e258e-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="e258e-172">**Windows 2000:**  Unter Windows 2000 sollte dieser Parameter auf einen Wert festgelegt werden, der ungefähr so groß wie die Anzahl der Threads ist, die gleichzeitig in der ESE-API vorkommen werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="e258e-173">Dies ist erforderlich, um Deadlocks zu vermeiden, die durch eine unzureichende Anzahl von Datenbankseiten Cache Puffern verursacht werden, um komplexe Vorgänge wie B +-Struktur Teilungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e258e-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="e258e-174">**Windows XP und höher:**  Der Cache-Manager legt automatisch seine eigene minimale Cache Größe fest, um Deadlocks zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e258e-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-175">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-176"><strong>Windows 2000:</strong>  64</span><span class="sxs-lookup"><span data-stu-id="e258e-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="e258e-177"><strong>Windows XP:</strong>  1</span><span class="sxs-lookup"><span data-stu-id="e258e-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-178">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-179">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-180">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-181"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="e258e-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="e258e-182"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-183">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-184">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-185">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-186"><strong>Windows 2000:</strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="e258e-187"><strong>Windows XP:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="e258e-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-188">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-189"><strong>Windows 2000:</strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="e258e-190"><strong>Windows XP:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="e258e-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-191">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-192">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-193">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-194">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-195">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-196">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-197">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-198">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-199">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-200">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="e258e-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="e258e-202">23</span><span class="sxs-lookup"><span data-stu-id="e258e-202">23</span></span>  

<span data-ttu-id="e258e-203">Dieser Parameter konfiguriert die maximale Größe des Datenbankseiten Caches.</span><span class="sxs-lookup"><span data-stu-id="e258e-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="e258e-204">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="e258e-204">The size is in database pages.</span></span>

<span data-ttu-id="e258e-205">Standardmäßig wird die Größe des Daten Bank Caches automatisch zwischen den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** festgelegten Grenzwerten angepasst.</span><span class="sxs-lookup"><span data-stu-id="e258e-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="e258e-206">**Hinweis**   Wenn dieser Parameter auf seinen Standardwert zurückgesetzt wird, wird die maximale Cache Größe auf die Größe des physischen Arbeitsspeichers festgelegt, wenn [jetinit](./jetinit-function.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="e258e-207">**Windows Vista:**  Ab Windows Vista wurde der Standardwert dieses Parameters geändert, um dieses Verhalten zu verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="e258e-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-208">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-209"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  512</span><span class="sxs-lookup"><span data-stu-id="e258e-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="e258e-210"><strong>Windows Vista:</strong>  2 Milliarden</span><span class="sxs-lookup"><span data-stu-id="e258e-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-211">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-212">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-213">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-214"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="e258e-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="e258e-215"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-216">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-217">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-218">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-219"><strong>Windows 2000:</strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="e258e-220"><strong>Windows XP:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="e258e-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-221">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-222"><strong>Windows XP und Windows 2000:</strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="e258e-223"><strong>Windows Vista und Windows Server 2003:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="e258e-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-224">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-225">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-226">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-227">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-228">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-229">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-230">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-231">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-232">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-233">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="e258e-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="e258e-235">24</span><span class="sxs-lookup"><span data-stu-id="e258e-235">24</span></span> 

<span data-ttu-id="e258e-236">Mit diesem Parameter wird gesteuert, wie aggressiv Datenbankseiten aus dem Datenbankseiten Cache geleert werden, um die Zeitspanne zu minimieren, die für die Wiederherstellung nach einem Absturz benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="e258e-237">Der-Parameter ist ein Schwellenwert in Bytes, der angibt, wie viele Transaktionsprotokoll Dateien nach einem Absturz wiedergegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e258e-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="e258e-238">Wenn die zirkuläre Protokollierung mithilfe [JET_paramCircularLog](./transaction-log-parameters.md) aktiviert wird, steuert dieser Parameter auch die ungefähre Menge an Transaktionsprotokoll Dateien, die auf dem Datenträger beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="e258e-239">Es ist wichtig, dass dieser Parameter nicht zu niedrig festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="e258e-240">Da der Wert dieses Parameters NULL ist, wird der Cache beim Leeren von Datenbankseiten auf den Datenträger immer komplexer.</span><span class="sxs-lookup"><span data-stu-id="e258e-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="e258e-241">Dies führt nicht nur zu einer größeren Anzahl von Schreibvorgängen für die Datenbankdateien, sondern auch indirekt zu einer größeren Anzahl von Lesevorgängen für diese Dateien.</span><span class="sxs-lookup"><span data-stu-id="e258e-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="e258e-242">Dies kann in einigen Fällen sehr erhebliche Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="e258e-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="e258e-243">Leider kann das Festlegen des kleinsten optimalen Werts für diesen Parameter nur mithilfe von Experimenten mit der Zielanwendung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e258e-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-244">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-245">20971520</span><span class="sxs-lookup"><span data-stu-id="e258e-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-246">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-247">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-248">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-249"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="e258e-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="e258e-250"><strong>Windows Vista:</strong>  Alle Werte</span><span class="sxs-lookup"><span data-stu-id="e258e-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-251">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-252"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> Dieser Parameter ist Global.</span><span class="sxs-lookup"><span data-stu-id="e258e-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="e258e-253"><strong>Windows Vista:</strong>  Dieser Parameter ist pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="e258e-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-254">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-255">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-256">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-257">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-258">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-259">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-260">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-261">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-262">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-263">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-264">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-265">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-266">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-267">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="e258e-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="e258e-269">135</span><span class="sxs-lookup"><span data-stu-id="e258e-269">135</span></span>  

<span data-ttu-id="e258e-270">Dieser Parameter steuert die maximale Anzahl von gleichzeitigen Schreibvorgängen, die von der Datenbank-Engine verwendet werden, um geänderte Datenbankseiten zum Zweck der Weiterentwicklung des Prüf Punkts zu leeren.</span><span class="sxs-lookup"><span data-stu-id="e258e-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="e258e-271">Der Wert dieses Parameters kann verwendet werden, um die Geschwindigkeit auszugleichen, mit der der Prüfpunkt erweitert werden kann, im Vergleich zu den negativen Auswirkungen, die dieser Prozess für die Antwortzeit für andere e/a-Vorgänge auf die Datenträger mit der Datenbank hat.</span><span class="sxs-lookup"><span data-stu-id="e258e-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-272">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-273">96</span><span class="sxs-lookup"><span data-stu-id="e258e-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-274">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-275">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-276">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-277">8 – 1024</span><span class="sxs-lookup"><span data-stu-id="e258e-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-278">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-279">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-280">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-281">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-282">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-283">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-284">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-285">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-286">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-287">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-288">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-289">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-290">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-291">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-292">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-293">Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="e258e-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="e258e-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="e258e-295">127</span><span class="sxs-lookup"><span data-stu-id="e258e-295">127</span></span>  

<span data-ttu-id="e258e-296">Wenn dieser Parameter **true** ist, verwendet die Datenbank-Engine Datenbankdaten direkt aus dem Windows-Dateicache, anstatt die zwischengespeicherten Daten in ihren eigenen privaten Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="e258e-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="e258e-297">Alle geänderten Datenbankdaten werden weiterhin im privaten Speicher zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="e258e-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="e258e-298">Der Zweck dieses Modus besteht darin, den Umfang des privaten Speichers, der von der Datenbank-Engine zum Zwischenspeichern von Datenbankdaten verwendet wird, weiter zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="e258e-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="e258e-299">Der Ansichts Cache kann nur verwendet werden, wenn die Verwendung des Windows-Datei Caches aktiviert ist, indem JET_paramEnableFileCache auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-300">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-301">False</span><span class="sxs-lookup"><span data-stu-id="e258e-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-302">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="e258e-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-304">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-305">False, True</span><span class="sxs-lookup"><span data-stu-id="e258e-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-306">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-307">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-308">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-309">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-310">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-311">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-312">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-313">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-314">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-315">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-316">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-317">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-318">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-319">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-320">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-321">Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="e258e-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="e258e-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="e258e-323">25</span><span class="sxs-lookup"><span data-stu-id="e258e-323">25</span></span>  

<span data-ttu-id="e258e-324">Mit diesem Parameter wird das Zeitintervall in Mikrosekunden festgelegt, in dem zwei Datenbankseiten Zugriffe als korreliert angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="e258e-325">Mit diesem Korrelations Intervall wird die Vertraulichkeit des Seiten Ersetzungs Algorithmus (LRU-K) zwischen Cache und aufeinander folgenden Seiten Zugriffen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e258e-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="e258e-326">Dies wirkt sich wiederum auf die Seiten aus, die für die Zwischenspeicherung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-327">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-328">128000</span><span class="sxs-lookup"><span data-stu-id="e258e-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-329">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-330">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-331">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-332"><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="e258e-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="e258e-333"><strong>Windows Vista:</strong>  Alle Werte</span><span class="sxs-lookup"><span data-stu-id="e258e-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-334">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-335">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-336">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-337">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-338">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-339">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-340">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-341">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-342">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-343">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-344">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-345">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-346">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-347">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-348">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-349">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="e258e-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="e258e-351">26</span><span class="sxs-lookup"><span data-stu-id="e258e-351">26</span></span>  

<span data-ttu-id="e258e-352">Mit diesem Parameter wird die maximale Anzahl nicht zwischen gespeicherter Datenbankseiten festgelegt, für die Datenbankseiten Zugriffszeiten beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="e258e-353">Diese Verlaufs Datensätze ermöglichen es dem Cache mit dem Seiten Ersetzungs Algorithmus (LRU-K), beliebte Seiten, die fälschlicherweise aus dem Datenbankseiten Cache entfernt wurden, genauer zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="e258e-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="e258e-354">**Windows XP und Windows Server 2003:**  Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="e258e-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-355">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-356"><strong>Windows 2000:</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="e258e-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="e258e-357"><strong>Windows Vista:</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="e258e-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-358">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-359">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-360">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-361"><strong>Windows 2000:</strong>  0 – 4194303</span><span class="sxs-lookup"><span data-stu-id="e258e-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="e258e-362"><strong>Windows Vista:</strong>  Alle Werte</span><span class="sxs-lookup"><span data-stu-id="e258e-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-363">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-364">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-365">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-366">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-367">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-368">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-369">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-370">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-371">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-372">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-373">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-374">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-375">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-376">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-377">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-378">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="e258e-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="e258e-380">27</span><span class="sxs-lookup"><span data-stu-id="e258e-380">27</span></span>  

<span data-ttu-id="e258e-381">Mit diesem Parameter wird die Anzahl der Datenbankseiten Zugriffe konfiguriert, die zum Ermitteln der Nützlichkeit der Seite berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="e258e-382">Bei diesem Parameter handelt es sich im Wesentlichen um das k in LRU-K, den Seiten Ersetzungs Algorithmus des Datenbankseiten Caches.</span><span class="sxs-lookup"><span data-stu-id="e258e-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-383">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-384">2</span><span class="sxs-lookup"><span data-stu-id="e258e-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-385">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-386">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-387">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-388">1 - 2</span><span class="sxs-lookup"><span data-stu-id="e258e-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-389">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-390">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-391">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-392">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-393">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-394">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-395">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-396">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-397">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-398">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-399">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-400">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-401">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-402">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-403">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-404">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="e258e-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="e258e-406">28</span><span class="sxs-lookup"><span data-stu-id="e258e-406">28</span></span>

<span data-ttu-id="e258e-407">Dieser Parameter gibt den Zeitraum in Sekunden an, nach dem eine Seite im Datenbankseiten Cache einen Seiten Zugriff verloren hat, um die Nützlichkeit der Seite zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e258e-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-408">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-409">100</span><span class="sxs-lookup"><span data-stu-id="e258e-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-410">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-411">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-412">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-413"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="e258e-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="e258e-414"><strong>Windows Vista:</strong>   1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-415">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-416">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-417">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-418">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-419">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-420">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-421">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-422">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-423">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-424">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-425">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-426">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-427">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-428">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-429">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-430">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="e258e-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="e258e-432">29</span><span class="sxs-lookup"><span data-stu-id="e258e-432">29</span></span>  

<span data-ttu-id="e258e-433">Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="e258e-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="e258e-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="e258e-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="e258e-435">31</span><span class="sxs-lookup"><span data-stu-id="e258e-435">31</span></span>  

<span data-ttu-id="e258e-436">Mit diesem Parameter wird gesteuert, wann der Datenbankseiten Cache mit der Erstellung von Seiten aus dem Cache beginnt, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="e258e-437">Wenn die Anzahl der Seiten Puffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um den Pool der verfügbaren Puffer aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="e258e-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="e258e-438">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von **JET_paramCacheSizeMax** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="e258e-439">Dieser Schwellenwert muss auch immer niedriger als der von **JET_paramStopFlushThreshold** festgelegte Schwellenwert sein.</span><span class="sxs-lookup"><span data-stu-id="e258e-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="e258e-440">Die Entfernungs Höhe des Start Schwellenwerts bestimmt die Antwortzeit, die der Datenbankseiten Cache aufweisen muss, damit verfügbare Puffer erstellt werden, bevor die Anwendung Sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="e258e-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="e258e-441">Ein Schwellenwert für hohe Starts gibt dem Hintergrundprozess mehr Zeit für die Reaktion.</span><span class="sxs-lookup"><span data-stu-id="e258e-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="e258e-442">Ein Schwellenwert für hohe Starts impliziert jedoch einen höheren Schwellenwert für die Beendigung, wodurch die effektive Größe des Datenbankseiten Caches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-443">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-444"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="e258e-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="e258e-445"><strong>Windows Vista:</strong>  20 Millionen (1%)</span><span class="sxs-lookup"><span data-stu-id="e258e-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-446">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-447">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-448">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-449"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="e258e-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="e258e-450"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="e258e-451"><strong>Windows Vista:</strong>  Alle Werte</span><span class="sxs-lookup"><span data-stu-id="e258e-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-452">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-453">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-454">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-455">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-456">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-457">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-458">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-459">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-460">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-461">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-462">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-463">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-464">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-465">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-466">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-467">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e258e-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="e258e-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="e258e-469">32</span><span class="sxs-lookup"><span data-stu-id="e258e-469">32</span></span>  

<span data-ttu-id="e258e-470">Mit diesem Parameter wird gesteuert, wann der Datenbankseiten Cache das Entfernen von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="e258e-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="e258e-471">Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e258e-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="e258e-472">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von **JET_paramCacheSizeMax** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="e258e-473">Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch **JET_paramStartFlushThreshold** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e258e-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="e258e-474">Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="e258e-475">Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="e258e-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="e258e-476">Durch einen Schwellenwert für hohe Beendigung wird jedoch die effektive Größe des Datenbankseiten Caches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) verringert.</span><span class="sxs-lookup"><span data-stu-id="e258e-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-477">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="e258e-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e258e-478"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="e258e-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="e258e-479"><strong>Windows Vista:</strong>  40 Millionen (2%)</span><span class="sxs-lookup"><span data-stu-id="e258e-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-480">Typ:</span><span class="sxs-lookup"><span data-stu-id="e258e-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="e258e-481">Integer</span><span class="sxs-lookup"><span data-stu-id="e258e-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-482">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="e258e-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e258e-483"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="e258e-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="e258e-484"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="e258e-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="e258e-485"><strong>Windows Vista:</strong>  Alle Werte</span><span class="sxs-lookup"><span data-stu-id="e258e-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-486">Umfang:</span><span class="sxs-lookup"><span data-stu-id="e258e-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e258e-487">Global</span><span class="sxs-lookup"><span data-stu-id="e258e-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-488">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-489">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-490">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="e258e-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e258e-491">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-492">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="e258e-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e258e-493">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-494">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-495">Nein</span><span class="sxs-lookup"><span data-stu-id="e258e-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-496">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="e258e-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e258e-497">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-498">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e258e-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e258e-499">Ja</span><span class="sxs-lookup"><span data-stu-id="e258e-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-500">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="e258e-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e258e-501">Alle</span><span class="sxs-lookup"><span data-stu-id="e258e-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e258e-502">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e258e-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e258e-503"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e258e-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e258e-504">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e258e-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e258e-505"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e258e-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e258e-506">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e258e-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e258e-507"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e258e-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e258e-508">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e258e-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e258e-509">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e258e-509">See Also</span></span>

[<span data-ttu-id="e258e-510">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="e258e-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e258e-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="e258e-511">JetInit</span></span>](./jetinit-function.md)
