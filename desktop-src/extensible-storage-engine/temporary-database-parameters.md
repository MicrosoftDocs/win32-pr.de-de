---
description: 'Weitere Informationen finden Sie hier: temporäre Daten Bank Parameter'
title: Temporäre Daten Bank Parameter
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217848"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="0ecfd-103">Temporäre Daten Bank Parameter</span><span class="sxs-lookup"><span data-stu-id="0ecfd-103">Temporary Database Parameters</span></span>


<span data-ttu-id="0ecfd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0ecfd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="0ecfd-105">Temporäre Daten Bank Parameter</span><span class="sxs-lookup"><span data-stu-id="0ecfd-105">Temporary Database Parameters</span></span>

<span data-ttu-id="0ecfd-106">Dieses Thema enthält Parameter, die für die temporäre Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="0ecfd-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="0ecfd-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="0ecfd-108">46</span><span class="sxs-lookup"><span data-stu-id="0ecfd-108">46</span></span>  

<span data-ttu-id="0ecfd-109">Dieser Parameter steuert die Verwendung von Transaktionen in temporären Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="0ecfd-110">Wenn dieser Parameter den Wert false hat, sind temporäre Tabellen schneller, aber es ist nicht möglich, ein Rollback für Updates durchzuführen, die in einer Transaktion durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-111">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-112">Richtig</span><span class="sxs-lookup"><span data-stu-id="0ecfd-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="0ecfd-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-115">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-116">False, True</span><span class="sxs-lookup"><span data-stu-id="0ecfd-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-117">Umfang:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-118">Instanz</span><span class="sxs-lookup"><span data-stu-id="0ecfd-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-119">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-120">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-121">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-122">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-123">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-124">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-125">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-126">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-127">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-128">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-129">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-130">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-131">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-132">Alle</span><span class="sxs-lookup"><span data-stu-id="0ecfd-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ecfd-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="0ecfd-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="0ecfd-134">19</span><span class="sxs-lookup"><span data-stu-id="0ecfd-134">19</span></span>  

<span data-ttu-id="0ecfd-135">Dieser Parameter steuert die anfängliche Größe der temporären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="0ecfd-136">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-136">The size is in database pages.</span></span> <span data-ttu-id="0ecfd-137">Eine Größe von NULL gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="0ecfd-138">Häufig ist es wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="0ecfd-139">Wenn Sie diesen Parameter auf 14 festlegen, wird die kleinste temporäre Datenbank erreicht.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="0ecfd-140">Beachten Sie, dass Sie die temporäre Datenbank auch vollständig ausschließen können, indem Sie **JET_paramMaxTemporaryTables** auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-141">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-142">0</span><span class="sxs-lookup"><span data-stu-id="0ecfd-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-143">Typ:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-144">Integer</span><span class="sxs-lookup"><span data-stu-id="0ecfd-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-145">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-146">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="0ecfd-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-147">Umfang:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-148">Instanz</span><span class="sxs-lookup"><span data-stu-id="0ecfd-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-149">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-150">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-151">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-152">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-153">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-154">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-155">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-156">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-157">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-158">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-159">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-160">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-161">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-162">Alle</span><span class="sxs-lookup"><span data-stu-id="0ecfd-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ecfd-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="0ecfd-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="0ecfd-164">1</span><span class="sxs-lookup"><span data-stu-id="0ecfd-164">1</span></span>  

<span data-ttu-id="0ecfd-165">Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners oder der Datei an, der bzw. die die temporäre Datenbank für die Instanz enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="0ecfd-166">Wenn der Pfad zu einem Ordner gehört, der die temporäre Datenbank enthalten soll, muss er mit einem umgekehrten Schrägstrich beendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="0ecfd-167">Die temporäre Datenbank wird verwendet, um flüchtige Daten aufzunehmen, die bei der Verarbeitung von ESE-API-Informations aufrufen, beim Erstellen von Indizes oder beim Speichern des Inhalts einer temporären Tabelle generiert werden.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="0ecfd-168">**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-169">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-170">&quot;tmp. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="0ecfd-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-171">Typ:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-172">Path (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="0ecfd-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-173">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-174">0 – 247 Zeichen</span><span class="sxs-lookup"><span data-stu-id="0ecfd-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-175">Umfang:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-176">Instanz</span><span class="sxs-lookup"><span data-stu-id="0ecfd-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-177">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-178">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-179">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-180">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-181">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-182">Ja</span><span class="sxs-lookup"><span data-stu-id="0ecfd-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-183">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-184">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-185">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-186">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-187">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-188">Nein</span><span class="sxs-lookup"><span data-stu-id="0ecfd-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-189">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="0ecfd-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0ecfd-190">Alle</span><span class="sxs-lookup"><span data-stu-id="0ecfd-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="0ecfd-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ecfd-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0ecfd-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0ecfd-193">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ecfd-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0ecfd-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0ecfd-195">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ecfd-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0ecfd-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0ecfd-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0ecfd-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0ecfd-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ecfd-198">See Also</span></span>

[<span data-ttu-id="0ecfd-199">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="0ecfd-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0ecfd-200">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="0ecfd-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0ecfd-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="0ecfd-201">JetInit</span></span>](./jetinit-function.md)
