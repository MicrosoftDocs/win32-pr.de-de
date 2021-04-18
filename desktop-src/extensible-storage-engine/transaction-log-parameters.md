---
description: Weitere Informationen finden Sie im Artikel zu Transaktionsprotokoll Parametern.
title: Transaktionsprotokollparameters
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347526"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="ef03e-103">Transaktionsprotokollparameters</span><span class="sxs-lookup"><span data-stu-id="ef03e-103">Transaction Log Parameters</span></span>


<span data-ttu-id="ef03e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef03e-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="ef03e-105">**Inhalt dieses Artikels:**</span><span class="sxs-lookup"><span data-stu-id="ef03e-105">**In this article**</span></span>  
<span data-ttu-id="ef03e-106">Transaktionsprotokollparameters</span><span class="sxs-lookup"><span data-stu-id="ef03e-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="ef03e-107">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ef03e-107">Requirements</span></span>  
<span data-ttu-id="ef03e-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef03e-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="ef03e-109">Transaktionsprotokollparameters</span><span class="sxs-lookup"><span data-stu-id="ef03e-109">Transaction Log Parameters</span></span>

<span data-ttu-id="ef03e-110">Dieses Thema enthält Parameter, die für Transaktionsprotokolle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="ef03e-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="ef03e-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="ef03e-112">3</span><span class="sxs-lookup"><span data-stu-id="ef03e-112">3</span></span>  

<span data-ttu-id="ef03e-113">Mit diesem Parameter wird das drei Buchstabe festgelegt, das für viele der von der Datenbank-Engine verwendeten Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="ef03e-114">Beispielsweise wird die Prüf Punkt Datei als EDB bezeichnet. Standardmäßig chk, da EDB der Standardbasis Name ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="ef03e-115">Der Basisname kann verwendet werden, um problemlos zwischen Gruppen von Dateien zu unterscheiden, die zu unterschiedlichen Instanzen oder anderen Anwendungen gehören.</span><span class="sxs-lookup"><span data-stu-id="ef03e-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-116">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-117">&quot;EDB&quot;</span><span class="sxs-lookup"><span data-stu-id="ef03e-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-118">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-119">String</span><span class="sxs-lookup"><span data-stu-id="ef03e-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-120">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-121">3 Zeichen</span><span class="sxs-lookup"><span data-stu-id="ef03e-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-122">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-123">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-124">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-125">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-126">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-127">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-128">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-129">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-130">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-131">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-132">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-133">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-134">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-135">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-136">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-137">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="ef03e-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="ef03e-139">17</span><span class="sxs-lookup"><span data-stu-id="ef03e-139">17</span></span>  

<span data-ttu-id="ef03e-140">Mit diesem Parameter wird konfiguriert, wie Transaktionsprotokoll Dateien von der Datenbank-Engine verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="ef03e-141">Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokoll Dateien auf dem Datenträger gespeichert, bis Sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef03e-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="ef03e-142">In diesem Modus ist es möglich, eine Wiederherstellung aus einer älteren Sicherung durchzuführen und alle beibehaltenen Transaktionsprotokoll Dateien durchzuführen, sodass keine Daten verloren gehen, weil der Notfall die Wiederherstellung erzwungen hat.</span><span class="sxs-lookup"><span data-stu-id="ef03e-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="ef03e-143">Reguläre vollständige Sicherungen sind erforderlich, um zu verhindern, dass der Datenträger die Transaktionsprotokoll Dateien füllt.</span><span class="sxs-lookup"><span data-stu-id="ef03e-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="ef03e-144">Wenn die zirkuläre Protokollierung auf on festgehalten wird, werden nur Transaktionsprotokoll Dateien auf dem Datenträger beibehalten</span><span class="sxs-lookup"><span data-stu-id="ef03e-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="ef03e-145">Der Vorteil dieses Modus besteht darin, dass keine Sicherungen erforderlich sind, um alte Transaktionsprotokoll Dateien abzukoppeln.</span><span class="sxs-lookup"><span data-stu-id="ef03e-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="ef03e-146">Der Kompromiss besteht darin, dass eine Wiederherstellung ohne Datenverlust nicht mehr möglich ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-147">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-148">False</span><span class="sxs-lookup"><span data-stu-id="ef03e-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-149">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="ef03e-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-151">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-152">False, True</span><span class="sxs-lookup"><span data-stu-id="ef03e-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-153">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-154">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-155">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-156">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-157">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-158">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-159">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-160">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-161">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-162">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-163">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-164">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-165">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-166">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-167">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-168">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="ef03e-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="ef03e-170">16</span><span class="sxs-lookup"><span data-stu-id="ef03e-170">16</span></span>  

<span data-ttu-id="ef03e-171">Dieser Parameter steuert die Standardaktion, die ausgeführt wird, wenn für die äußere Transaktion ein Commit in einer Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="ef03e-172">Alle gültigen Optionen, die an [jetcommittransaction](./jetcommittransaction-function.md) übermittelt werden können, können auch als Standard für alle Sitzungen in einer Instanz und/oder für eine bestimmte Sitzung fest gegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="ef03e-173">Weitere Informationen zu diesen Optionen finden Sie unter [jetcommittransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ef03e-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="ef03e-174">Dieser Parameter wirkt sich auf die Zuverlässigkeit und Leistung von Transaktionen aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="ef03e-175">Weitere Informationen finden Sie unter [jetcommittransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ef03e-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-176">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-177">0</span><span class="sxs-lookup"><span data-stu-id="ef03e-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-178">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-179">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ef03e-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-180">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-181">Eine gültige Option für jetcommittransaction.</span><span class="sxs-lookup"><span data-stu-id="ef03e-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-182">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-183">Instanz oder Sitzung</span><span class="sxs-lookup"><span data-stu-id="ef03e-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-184">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-185">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-186">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-187">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-188">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-189">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-190">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-191">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-192">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-193">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-194">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-195">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-196">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-197">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="ef03e-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="ef03e-199">48</span><span class="sxs-lookup"><span data-stu-id="ef03e-199">48</span></span>  

<span data-ttu-id="ef03e-200">Wenn dieser Parameter den Wert true hat und die Transaktionsprotokoll Dateien, auf die der Pfad der Protokolldatei (**JET_paramLogFilePath**) verweist, eine veraltete Version aufweisen, werden diese Transaktionsprotokoll Dateien automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ef03e-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="ef03e-201">**Windows 2000:**  Beachten Sie beim Aktualisieren einer Datenbank von Windows NT auf Windows 2000 die Verwendung dieses Parameters.</span><span class="sxs-lookup"><span data-stu-id="ef03e-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="ef03e-202">Wenn sich die Datenbank nicht in einem konsistenten Zustand befindet und die alten Protokolldateien gelöscht werden, geht der Inhalt der Datenbank verloren.</span><span class="sxs-lookup"><span data-stu-id="ef03e-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-203">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-204"><strong>Windows 2000:</strong>  Alarm</span><span class="sxs-lookup"><span data-stu-id="ef03e-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="ef03e-205"><strong>Windows XP:</strong>  Fall</span><span class="sxs-lookup"><span data-stu-id="ef03e-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-206">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="ef03e-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-208">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-209">False, True</span><span class="sxs-lookup"><span data-stu-id="ef03e-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-210">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-211">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-212">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-213">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-214">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-215">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-216">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-217">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-218">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-219">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-220">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-221">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-222">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-223">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-224">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-225">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="ef03e-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="ef03e-227">47</span><span class="sxs-lookup"><span data-stu-id="ef03e-227">47</span></span>  

<span data-ttu-id="ef03e-228">Wenn dieser Parameter true ist, wird die Versionsnummer der Transaktionsprotokoll Datei von der Datenbank-Engine während [jetinit](./jetinit-function.md)nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="ef03e-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="ef03e-229">**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-230">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-231">False</span><span class="sxs-lookup"><span data-stu-id="ef03e-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-232">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="ef03e-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-234">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-235">False, True</span><span class="sxs-lookup"><span data-stu-id="ef03e-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-236">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-237">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-238">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-239">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-240">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-241">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-242">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-243">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-244">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-245">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-246">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-247">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-248">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-249">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-250">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-251">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="ef03e-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="ef03e-253">136</span><span class="sxs-lookup"><span data-stu-id="ef03e-253">136</span></span>  

<span data-ttu-id="ef03e-254">Dieser Parameter stellt Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine bereit.</span><span class="sxs-lookup"><span data-stu-id="ef03e-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="ef03e-255">Derzeit werden die folgenden Optionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ef03e-255">The following options are currently supported:</span></span>

<span data-ttu-id="ef03e-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ef03e-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="ef03e-257">Wenn diese Option vorhanden ist, verwendet die Datenbank-Engine die folgenden Benennungs Konventionen für die zugehörigen Dateien:</span><span class="sxs-lookup"><span data-stu-id="ef03e-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="ef03e-258">Transaktionsprotokoll Dateien werden verwenden. Protokolldatei Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ef03e-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="ef03e-259">Prüf Punkt Dateien verwenden. CHK für die Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="ef03e-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-260">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ef03e-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-262">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-263">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ef03e-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-264">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ef03e-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-266">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-267">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-268">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-269">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-270">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-271">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-272">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-273">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-274">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-275">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-276">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-277">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-278">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-279">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-280">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-281">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="ef03e-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="ef03e-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="ef03e-283">12</span><span class="sxs-lookup"><span data-stu-id="ef03e-283">12</span></span>  

<span data-ttu-id="ef03e-284">Mit diesem Parameter wird die Menge an Arbeitsspeicher konfiguriert, die zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="ef03e-285">Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="ef03e-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="ef03e-286">Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="ef03e-287">Dieser Parameter wirkt sich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="ef03e-288">Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="ef03e-289">Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung.</span><span class="sxs-lookup"><span data-stu-id="ef03e-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="ef03e-290">Der Standardwert ist für diesen Fall zu klein.</span><span class="sxs-lookup"><span data-stu-id="ef03e-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="ef03e-291">**Windows XP und Windows 2000:**  Unter Windows XP und früheren Versionen wird empfohlen, diesen Parameter nicht auf eine Anzahl von größeren Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-292">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-293"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  80</span><span class="sxs-lookup"><span data-stu-id="ef03e-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="ef03e-294"><strong>Windows Vista:</strong>  126</span><span class="sxs-lookup"><span data-stu-id="ef03e-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-295">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-296">Integer</span><span class="sxs-lookup"><span data-stu-id="ef03e-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-297">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-298"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ef03e-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="ef03e-299"><strong>Windows Vista:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ef03e-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-300">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-301">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-302">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-303">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-304">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-305">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-306">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-307">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-308">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-309">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-310">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-311">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-312">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-313">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-314">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-315">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="ef03e-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="ef03e-317">14</span><span class="sxs-lookup"><span data-stu-id="ef03e-317">14</span></span>  

<span data-ttu-id="ef03e-318">Mit diesem Parameter wird die Datenbank-Engine so konfiguriert, dass ein Prüfpunkt erstellt wird, wenn die angegebene Anzahl von Protokolldatei Sektoren generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef03e-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="ef03e-319">**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-320">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-321">1024</span><span class="sxs-lookup"><span data-stu-id="ef03e-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-322">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-323">Integer</span><span class="sxs-lookup"><span data-stu-id="ef03e-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-324">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-325">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ef03e-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-326">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-327">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-328">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-329">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-330">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-331">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-332">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-333">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-334">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-335">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-336">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-337">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-338">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-339">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-340">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-341">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="ef03e-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="ef03e-343">69</span><span class="sxs-lookup"><span data-stu-id="ef03e-343">69</span></span>  

<span data-ttu-id="ef03e-344">Wenn dieser Parameter auf true festgelegt ist, wird die nächste Transaktionsprotokoll Datei von der Datenbank-Engine erstellt, wenn die aktuelle Transaktionsprotokoll Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="ef03e-345">Die Absicht besteht darin, die Zeit zu verkürzen, die für den Wechsel von einer Transaktionsprotokoll Datei zur nächsten bei hoher Update Auslastung aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ef03e-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-346">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-347">Richtig</span><span class="sxs-lookup"><span data-stu-id="ef03e-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-348">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="ef03e-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-350">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-351">False, True</span><span class="sxs-lookup"><span data-stu-id="ef03e-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-352">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-353">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-354">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-355">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-356">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-357">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-358">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-359">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-360">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-361">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-362">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-363">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-364">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-365">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-366">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-367">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="ef03e-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="ef03e-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="ef03e-369">2</span><span class="sxs-lookup"><span data-stu-id="ef03e-369">2</span></span> 

<span data-ttu-id="ef03e-370">Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Transaktionsprotokolle für die Instanz enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="ef03e-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="ef03e-371">Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, was darauf hinweist, dass der Zielpfad ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="ef03e-372">Die Transaktionsprotokoll Dateien enthalten die Informationen, die erforderlich sind, um die Datenbankdateien nach einem Absturz in einen konsistenten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="ef03e-373">Sie werden normalerweise als EDB bezeichnet \* . Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef03e-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="ef03e-374">Der Inhalt der Transaktionsprotokoll Dateien ist ebenso wichtig (falls nicht mehr) als die Datenbankdateien selbst.</span><span class="sxs-lookup"><span data-stu-id="ef03e-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="ef03e-375">Jeder Versuch sollte durchgeführt werden, um Sie zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="ef03e-376">Es werden auch weitere Reservierungs Protokolldateien mit dem Namen "RES1" angezeigt. Log und RES2. Das Protokoll wird zusammen mit den normalen Protokolldateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef03e-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="ef03e-377">Der Inhalt dieser Dateien ist nicht wichtig, da nur der Speicherplatz reserviert werden muss, damit die Engine in einem Szenario mit geringem Datenträger ordnungsgemäß heruntergefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef03e-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="ef03e-378">Dabei handelt es sich auch um eine temporäre Protokolldatei mit dem Namen edbtmp. Melden Sie sich in demselben Ordner an.</span><span class="sxs-lookup"><span data-stu-id="ef03e-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="ef03e-379">Der Inhalt dieser Datei ist entweder nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="ef03e-379">The contents of this file are not important either.</span></span> <span data-ttu-id="ef03e-380">Bei dieser Datei handelt es sich um eine neue Protokolldatei, die zur Verwendung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="ef03e-381">Die Eigenschaften des Host Volumens der Transaktionsprotokoll Dateien und deren Platzierung in Relation zu den anderen Dateien, die von der Datenbank-Engine verwendet werden, können sich erheblich auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="ef03e-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="ef03e-382">**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef03e-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-383">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-384">&quot;.\& quot</span><span class="sxs-lookup"><span data-stu-id="ef03e-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-385">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-386">Ordner Pfad (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ef03e-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-387">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-388">0 – 246 Zeichen</span><span class="sxs-lookup"><span data-stu-id="ef03e-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-389">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-390">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-391">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-392">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-393">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-394">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-395">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-396">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-397">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-398">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-399">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-400">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-401">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-402">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-403">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-404">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="ef03e-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="ef03e-406">11</span><span class="sxs-lookup"><span data-stu-id="ef03e-406">11</span></span>  

<span data-ttu-id="ef03e-407">Mit diesem Parameter wird die Größe der Transaktionsprotokoll Dateien konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ef03e-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="ef03e-408">Jede Transaktionsprotokoll Datei hat eine Größe mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="ef03e-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="ef03e-409">Die Größe entspricht der Einstellung dieses System Parameters in Einheiten von 1024 Byte.</span><span class="sxs-lookup"><span data-stu-id="ef03e-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="ef03e-410">Dieser Parameter wirkt sich auf die Zuverlässigkeit aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="ef03e-411">Wenn die Einstellung zu klein ist, wird die maximale Anzahl von Protokolldateien (1048575) wesentlich schneller erreicht.</span><span class="sxs-lookup"><span data-stu-id="ef03e-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="ef03e-412">In diesem Fall muss die Instanz ordnungsgemäß heruntergefahren werden, die vorhandenen Protokolldateien müssen gelöscht werden, und die Instanz muss neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="ef03e-413">Durch diese Aktion wird nicht nur die Verfügbarkeit der Anwendung verringert, sondern auch alle vorherigen Sicherungen der Datenbank der Anwendung werden für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="ef03e-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="ef03e-414">Dieser Parameter wirkt sich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="ef03e-415">Wenn die Einstellung sehr groß ist, ist [jetinit](./jetinit-function.md) langsam, da die Datenbank-Engine die jüngste Protokolldatei (zumindest) lesen muss, wenn Sie initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="ef03e-416">Wenn die Einstellung sehr groß ist, dauert es auch länger, bis zwischen den Protokolldateien gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="ef03e-417">Wenn die Einstellung sehr klein ist, müssen für eine bestimmte Anzahl von Updates weitere Protokolldateien erstellt werden, die mehr Aufwand verursachen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-418">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-419">5120</span><span class="sxs-lookup"><span data-stu-id="ef03e-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-420">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-421">Integer</span><span class="sxs-lookup"><span data-stu-id="ef03e-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-422">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-423"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="ef03e-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="ef03e-424"><strong>Windows Vista:</strong>  64 – 32768</span><span class="sxs-lookup"><span data-stu-id="ef03e-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-425">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-426">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-427">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-428">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-429">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-430">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-431">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-432">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-433">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-434">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-435">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-436">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-437">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-438">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-439">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-440">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="ef03e-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="ef03e-442">15</span><span class="sxs-lookup"><span data-stu-id="ef03e-442">15</span></span>  

<span data-ttu-id="ef03e-443">Dieser Parameter versucht, die Leerung des Protokoll Puffers zu optimieren, der durch einen permanenten Commit verursacht wurde, indem auf eine angegebene Anzahl von Sitzungen gewartet wird, die auf einen permanenten Commit gewartet wird, bevor eine Leerung durchgeführt wird, um zu erzwingen, dass eine andere Transaktion den Löschvorgang gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef03e-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="ef03e-444">**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-445">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-446">3</span><span class="sxs-lookup"><span data-stu-id="ef03e-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-447">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-448">Integer</span><span class="sxs-lookup"><span data-stu-id="ef03e-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-449">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-450">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ef03e-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-451">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-452">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-453">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-454">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-455">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-456">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-457">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-458">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-459">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-460">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-461">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-462">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-463">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-464">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-465">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-466">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="ef03e-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="ef03e-468">34</span><span class="sxs-lookup"><span data-stu-id="ef03e-468">34</span></span>  

<span data-ttu-id="ef03e-469">Dieser Parameter ist der Hauptschalter, der die Wiederherstellung von Abstürzen für eine-Instanz steuert.</span><span class="sxs-lookup"><span data-stu-id="ef03e-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="ef03e-470">Wenn dieser Parameter auf "on" festgelegt ist, wird die Wiederherstellung im Aries-Stil verwendet, um alle Datenbanken in der Instanz in einen konsistenten Zustand zu bringen, wenn ein Prozess oder ein Computerabsturz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="ef03e-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="ef03e-471">Wenn dieser Parameter auf "Off" festgelegt ist, werden alle Datenbanken in der Instanz ohne den Vorteil der Wiederherstellung von Abstürzen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ef03e-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="ef03e-472">Das heißt, wenn die Instanz nicht mit [jetterm](./jetterm-function.md) ordnungsgemäß heruntergefahren wird, bevor der Prozess beendet oder der Computer heruntergefahren wird, wird der Inhalt aller Datenbanken in dieser Instanz beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ef03e-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="ef03e-473">Die Deaktivierung der Wiederherstellung ist in besonderen Situationen nützlich, in denen bekannt ist, dass der Inhalt einer Datenbank im Falle eines Absturzes nicht nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="ef03e-474">Die Wiederherstellung sollte für alle anderen Fälle aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-475">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-476">&quot;On&quot;</span><span class="sxs-lookup"><span data-stu-id="ef03e-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-477">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-478">String</span><span class="sxs-lookup"><span data-stu-id="ef03e-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-479">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-480">0 – 259 Zeichen</span><span class="sxs-lookup"><span data-stu-id="ef03e-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-481">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-482">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-483">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-484">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-485">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-486">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-487">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-488">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-489">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-490">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-491">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-492">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-493">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-494">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-495">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-496">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="ef03e-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="ef03e-498">0</span><span class="sxs-lookup"><span data-stu-id="ef03e-498">0</span></span>  

<span data-ttu-id="ef03e-499">Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Prüf Punkt Datei für die Instanz enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="ef03e-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="ef03e-500">Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, was darauf hinweist, dass der Zielpfad ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="ef03e-501">Die Prüf Punkt Datei ist eine einfache Datei, die pro Instanz verwaltet wird und die älteste Transaktionsprotokoll Datei speichert, die wiedergegeben werden muss, um alle Datenbanken in dieser Instanz nach einem Absturz in einen konsistenten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="ef03e-502">Die Prüf Punkt Datei wird in der Regel als EDB bezeichnet. CHK.</span><span class="sxs-lookup"><span data-stu-id="ef03e-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="ef03e-503">**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef03e-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-504">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-505">&quot;.\& quot</span><span class="sxs-lookup"><span data-stu-id="ef03e-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-506">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-507">Ordner Pfad (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="ef03e-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-508">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-509">0 – 246 Zeichen</span><span class="sxs-lookup"><span data-stu-id="ef03e-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-510">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-511">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-512">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-513">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-514">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-515">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-516">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-517">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-518">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-519">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-520">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-521">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-522">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-523">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-524">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-525">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="ef03e-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="ef03e-527">13</span><span class="sxs-lookup"><span data-stu-id="ef03e-527">13</span></span> 

<span data-ttu-id="ef03e-528">Dieser Parameter versucht, die Leerung des Protokoll Puffers zu optimieren, der durch einen permanenten Commit verursacht wurde, indem ein angegebener Zeitraum gewartet wird, bevor eine Leerung in der Hoffnung ausgelöst wird, dass der Löschvorgang von einer anderen Transaktion gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="ef03e-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="ef03e-529">**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="ef03e-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-530">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-531">0</span><span class="sxs-lookup"><span data-stu-id="ef03e-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-532">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-533">Integer</span><span class="sxs-lookup"><span data-stu-id="ef03e-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-534">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-535">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ef03e-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-536">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-537">Instanz oder Sitzung</span><span class="sxs-lookup"><span data-stu-id="ef03e-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-538">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-539">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-540">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-541">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-542">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-543">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-544">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-545">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-546">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-547">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-548">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-549">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-550">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-551">Alle</span><span class="sxs-lookup"><span data-stu-id="ef03e-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef03e-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="ef03e-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="ef03e-553">136</span><span class="sxs-lookup"><span data-stu-id="ef03e-553">136</span></span>  

<span data-ttu-id="ef03e-554">Dieser Parameter wird verwendet, um die Dateinamen Kompatibilitäts Features anzugeben, die mit Windows Server 2003 und dem vorherigen Datei Benennungs Schema verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef03e-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="ef03e-555">Weitere Informationen zu den verschiedenen Dateien und deren Benennung finden Sie unter [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span><span class="sxs-lookup"><span data-stu-id="ef03e-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="ef03e-556">Der JET_bitESE98FileNames stellt sicher, dass die Dateierweiterung, die für die Transaktionsprotokoll Dateien und die Prüf Punkt Datei verwendet wird, identisch mit der in Windows Server 2003 verwendeten Dateierweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="ef03e-557">Hinweis Wenn Sie ein Upgrade von Windows Server 2003 ausführen, muss dieses Bit noch nicht angegeben werden, da die Engine die Dateierweiterungen automatisch aktualisiert, wenn JET_paramCircularLog auf **true** festgelegt ist, oder die ältere Protokollerweiterung beibehalten, wenn JET_paramCircularLog **false** ist.</span><span class="sxs-lookup"><span data-stu-id="ef03e-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="ef03e-558">**Hinweis**  Wenn Sie ein Bit festlegen möchten, sollte der Wert zuerst abgerufen und anschließend im gewünschten Kompatibilitäts Bit "oder" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef03e-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-559">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="ef03e-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ef03e-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-561">Typ:</span><span class="sxs-lookup"><span data-stu-id="ef03e-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-562">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ef03e-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-563">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef03e-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ef03e-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-565">Umfang:</span><span class="sxs-lookup"><span data-stu-id="ef03e-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-566">Instanz</span><span class="sxs-lookup"><span data-stu-id="ef03e-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-567">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-568">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-569">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-570">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-571">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="ef03e-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-572">Ja</span><span class="sxs-lookup"><span data-stu-id="ef03e-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-573">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-574">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-575">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="ef03e-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-576">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-577">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ef03e-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-578">Nein</span><span class="sxs-lookup"><span data-stu-id="ef03e-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-579">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="ef03e-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ef03e-580">Ab Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef03e-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="ef03e-581">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef03e-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-582"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ef03e-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef03e-583">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef03e-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef03e-584"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef03e-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef03e-585">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef03e-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef03e-586"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ef03e-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef03e-587">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ef03e-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ef03e-588">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef03e-588">See Also</span></span>

[<span data-ttu-id="ef03e-589">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="ef03e-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="ef03e-590">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="ef03e-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="ef03e-591">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="ef03e-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="ef03e-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="ef03e-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ef03e-593">Jetterm</span><span class="sxs-lookup"><span data-stu-id="ef03e-593">JetTerm</span></span>](./jetterm-function.md)
