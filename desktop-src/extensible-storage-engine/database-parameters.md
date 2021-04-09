---
description: 'Weitere Informationen finden Sie hier: Daten Bank Parameter'
title: Datenbankparameter
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130200"
---
# <a name="database-parameters"></a><span data-ttu-id="52685-103">Datenbankparameter</span><span class="sxs-lookup"><span data-stu-id="52685-103">Database Parameters</span></span>


<span data-ttu-id="52685-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52685-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="52685-105">Datenbankparameter</span><span class="sxs-lookup"><span data-stu-id="52685-105">Database Parameters</span></span>

<span data-ttu-id="52685-106">Dieses Thema enthält Parameter, die für die-Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52685-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="52685-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="52685-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="52685-108">44</span><span class="sxs-lookup"><span data-stu-id="52685-108">44</span></span>  

<span data-ttu-id="52685-109">Wenn dieser Parameter festgelegt wird, gibt [jetinit](./jetinit-function.md) einen besonderen Fehler zurück, wenn eine Datenbank oder ein Transaktionsprotokoll einer früheren Version der Datenbank-Engine geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="52685-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="52685-110">Folgende Fehler sind aufgetreten:</span><span class="sxs-lookup"><span data-stu-id="52685-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52685-111">Fehler</span><span class="sxs-lookup"><span data-stu-id="52685-111">Error</span></span></p></th>
<th><p><span data-ttu-id="52685-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52685-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="52685-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="52685-114">Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden mit der Datenbank-Engine in Windows NT 3,51 erstellt.</span><span class="sxs-lookup"><span data-stu-id="52685-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="52685-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="52685-116">Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden in einer Testversion vor Windows NT Server 4,0 mit der Datenbank-Engine erstellt.</span><span class="sxs-lookup"><span data-stu-id="52685-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="52685-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="52685-118">Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden mit der Datenbank-Engine in Windows NT Server 4,0 erstellt.</span><span class="sxs-lookup"><span data-stu-id="52685-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-119">**Windows Vista:**  Für Windows Vista und höher ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="52685-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-120">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-121">Richtig</span><span class="sxs-lookup"><span data-stu-id="52685-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-122">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="52685-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-124">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-125">False, True</span><span class="sxs-lookup"><span data-stu-id="52685-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-126">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-127">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-128">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-129">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-130">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-131">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-132">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-133">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-134">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-135">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-136">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-137">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-138">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-139">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-140">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-141">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="52685-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="52685-143">64</span><span class="sxs-lookup"><span data-stu-id="52685-143">64</span></span>  

<span data-ttu-id="52685-144">Dieser Parameter konfiguriert die Seitengröße für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="52685-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="52685-145">Die Seitengröße ist die kleinste Einheit der Speicherplatz Zuordnung, die für eine Datenbankdatei möglich ist.</span><span class="sxs-lookup"><span data-stu-id="52685-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="52685-146">Die Größe der Datenbankseite ist ebenfalls sehr wichtig, da Sie die Obergrenze für die Größe eines einzelnen Datensatzes in der Datenbank festlegt.</span><span class="sxs-lookup"><span data-stu-id="52685-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="52685-147">**Hinweis** Zurzeit wird pro Prozess nur eine Datenbankseiten Größe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52685-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="52685-148">Dies bedeutet, dass Sie, wenn Sie sich in einem einzelnen Prozess befinden, der verschiedene Anwendungen enthält, die die Datenbank-Engine verwenden, alle für eine Datenbankseiten Größe zustimmen müssen.</span><span class="sxs-lookup"><span data-stu-id="52685-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-149">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-150">4096</span><span class="sxs-lookup"><span data-stu-id="52685-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-151">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-152">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-153">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="52685-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-155">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-156">Global</span><span class="sxs-lookup"><span data-stu-id="52685-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-157">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-158">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-159">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-160">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-161">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-162">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-163">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-164">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-165">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-166">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-167">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-168">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-169">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-170">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="52685-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="52685-172">18</span><span class="sxs-lookup"><span data-stu-id="52685-172">18</span></span>  

<span data-ttu-id="52685-173">Mit diesem Parameter wird die Menge des Speicherplatzes gesteuert, der einer Datenbankdatei hinzugefügt wird, wenn Sie vergrößert werden muss, um mehr Daten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="52685-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="52685-174">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="52685-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-175">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-176">256</span><span class="sxs-lookup"><span data-stu-id="52685-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-177">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-178">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-179">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-180">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="52685-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-181">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-182">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-183">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-184">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-185">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-186">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-186">No</span></span></p>
<p><span data-ttu-id="52685-187"><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</span><span class="sxs-lookup"><span data-stu-id="52685-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-188">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-189">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-190">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-191">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-192">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-193">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-194">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-195">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-196">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-197">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="52685-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="52685-199">45</span><span class="sxs-lookup"><span data-stu-id="52685-199">45</span></span>  

<span data-ttu-id="52685-200">Wenn dieser Parameter true ist, wird jede Datenbank bei der [jetattachdatabase](./jetattachdatabase-function.md) -Zeit für Indizes über Unicode-Schlüssel Spalten geprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="52685-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="52685-201">Dies muss erreicht werden, da die Datenbank-Engine die von [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) generierten Sortierschlüssel beibehält und der Wert dieser Sortierschlüssel von Release zu Release geändert wird.</span><span class="sxs-lookup"><span data-stu-id="52685-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="52685-202">Wenn ein primärer Index in diesem Status erkannt wird, schlägt [jetattachdatabase](./jetattachdatabase-function.md) immer mit JET_errPrimaryIndexCorrupted fehl.</span><span class="sxs-lookup"><span data-stu-id="52685-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="52685-203">Wenn sekundäre Indizes in diesem Status erkannt werden, gibt es zwei mögliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="52685-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="52685-204">Wenn JET_bitDbDeleteCorruptIndexes an [jetattachdatabase](./jetattachdatabase-function.md) weitergeleitet wurde, werden diese Indizes gelöscht, und JET_wrnCorruptIndexDeleted wird von [jetattachdatabase](./jetattachdatabase-function.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52685-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="52685-205">Diese Indizes müssen von Ihrer Anwendung neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="52685-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="52685-206">Wenn JET_bitDbDeleteCorruptIndexes nicht an [jetattachdatabase](./jetattachdatabase-function.md) weitergegeben wurde, schlägt der-Rückruf mit JET_errSecondaryIndexCorrupted fehl.</span><span class="sxs-lookup"><span data-stu-id="52685-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="52685-207">**Hinweis** Es wird dringend empfohlen, dass dieser Parameter von Ihrer Anwendung auf true festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="52685-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="52685-208">**Hinweis** Es wird dringend empfohlen, dass Anwendungen die Verwendung von Unicode-Schlüssel Spalten in ihren Primärschlüssel Indizes (gruppierte Indizes) vermeiden.</span><span class="sxs-lookup"><span data-stu-id="52685-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-209">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-210">False</span><span class="sxs-lookup"><span data-stu-id="52685-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-211">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="52685-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-213">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-214">False, True</span><span class="sxs-lookup"><span data-stu-id="52685-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-215">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-216">Global</span><span class="sxs-lookup"><span data-stu-id="52685-216">Global</span></span></p>
<p><span data-ttu-id="52685-217"><strong>Windows Vista:</strong>  Für Windows Vista und höher: Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-218">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-219">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-220">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-221">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-222">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-223">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-224">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-225">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-226">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-227">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-228">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-229">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-230">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-231">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="52685-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="52685-233">54</span><span class="sxs-lookup"><span data-stu-id="52685-233">54</span></span>  

<span data-ttu-id="52685-234">Wenn dieser Parameter auf "true" festgelegt ist, kann die Datenbank-Engine ggf. Indizes über Unicode-Schlüssel Spalten automatisch bereinigen [, um Daten](./jetinit-function.md) Bank Formatänderungen zu vermeiden, die durch Änderungen an der NLS-Bibliothek in Windows verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="52685-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="52685-235">Diese Änderungen werden regelmäßig an der NLS-Bibliothek vorgenommen, um Unterstützung für neue Sprachen hinzuzufügen, einer Sprache fehlende Zeichen hinzuzufügen, einer Sprache eine Sortierreihenfolge hinzuzufügen oder Fehler in der Sortierreihenfolge einer Sprache zu beheben.</span><span class="sxs-lookup"><span data-stu-id="52685-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="52685-236">Diese Änderungen wirken sich auf die von [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) erzeugten Sortierschlüssel aus, die von der Datenbank-Engine als Komponenten von Index Schlüsseln persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="52685-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="52685-237">Es ist wichtig zu wissen, dass es möglich ist, dass die Änderungen am Index so groß sind, dass eine inkrementelle Bereinigung nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="52685-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="52685-238">In diesem Fall wird der Index wie von **JET_paramEnableIndexChecking** vorgeschrieben behandelt.</span><span class="sxs-lookup"><span data-stu-id="52685-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="52685-239">**Hinweis** Es wird dringend empfohlen, diesen Parameter und **JET_paramEnableIndexChecking** von Ihrer Anwendung auf **true** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52685-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-240">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="52685-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-242">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="52685-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-244">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-245">False, True</span><span class="sxs-lookup"><span data-stu-id="52685-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-246">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-247">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-248">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-249">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-250">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-251">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-251">No</span></span></p>
<p><span data-ttu-id="52685-252"><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</span><span class="sxs-lookup"><span data-stu-id="52685-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-253">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-254">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-255">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-256">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-257">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-258">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-259">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-260">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-261">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-262">Windows Server 2003 und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="52685-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="52685-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="52685-264">102</span><span class="sxs-lookup"><span data-stu-id="52685-264">102</span></span>  

<span data-ttu-id="52685-265">Wenn dieser Parameter true ist, kann jeweils nur eine Datenbank von einer bestimmten Sitzung aus mit [jetopddatabase](./jetopendatabase-function.md) geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="52685-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="52685-266">Die temporäre Datenbank wird von dieser Einschränkung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="52685-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="52685-267">**Windows XP und Windows Server 2003:**  Dieser Parameter ist nur unter Windows XP und Windows Server 2003 schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52685-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="52685-268">**Windows Vista:**  Dieser Parameter verhält sich normal mit Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52685-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="52685-269">**Hinweis**  Dieser Parameter ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52685-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-270">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-271">False</span><span class="sxs-lookup"><span data-stu-id="52685-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-272">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="52685-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-274">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-275">False, True</span><span class="sxs-lookup"><span data-stu-id="52685-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-276">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-277">Global</span><span class="sxs-lookup"><span data-stu-id="52685-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-278">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-279">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-279">No</span></span></p>
<p><span data-ttu-id="52685-280"><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</span><span class="sxs-lookup"><span data-stu-id="52685-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-281">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-282">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-283">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-284">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-285">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-286">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-287">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-288">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-289">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-290">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-291">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-292">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="52685-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="52685-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="52685-294">35</span><span class="sxs-lookup"><span data-stu-id="52685-294">35</span></span>  

<span data-ttu-id="52685-295">Dieser Parameter steuert das Verhalten der Online Defragmentierung, wenn es mithilfe von [jetdefragment](./jetdefragment-function.md)initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="52685-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="52685-296">Weitere Informationen finden Sie unter [jetdefragment](./jetdefragment-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52685-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="52685-297">Windows 2000: bei Windows 2000 war dieser Parameter ein einfacher boolescher Wert, der eine Online Defragmentierung durchführt, wenn er von [jetdefragment](./jetdefragment-function.md)initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="52685-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="52685-298">Wenn diese Einstellung auf " **true**" festgelegt ist, wird die Online Defragmentierung für die Datensätze der einzelnen Tabellen in der Datenbank ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52685-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="52685-299">**Windows XP:**  Unter Windows XP und höheren Versionen kann dieser Parameter auf eine oder mehrere der folgenden Optionen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="52685-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52685-300">Option</span><span class="sxs-lookup"><span data-stu-id="52685-300">Option</span></span></p></th>
<th><p><span data-ttu-id="52685-301">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52685-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="52685-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="52685-303">Führen Sie keine Online Defragmentierung durch.</span><span class="sxs-lookup"><span data-stu-id="52685-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="52685-304">Dies ist das binäre Äquivalent zur Windows 2000-Einstellung false für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="52685-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="52685-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="52685-306">Führen Sie eine vollständige Online Defragmentierung durch.</span><span class="sxs-lookup"><span data-stu-id="52685-306">Perform full online defragmentation.</span></span> <span data-ttu-id="52685-307">Dies ist die Binärdatei, die der Einstellung "true" von Windows 2000 für diesen Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="52685-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="52685-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="52685-309">Führt eine Online Defragmentierung der Datensätze der einzelnen Tabellen in der Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="52685-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="52685-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="52685-311">Führt eine Online Defragmentierung der Leerräume der einzelnen Tabellen in der Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="52685-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="52685-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="52685-313">Dieser Parameter wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="52685-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="52685-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="52685-315">Führen Sie eine vollständige Online Defragmentierung durch.</span><span class="sxs-lookup"><span data-stu-id="52685-315">Perform full online defragmentation.</span></span> <span data-ttu-id="52685-316">Dies ist das konzeptionelle Äquivalent zur Windows 2000-Einstellung true für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="52685-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-317">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-318"><strong>Windows 2000:</strong>  Fall</span><span class="sxs-lookup"><span data-stu-id="52685-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="52685-319"><strong>Windows XP: für Windows XP und höher:</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="52685-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-320">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-321"><strong>Windows 2000:</strong>  Booleschen</span><span class="sxs-lookup"><span data-stu-id="52685-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="52685-322"><strong>Windows XP und höher:</strong>  JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="52685-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-323">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-324"><strong>Windows 2000:</strong>  False, true</span><span class="sxs-lookup"><span data-stu-id="52685-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="52685-325"><strong>Windows XP und höher:</strong>  0 – JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="52685-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-326">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-327">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-328">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-329">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-330">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-331">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-332">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-333">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-334">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-335">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-336">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-337">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-338">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-339">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-340">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-341">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="52685-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="52685-343">20</span><span class="sxs-lookup"><span data-stu-id="52685-343">20</span></span>  

<span data-ttu-id="52685-344">Dieser Parameter ist der Schwellenwert, den die Datenbank-Engine zum Steuern der Fragmentierung des freien Speicherplatzes verwendet.</span><span class="sxs-lookup"><span data-stu-id="52685-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="52685-345">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="52685-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-346">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-347">8</span><span class="sxs-lookup"><span data-stu-id="52685-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-348">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-349">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-350">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-351">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="52685-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-352">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-353">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-354">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-355">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-356">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-357">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-358">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-359">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-360">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-361">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-362">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-363">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-364">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-365">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-366">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-367">Alle</span><span class="sxs-lookup"><span data-stu-id="52685-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="52685-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="52685-369">78</span><span class="sxs-lookup"><span data-stu-id="52685-369">78</span></span>

<span data-ttu-id="52685-370">Mit diesem Parameter wird gesteuert, wie aggressiv der Cache-Manager für die Datenbankseite eine Datenbankseite schreibt, bei der eine direkte Formatkonvertierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="52685-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="52685-371">Diese Formatkonvertierungen erfolgen im laufenden Betrieb, wenn Seiten aus einer Datenbank geladen werden, die mit dem Windows 2000-Datenbankmodul erstellt, aber von einer Windows XP-Version oder einer neueren Version der Datenbank-Engine verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="52685-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-372">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-373">1</span><span class="sxs-lookup"><span data-stu-id="52685-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-374">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-375">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-376">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-377">0-3</span><span class="sxs-lookup"><span data-stu-id="52685-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-378">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-379">Global</span><span class="sxs-lookup"><span data-stu-id="52685-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-380">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-381">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-382">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-383">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-384">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-385">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-386">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-387">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-388">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-389">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-390">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-391">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-392">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-393">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="52685-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="52685-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="52685-395">153</span><span class="sxs-lookup"><span data-stu-id="52685-395">153</span></span>  

<span data-ttu-id="52685-396">Die Wartezeit (in Protokollen) hinter dem Tip/Most-Commit-Protokoll, um Datenbankseiten Leerungen abzuschieben.</span><span class="sxs-lookup"><span data-stu-id="52685-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="52685-397">Wenn Sie diese Wartezeit aktivieren, kann die Daten Bank Wiederherstellung bei einem schwerwiegenden Verlust der aktuellen Protokolldatei möglich sein.</span><span class="sxs-lookup"><span data-stu-id="52685-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="52685-398">Siehe JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="52685-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-399">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-400">0</span><span class="sxs-lookup"><span data-stu-id="52685-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-401">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-402">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-403">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="52685-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-405">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-406">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-407">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-408">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-409">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-410">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-411">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-412">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-413">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-414">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-415">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-416">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-417">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-418">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-419">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52685-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="52685-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="52685-422">160</span><span class="sxs-lookup"><span data-stu-id="52685-422">160</span></span>  

<span data-ttu-id="52685-423">Aktivieren/Deaktivieren Sie die automatische sequenzielle B-Struktur-Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="52685-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-424">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-425">1</span><span class="sxs-lookup"><span data-stu-id="52685-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-426">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="52685-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-428">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-429">0-1</span><span class="sxs-lookup"><span data-stu-id="52685-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-430">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-431">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-432">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-433">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-434">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-435">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-436">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-437">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-438">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-439">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-440">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-441">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-442">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-443">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-444">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52685-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="52685-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="52685-447">161</span><span class="sxs-lookup"><span data-stu-id="52685-447">161</span></span>  

<span data-ttu-id="52685-448">Bestimmt, wie oft die B-Struktur Dichte überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="52685-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-449">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-450">10</span><span class="sxs-lookup"><span data-stu-id="52685-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-451">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-452">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-453">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-454">0-maximale Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="52685-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-455">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-456">Instanz</span><span class="sxs-lookup"><span data-stu-id="52685-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-457">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-458">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-459">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-460">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-461">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-462">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-463">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-464">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-465">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-466">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-467">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-468">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-469">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52685-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52685-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="52685-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="52685-472">162</span><span class="sxs-lookup"><span data-stu-id="52685-472">162</span></span>  

<span data-ttu-id="52685-473">Maximale Zeit in Millisekunden, die der e/a-einschränstungs Mechanismus eine auszuwertende Aufgabe angibt, damit Sie als "abgeschlossen" angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="52685-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-474">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="52685-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="52685-475">125</span><span class="sxs-lookup"><span data-stu-id="52685-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-476">Typ:</span><span class="sxs-lookup"><span data-stu-id="52685-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="52685-477">Integer</span><span class="sxs-lookup"><span data-stu-id="52685-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-478">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="52685-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="52685-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="52685-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-480">Umfang:</span><span class="sxs-lookup"><span data-stu-id="52685-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="52685-481">Global</span><span class="sxs-lookup"><span data-stu-id="52685-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-482">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-483">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-484">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="52685-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="52685-485">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-486">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="52685-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="52685-487">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-488">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="52685-489">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-490">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="52685-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="52685-491">Ja</span><span class="sxs-lookup"><span data-stu-id="52685-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-492">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52685-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="52685-493">Nein</span><span class="sxs-lookup"><span data-stu-id="52685-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-494">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="52685-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="52685-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52685-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="52685-496">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52685-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52685-497"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="52685-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52685-498">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="52685-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52685-499"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="52685-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52685-500">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="52685-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52685-501"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="52685-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52685-502">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="52685-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="52685-503">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52685-503">See Also</span></span>

[<span data-ttu-id="52685-504">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="52685-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="52685-505">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="52685-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="52685-506">Jetdebug</span><span class="sxs-lookup"><span data-stu-id="52685-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="52685-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="52685-507">JetInit</span></span>](./jetinit-function.md)
