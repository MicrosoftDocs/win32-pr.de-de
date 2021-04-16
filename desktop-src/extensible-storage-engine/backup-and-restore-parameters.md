---
description: Weitere Informationen zu Sicherungs-und Wiederherstellungs Parametern
title: Sicherungs-und Wiederherstellungs Parameter
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530116"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="ec0f5-103">Sicherungs-und Wiederherstellungs Parameter</span><span class="sxs-lookup"><span data-stu-id="ec0f5-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="ec0f5-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec0f5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="ec0f5-105">Sicherungs-und Wiederherstellungs Parameter</span><span class="sxs-lookup"><span data-stu-id="ec0f5-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="ec0f5-106">Dieses Thema enthält Parameter, die für die Sicherung und Wiederherstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="ec0f5-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="ec0f5-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="ec0f5-108">113</span><span class="sxs-lookup"><span data-stu-id="ec0f5-108">113</span></span>  

<span data-ttu-id="ec0f5-109">Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktions Protokollen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="ec0f5-110">Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktions Wiedergabe ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="ec0f5-111">Dieser Parameter kann verwendet werden, um die Wiederherstellung von abstürzen oder einen Wiederherstellungs Vorgang zum Suchen nach den Datenbanken zu erzwingen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-112">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-114">Ordner Pfad (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ec0f5-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-115">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-116">0 – 246 Zeichen</span><span class="sxs-lookup"><span data-stu-id="ec0f5-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-117">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-118">Instanz</span><span class="sxs-lookup"><span data-stu-id="ec0f5-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-119">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-120">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-121">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-122">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-123">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-124">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-125">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-126">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-127">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-128">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-129">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-130">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-131">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-132">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="ec0f5-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec0f5-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="ec0f5-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="ec0f5-134">77</span><span class="sxs-lookup"><span data-stu-id="ec0f5-134">77</span></span>  

<span data-ttu-id="ec0f5-135">Dieser Parameter steuert das Ergebnis von [jetinit](./jetinit-function.md) , wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte haben.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="ec0f5-136">Normalerweise stellt [jetinit](./jetinit-function.md) die Datenbanken erfolgreich wieder her, schlägt jedoch mit JET_errLogFileSizeMismatchDatabasesConsistent fehl, um anzugeben, dass die Größe der Protokolldatei falsch konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="ec0f5-137">Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien, startet einen neuen Satz von Transaktionsprotokoll Dateien mit der konfigurierten Protokolldatei Größe und gibt JET_errSuccess zurück.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="ec0f5-138">Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-139">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-140">False</span><span class="sxs-lookup"><span data-stu-id="ec0f5-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-141">Typ:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="ec0f5-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-143">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-144">False, True</span><span class="sxs-lookup"><span data-stu-id="ec0f5-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-145">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-146">Instanz</span><span class="sxs-lookup"><span data-stu-id="ec0f5-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-147">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-148">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-149">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-150">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-151">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-152">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-153">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-154">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-155">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-156">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-157">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-158">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-159">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-160">Alle</span><span class="sxs-lookup"><span data-stu-id="ec0f5-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec0f5-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="ec0f5-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="ec0f5-162">52</span><span class="sxs-lookup"><span data-stu-id="ec0f5-162">52</span></span>  

<span data-ttu-id="ec0f5-163">Wenn dieser Parameter true ist, werden alle auf dem Datenträger gefundenen Transaktionsprotokoll Dateien, die nicht Teil der aktuellen Sequenz von Protokolldateien sind, von [jetinit](./jetinit-function.md)gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="ec0f5-164">Dies kann verwendet werden, um überflüssige Protokolldateien nach einem Wiederherstellungs Vorgang automatisch zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="ec0f5-165">**Windows XP:**  Eingeführt in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-166">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-167">False</span><span class="sxs-lookup"><span data-stu-id="ec0f5-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-168">Typ:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="ec0f5-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-170">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-171">False, True</span><span class="sxs-lookup"><span data-stu-id="ec0f5-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-172">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-173">Instanz</span><span class="sxs-lookup"><span data-stu-id="ec0f5-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-174">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-175">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-176">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-177">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-178">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-179">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-180">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-181">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-182">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-183">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-184">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-185">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-186">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-187">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="ec0f5-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec0f5-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="ec0f5-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="ec0f5-189">82</span><span class="sxs-lookup"><span data-stu-id="ec0f5-189">82</span></span>  

<span data-ttu-id="ec0f5-190">Dieser Parameter konfiguriert den Zeitraum, der zwischen einem Aufruf von [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) und [jedessnapshotthaw](./jetossnapshotthaw-function.md) zulässig ist, bevor ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="ec0f5-191">Weitere Informationen finden Sie unter [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) und [jedessnapshotthaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0f5-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="ec0f5-192">Das Timeout ist in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-193">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-194">20000 (Windows XP und Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="ec0f5-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="ec0f5-195">70000 (Windows Server 2003 SP1)</span><span class="sxs-lookup"><span data-stu-id="ec0f5-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-196">Typ:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-197">Integer</span><span class="sxs-lookup"><span data-stu-id="ec0f5-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-198">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-199">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ec0f5-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-200">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-201">Global</span><span class="sxs-lookup"><span data-stu-id="ec0f5-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-202">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-203">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-204">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-205">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-206">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-207">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-208">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-209">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-210">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-211">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-212">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-213">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-214">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-215">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="ec0f5-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec0f5-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="ec0f5-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="ec0f5-217">71</span><span class="sxs-lookup"><span data-stu-id="ec0f5-217">71</span></span>  

<span data-ttu-id="ec0f5-218">Wenn dieser Parameter true ist, wird für jede Seite in einer Datenbank, die eine Streamingsicherung durchläuft, die gelöschte Daten bereinigt.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="ec0f5-219">Es ist wichtig zu beachten, dass sich die Datenbankseiten, die bereinigt werden, auf der Festplatte befinden.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="ec0f5-220">Das vollständige DataSet wird vor dem Bereinigungs Prozess gesichert.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-221">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-222">False</span><span class="sxs-lookup"><span data-stu-id="ec0f5-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-223">Typ:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="ec0f5-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-225">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-226">False, True</span><span class="sxs-lookup"><span data-stu-id="ec0f5-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-227">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-228">Instanz</span><span class="sxs-lookup"><span data-stu-id="ec0f5-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-229">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-230">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-231">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-232">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-233">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-234">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-235">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-236">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-237">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-238">Ja</span><span class="sxs-lookup"><span data-stu-id="ec0f5-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-239">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-240">Nein</span><span class="sxs-lookup"><span data-stu-id="ec0f5-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-241">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ec0f5-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ec0f5-242">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="ec0f5-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="ec0f5-243">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec0f5-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-244"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec0f5-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec0f5-245">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec0f5-246"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec0f5-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec0f5-247">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec0f5-248"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ec0f5-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec0f5-249">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ec0f5-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ec0f5-250">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec0f5-250">See Also</span></span>

[<span data-ttu-id="ec0f5-251">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="ec0f5-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="ec0f5-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="ec0f5-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ec0f5-253">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="ec0f5-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="ec0f5-254">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="ec0f5-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
