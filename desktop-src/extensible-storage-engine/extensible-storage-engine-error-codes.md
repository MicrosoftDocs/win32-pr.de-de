---
description: Weitere Informationen finden Sie in den Fehler Codes der Extensible Storage Engine.
title: Fehler Codes für erweiterbare Speicher-Engine
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360796"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="1833d-103">Fehler Codes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="1833d-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="1833d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1833d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="1833d-105">Fehler Codes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="1833d-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="1833d-106">Die folgenden Fehlercodes (Flags) werden von Funktionen in der Extensible Storage Engine-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="1833d-107">Ein [JET_ERR](./jet-err.md) Wert von 0 (null) sollte als Erfolg interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1833d-108">Erfolg</span><span class="sxs-lookup"><span data-stu-id="1833d-108">Success</span></span></p></th>
<th><p><span data-ttu-id="1833d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1833d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1833d-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="1833d-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="1833d-111">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1833d-112">Ein [JET_ERR](./jet-err.md) Wert, der größer als 0 (null) ist, sollte als Warnung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1833d-113">Warnungen</span><span class="sxs-lookup"><span data-stu-id="1833d-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="1833d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1833d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1833d-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="1833d-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="1833d-116">321</span><span class="sxs-lookup"><span data-stu-id="1833d-116">321</span></span></p></td>
<td><p><span data-ttu-id="1833d-117">Der Versionsspeicher ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="1833d-117">The version store is still active.</span></span> <span data-ttu-id="1833d-118">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="1833d-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="1833d-120">345</span><span class="sxs-lookup"><span data-stu-id="1833d-120">345</span></span></p></td>
<td><p><span data-ttu-id="1833d-121">Eine Suche nach einem nicht eindeutigen Index ergab einen eindeutigen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1833d-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="1833d-122">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="1833d-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="1833d-124">406</span><span class="sxs-lookup"><span data-stu-id="1833d-124">406</span></span></p></td>
<td><p><span data-ttu-id="1833d-125">Eine Daten Bank Spalte ist ein getrennter Long-Wert.</span><span class="sxs-lookup"><span data-stu-id="1833d-125">A database column is a separated long value.</span></span> <span data-ttu-id="1833d-126">Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="1833d-128">558</span><span class="sxs-lookup"><span data-stu-id="1833d-128">558</span></span></p></td>
<td><p><span data-ttu-id="1833d-129">Die vorhandene Protokolldatei hat eine ungültige Signatur.</span><span class="sxs-lookup"><span data-stu-id="1833d-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="1833d-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="1833d-131">559</span><span class="sxs-lookup"><span data-stu-id="1833d-131">559</span></span></p></td>
<td><p><span data-ttu-id="1833d-132">Die vorhandene Protokolldatei ist nicht zusammenhängend.</span><span class="sxs-lookup"><span data-stu-id="1833d-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="1833d-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="1833d-134">564</span><span class="sxs-lookup"><span data-stu-id="1833d-134">564</span></span></p></td>
<td><p><span data-ttu-id="1833d-135">Dieser Fehler ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1833d-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="1833d-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="1833d-137">578</span><span class="sxs-lookup"><span data-stu-id="1833d-137">578</span></span></p></td>
<td><p><span data-ttu-id="1833d-138">Die für die Wiederherstellung angegebene TargetInstance wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="1833d-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="1833d-140">595</span><span class="sxs-lookup"><span data-stu-id="1833d-140">595</span></span></p></td>
<td><p><span data-ttu-id="1833d-141">Die Daten Bank Beschädigung wurde repariert.</span><span class="sxs-lookup"><span data-stu-id="1833d-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="1833d-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="1833d-143">1004</span><span class="sxs-lookup"><span data-stu-id="1833d-143">1004</span></span></p></td>
<td><p><span data-ttu-id="1833d-144">Die Spalte weist einen <strong>null</strong> -Wert auf.</span><span class="sxs-lookup"><span data-stu-id="1833d-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="1833d-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="1833d-146">1006</span><span class="sxs-lookup"><span data-stu-id="1833d-146">1006</span></span></p></td>
<td><p><span data-ttu-id="1833d-147">Der Puffer ist zu klein für die Daten.</span><span class="sxs-lookup"><span data-stu-id="1833d-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="1833d-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="1833d-149">1007</span><span class="sxs-lookup"><span data-stu-id="1833d-149">1007</span></span></p></td>
<td><p><span data-ttu-id="1833d-150">Die Datenbank ist bereits angefügt.</span><span class="sxs-lookup"><span data-stu-id="1833d-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="1833d-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="1833d-152">1009</span><span class="sxs-lookup"><span data-stu-id="1833d-152">1009</span></span></p></td>
<td><p><span data-ttu-id="1833d-153">Die Sortierung, die versucht wird, verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1833d-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="1833d-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="1833d-155">1039</span><span class="sxs-lookup"><span data-stu-id="1833d-155">1039</span></span></p></td>
<td><p><span data-ttu-id="1833d-156">Bei einer Suche wurde eine genaue Entsprechung nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="1833d-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="1833d-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="1833d-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="1833d-159">Bei einer Suche wurde eine genaue Entsprechung nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="1833d-160">Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="1833d-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="1833d-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="1833d-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="1833d-163">Bei einer Suche wurde eine genaue Entsprechung nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="1833d-164">Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1833d-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="1833d-166">1.055</span><span class="sxs-lookup"><span data-stu-id="1833d-166">1055</span></span></p></td>
<td><p><span data-ttu-id="1833d-167">Es sind keine erweiterten Fehlerinformationen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="1833d-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="1833d-169">1058</span><span class="sxs-lookup"><span data-stu-id="1833d-169">1058</span></span></p></td>
<td><p><span data-ttu-id="1833d-170">Es ist keine Aktivität im Leerlauf aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="1833d-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="1833d-172">1067</span><span class="sxs-lookup"><span data-stu-id="1833d-172">1067</span></span></p></td>
<td><p><span data-ttu-id="1833d-173">Es ist keine Schreibsperre auf Transaktionsebene 0 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="1833d-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="1833d-175">1068</span><span class="sxs-lookup"><span data-stu-id="1833d-175">1068</span></span></p></td>
<td><p><span data-ttu-id="1833d-176">Die Spalte wird auf einen <strong>null</strong> -Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="1833d-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="1833d-178">1301</span><span class="sxs-lookup"><span data-stu-id="1833d-178">1301</span></span></p></td>
<td><p><span data-ttu-id="1833d-179">Eine leere Tabelle wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1833d-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="1833d-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="1833d-181">1327</span><span class="sxs-lookup"><span data-stu-id="1833d-181">1327</span></span></p></td>
<td><p><span data-ttu-id="1833d-182">Für die System Bereinigung ist ein Cursor in der Tabelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1833d-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="1833d-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="1833d-184">1415</span><span class="sxs-lookup"><span data-stu-id="1833d-184">1415</span></span></p></td>
<td><p><span data-ttu-id="1833d-185">Der veraltete Index muss entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="1833d-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="1833d-187">1512</span><span class="sxs-lookup"><span data-stu-id="1833d-187">1512</span></span></p></td>
<td><p><span data-ttu-id="1833d-188">Die maximale Länge ist zu groß und wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="1833d-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="1833d-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="1833d-190">1520</span><span class="sxs-lookup"><span data-stu-id="1833d-190">1520</span></span></p></td>
<td><p><span data-ttu-id="1833d-191">Ein BLOB-Wert wurde aus dem Datensatz in einen separaten Speicher großer BLOBs verschoben.</span><span class="sxs-lookup"><span data-stu-id="1833d-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="1833d-192"><strong>Hinweis</strong> Dieser Fehler ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1833d-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="1833d-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="1833d-194">1531</span><span class="sxs-lookup"><span data-stu-id="1833d-194">1531</span></span></p></td>
<td><p><span data-ttu-id="1833d-195">Die Spaltenwerte wurden nicht zurückgegeben, weil die entsprechende Spalten-ID oder das <em>itagsequence</em> -Element aus der <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> Struktur, die für die Enumeration angefordert wurde, NULL war.</span><span class="sxs-lookup"><span data-stu-id="1833d-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="1833d-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="1833d-197">1532</span><span class="sxs-lookup"><span data-stu-id="1833d-197">1532</span></span></p></td>
<td><p><span data-ttu-id="1833d-198">Die Spaltenwerte wurden nicht zurückgegeben, da Sie nicht aus den vorhandenen Daten rekonstruiert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="1833d-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="1833d-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="1833d-200">1533</span><span class="sxs-lookup"><span data-stu-id="1833d-200">1533</span></span></p></td>
<td><p><span data-ttu-id="1833d-201">Die vorhandenen Spaltenwerte wurden nicht für die Enumeration angefordert.</span><span class="sxs-lookup"><span data-stu-id="1833d-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="1833d-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="1833d-203">1534</span><span class="sxs-lookup"><span data-stu-id="1833d-203">1534</span></span></p></td>
<td><p><span data-ttu-id="1833d-204">Der Spaltenwert wurde bei der Enumeration an der angeforderten Größenbeschränkung abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="1833d-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="1833d-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="1833d-206">1535</span><span class="sxs-lookup"><span data-stu-id="1833d-206">1535</span></span></p></td>
<td><p><span data-ttu-id="1833d-207">Die Spaltenwerte sind vorhanden, wurden jedoch nicht von der Anforderung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="1833d-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="1833d-209">1536</span><span class="sxs-lookup"><span data-stu-id="1833d-209">1536</span></span></p></td>
<td><p><span data-ttu-id="1833d-210">Der Spaltenwert wurde in JET_COLUMNENUM zurückgegeben, weil der JET_bitEnumerateCompressOutput festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="1833d-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="1833d-212">1537</span><span class="sxs-lookup"><span data-stu-id="1833d-212">1537</span></span></p></td>
<td><p><span data-ttu-id="1833d-213">Der Spaltenwert wird auf den Standardwert der Spalte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="1833d-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="1833d-215">1610</span><span class="sxs-lookup"><span data-stu-id="1833d-215">1610</span></span></p></td>
<td><p><span data-ttu-id="1833d-216">Die Daten wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="1833d-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="1833d-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="1833d-218">1618</span><span class="sxs-lookup"><span data-stu-id="1833d-218">1618</span></span></p></td>
<td><p><span data-ttu-id="1833d-219">Es wird ein neuer Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="1833d-221">1813</span><span class="sxs-lookup"><span data-stu-id="1833d-221">1813</span></span></p></td>
<td><p><span data-ttu-id="1833d-222">Die Datenbankdatei ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="1833d-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="1833d-224">1908</span><span class="sxs-lookup"><span data-stu-id="1833d-224">1908</span></span></p></td>
<td><p><span data-ttu-id="1833d-225">Die Registrierung im Leerlauf ist voll.</span><span class="sxs-lookup"><span data-stu-id="1833d-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="1833d-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="1833d-227">2000</span><span class="sxs-lookup"><span data-stu-id="1833d-227">2000</span></span></p></td>
<td><p><span data-ttu-id="1833d-228">Es wurde bereits eine Online Defragmentierung für die angegebene Datenbank ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="1833d-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="1833d-230">2001</span><span class="sxs-lookup"><span data-stu-id="1833d-230">2001</span></span></p></td>
<td><p><span data-ttu-id="1833d-231">Eine Online Defragmentierung wird nicht für die angegebene Datenbank ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="1833d-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="1833d-233">2100</span><span class="sxs-lookup"><span data-stu-id="1833d-233">2100</span></span></p></td>
<td><p><span data-ttu-id="1833d-234">Die Registrierung einer nicht vorhandenen Rückruffunktion wurde aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1833d-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1833d-235">Ein [JET_ERR](./jet-err.md) Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1833d-236">Errors</span><span class="sxs-lookup"><span data-stu-id="1833d-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="1833d-237">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1833d-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1833d-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="1833d-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="1833d-239">-1</span><span class="sxs-lookup"><span data-stu-id="1833d-239">-1</span></span></p></td>
<td><p><span data-ttu-id="1833d-240">Die Funktion ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="1833d-242">-100</span><span class="sxs-lookup"><span data-stu-id="1833d-242">-100</span></span></p></td>
<td><p><span data-ttu-id="1833d-243">Der Ressourcen Fehler Simulator ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1833d-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="1833d-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="1833d-245">-101</span><span class="sxs-lookup"><span data-stu-id="1833d-245">-101</span></span></p></td>
<td><p><span data-ttu-id="1833d-246">Der Ressourcen Fehler Simulator wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="1833d-247">JET_errFileClose</span></span><br />
<span data-ttu-id="1833d-248">-102</span><span class="sxs-lookup"><span data-stu-id="1833d-248">-102</span></span></p></td>
<td><p><span data-ttu-id="1833d-249">Die Datei konnte nicht geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="1833d-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="1833d-251">-103</span><span class="sxs-lookup"><span data-stu-id="1833d-251">-103</span></span></p></td>
<td><p><span data-ttu-id="1833d-252">Der Thread konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="1833d-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="1833d-254">-105</span><span class="sxs-lookup"><span data-stu-id="1833d-254">-105</span></span></p></td>
<td><p><span data-ttu-id="1833d-255">Das System ist aufgrund zu vieler IOS ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="1833d-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="1833d-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="1833d-257">-106</span><span class="sxs-lookup"><span data-stu-id="1833d-257">-106</span></span></p></td>
<td><p><span data-ttu-id="1833d-258">Die angeforderte asynchrone Aufgabe konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="1833d-259">JET_errInternalError</span></span><br />
<span data-ttu-id="1833d-260">-107</span><span class="sxs-lookup"><span data-stu-id="1833d-260">-107</span></span></p></td>
<td><p><span data-ttu-id="1833d-261">Es ist ein schwerwiegender interner Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="1833d-263">-255</span><span class="sxs-lookup"><span data-stu-id="1833d-263">-255</span></span></p></td>
<td><p><span data-ttu-id="1833d-264">Die Puffer Abhängigkeiten wurden nicht ordnungsgemäß festgelegt, und es ist ein Wiederherstellungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="1833d-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="1833d-266">-322</span><span class="sxs-lookup"><span data-stu-id="1833d-266">-322</span></span></p></td>
<td><p><span data-ttu-id="1833d-267">Die Version war bereits vorhanden, und es ist ein Wiederherstellungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="1833d-268">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="1833d-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="1833d-270">-323</span><span class="sxs-lookup"><span data-stu-id="1833d-270">-323</span></span></p></td>
<td><p><span data-ttu-id="1833d-271">Die Seiten Grenze wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-271">The page boundary has been reached.</span></span> <span data-ttu-id="1833d-272">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="1833d-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="1833d-274">-324</span><span class="sxs-lookup"><span data-stu-id="1833d-274">-324</span></span></p></td>
<td><p><span data-ttu-id="1833d-275">Die Schlüssel Grenze wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-275">The key boundary has been reached.</span></span> <span data-ttu-id="1833d-276">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="1833d-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="1833d-278">-327</span><span class="sxs-lookup"><span data-stu-id="1833d-278">-327</span></span></p></td>
<td><p><span data-ttu-id="1833d-279">Die Datenbank ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-279">The database is corrupt.</span></span> <span data-ttu-id="1833d-280">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="1833d-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="1833d-282">-328</span><span class="sxs-lookup"><span data-stu-id="1833d-282">-328</span></span></p></td>
<td><p><span data-ttu-id="1833d-283">Das Lesezeichen hat keine entsprechende Adresse in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1833d-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="1833d-284">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="1833d-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="1833d-286">-334</span><span class="sxs-lookup"><span data-stu-id="1833d-286">-334</span></span></p></td>
<td><p><span data-ttu-id="1833d-287">Fehler beim Abrufen des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="1833d-287">The call to the operating system failed.</span></span> <span data-ttu-id="1833d-288">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="1833d-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="1833d-290">-338</span><span class="sxs-lookup"><span data-stu-id="1833d-290">-338</span></span></p></td>
<td><p><span data-ttu-id="1833d-291">Eine übergeordnete Datenbank ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-291">A parent database is corrupt.</span></span> <span data-ttu-id="1833d-292">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="1833d-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="1833d-294">-340</span><span class="sxs-lookup"><span data-stu-id="1833d-294">-340</span></span></p></td>
<td><p><span data-ttu-id="1833d-295">Der availext-Cache entspricht nicht der B +-Struktur.</span><span class="sxs-lookup"><span data-stu-id="1833d-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="1833d-296">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="1833d-298">-341</span><span class="sxs-lookup"><span data-stu-id="1833d-298">-341</span></span></p></td>
<td><p><span data-ttu-id="1833d-299">Die Struktur des allavailext-Raums ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="1833d-300">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1833d-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="1833d-302">-342</span><span class="sxs-lookup"><span data-stu-id="1833d-302">-342</span></span></p></td>
<td><p><span data-ttu-id="1833d-303">Fehler aufgrund von nicht genügend Arbeitsspeicher beim Zuordnen eines availext-Cache Knotens.</span><span class="sxs-lookup"><span data-stu-id="1833d-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="1833d-304">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="1833d-306">-343</span><span class="sxs-lookup"><span data-stu-id="1833d-306">-343</span></span></p></td>
<td><p><span data-ttu-id="1833d-307">Der OwnExt-Raum Baum ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="1833d-308">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="1833d-310">-344</span><span class="sxs-lookup"><span data-stu-id="1833d-310">-344</span></span></p></td>
<td><p><span data-ttu-id="1833d-311">Der dbtime-Wert auf der aktuellen Seite ist größer als die globale dbtime-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1833d-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="1833d-312">Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="1833d-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="1833d-314">-346</span><span class="sxs-lookup"><span data-stu-id="1833d-314">-346</span></span></p></td>
<td><p><span data-ttu-id="1833d-315">Der Versuch, einen Schlüssel für einen Index Eintrag zu erstellen, ist fehlgeschlagen, da der Schlüssel abgeschnitten wurde und die Index Definition die Schlüssel abgeschnittene nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="1833d-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="1833d-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="1833d-317">-408</span><span class="sxs-lookup"><span data-stu-id="1833d-317">-408</span></span></p></td>
<td><p><span data-ttu-id="1833d-318">Der Schlüssel ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="1833d-318">The key is too large.</span></span> <span data-ttu-id="1833d-319">Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="1833d-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="1833d-321">-500</span><span class="sxs-lookup"><span data-stu-id="1833d-321">-500</span></span></p></td>
<td><p><span data-ttu-id="1833d-322">Der protokollierte Vorgang kann nicht wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="1833d-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="1833d-324">-501</span><span class="sxs-lookup"><span data-stu-id="1833d-324">-501</span></span></p></td>
<td><p><span data-ttu-id="1833d-325">Die Protokolldatei ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="1833d-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="1833d-327">-503</span><span class="sxs-lookup"><span data-stu-id="1833d-327">-503</span></span></p></td>
<td><p><span data-ttu-id="1833d-328">Es wurde kein Sicherungs Verzeichnis angegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="1833d-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="1833d-330">-504</span><span class="sxs-lookup"><span data-stu-id="1833d-330">-504</span></span></p></td>
<td><p><span data-ttu-id="1833d-331">Das Sicherungs Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="1833d-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="1833d-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="1833d-333">-505</span><span class="sxs-lookup"><span data-stu-id="1833d-333">-505</span></span></p></td>
<td><p><span data-ttu-id="1833d-334">Die Sicherung ist bereits aktiv.</span><span class="sxs-lookup"><span data-stu-id="1833d-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1833d-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="1833d-336">-506</span><span class="sxs-lookup"><span data-stu-id="1833d-336">-506</span></span></p></td>
<td><p><span data-ttu-id="1833d-337">Eine Wiederherstellung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="1833d-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="1833d-339">-509</span><span class="sxs-lookup"><span data-stu-id="1833d-339">-509</span></span></p></td>
<td><p><span data-ttu-id="1833d-340">Die Protokolldatei fehlt für den Prüf Punkt.</span><span class="sxs-lookup"><span data-stu-id="1833d-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="1833d-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="1833d-342">-510</span><span class="sxs-lookup"><span data-stu-id="1833d-342">-510</span></span></p></td>
<td><p><span data-ttu-id="1833d-343">Fehler beim Schreiben in die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="1833d-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="1833d-345">-511</span><span class="sxs-lookup"><span data-stu-id="1833d-345">-511</span></span></p></td>
<td><p><span data-ttu-id="1833d-346">Der Versuch, nach der Wiederherstellung in das Protokoll zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1833d-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="1833d-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="1833d-348">-512</span><span class="sxs-lookup"><span data-stu-id="1833d-348">-512</span></span></p></td>
<td><p><span data-ttu-id="1833d-349">Fehler beim Schreiben in das Protokoll während der Wiederherstellungs Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="1833d-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="1833d-351">-513</span><span class="sxs-lookup"><span data-stu-id="1833d-351">-513</span></span></p></td>
<td><p><span data-ttu-id="1833d-352">Der Name der Protokolldatei entspricht nicht der internen Generierungs Nummer.</span><span class="sxs-lookup"><span data-stu-id="1833d-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="1833d-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="1833d-354">-514</span><span class="sxs-lookup"><span data-stu-id="1833d-354">-514</span></span></p></td>
<td><p><span data-ttu-id="1833d-355">Die Version der Protokolldatei ist nicht mit der ESE-Version kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1833d-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="1833d-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="1833d-357">-515</span><span class="sxs-lookup"><span data-stu-id="1833d-357">-515</span></span></p></td>
<td><p><span data-ttu-id="1833d-358">Der Zeitstempel im nächsten Protokoll stimmt nicht mit dem erwarteten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1833d-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="1833d-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="1833d-360">-516</span><span class="sxs-lookup"><span data-stu-id="1833d-360">-516</span></span></p></td>
<td><p><span data-ttu-id="1833d-361">Das Protokoll ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="1833d-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="1833d-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="1833d-363">-517</span><span class="sxs-lookup"><span data-stu-id="1833d-363">-517</span></span></p></td>
<td><p><span data-ttu-id="1833d-364">Der Protokollpuffer ist zu klein für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="1833d-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="1833d-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="1833d-366">-519</span><span class="sxs-lookup"><span data-stu-id="1833d-366">-519</span></span></p></td>
<td><p><span data-ttu-id="1833d-367">Die maximale Protokolldatei Nummer wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1833d-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="1833d-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="1833d-369">-520</span><span class="sxs-lookup"><span data-stu-id="1833d-369">-520</span></span></p></td>
<td><p><span data-ttu-id="1833d-370">Es wird keine Sicherung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="1833d-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="1833d-372">-521</span><span class="sxs-lookup"><span data-stu-id="1833d-372">-521</span></span></p></td>
<td><p><span data-ttu-id="1833d-373">Der Sicherungs Aufrufwert ist nicht in der Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1833d-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="1833d-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="1833d-375">-523</span><span class="sxs-lookup"><span data-stu-id="1833d-375">-523</span></span></p></td>
<td><p><span data-ttu-id="1833d-376">Zurzeit kann keine Sicherung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="1833d-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="1833d-378">-524</span><span class="sxs-lookup"><span data-stu-id="1833d-378">-524</span></span></p></td>
<td><p><span data-ttu-id="1833d-379">Eine Sicherungsdatei konnte nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="1833d-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="1833d-381">-525</span><span class="sxs-lookup"><span data-stu-id="1833d-381">-525</span></span></p></td>
<td><p><span data-ttu-id="1833d-382">Das temporäre Sicherungs Verzeichnis konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="1833d-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="1833d-384">-526</span><span class="sxs-lookup"><span data-stu-id="1833d-384">-526</span></span></p></td>
<td><p><span data-ttu-id="1833d-385">Zirkuläre Protokollierung ist aktiviert. eine inkrementelle Sicherung kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="1833d-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="1833d-387">-527</span><span class="sxs-lookup"><span data-stu-id="1833d-387">-527</span></span></p></td>
<td><p><span data-ttu-id="1833d-388">Die Daten wurden mit Fehlern wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="1833d-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="1833d-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="1833d-390">-528</span><span class="sxs-lookup"><span data-stu-id="1833d-390">-528</span></span></p></td>
<td><p><span data-ttu-id="1833d-391">Die aktuelle Protokolldatei fehlt.</span><span class="sxs-lookup"><span data-stu-id="1833d-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="1833d-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="1833d-393">-529</span><span class="sxs-lookup"><span data-stu-id="1833d-393">-529</span></span></p></td>
<td><p><span data-ttu-id="1833d-394">Der Protokolldatenträger ist voll.</span><span class="sxs-lookup"><span data-stu-id="1833d-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="1833d-396">-530</span><span class="sxs-lookup"><span data-stu-id="1833d-396">-530</span></span></p></td>
<td><p><span data-ttu-id="1833d-397">Für eine Protokolldatei ist eine ungültige Signatur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="1833d-399">-531</span><span class="sxs-lookup"><span data-stu-id="1833d-399">-531</span></span></p></td>
<td><p><span data-ttu-id="1833d-400">Für eine Datenbankdatei ist eine ungültige Signatur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="1833d-402">-532</span><span class="sxs-lookup"><span data-stu-id="1833d-402">-532</span></span></p></td>
<td><p><span data-ttu-id="1833d-403">Es ist eine ungültige Signatur für eine Prüf Punkt Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="1833d-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="1833d-405">-533</span><span class="sxs-lookup"><span data-stu-id="1833d-405">-533</span></span></p></td>
<td><p><span data-ttu-id="1833d-406">Die Prüf Punkt Datei wurde nicht gefunden oder ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1833d-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="1833d-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="1833d-408">-534</span><span class="sxs-lookup"><span data-stu-id="1833d-408">-534</span></span></p></td>
<td><p><span data-ttu-id="1833d-409">Die Seite "Datenbank-Patchdatei" wurde während der Wiederherstellung nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="1833d-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="1833d-411">-535</span><span class="sxs-lookup"><span data-stu-id="1833d-411">-535</span></span></p></td>
<td><p><span data-ttu-id="1833d-412">Die Seite "Datenbank-Patchdatei" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="1833d-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="1833d-414">-536</span><span class="sxs-lookup"><span data-stu-id="1833d-414">-536</span></span></p></td>
<td><p><span data-ttu-id="1833d-415">Die Wiederholung wurde aufgrund eines plötzlichen Fehlers beim Lesen der Protokolle aus der Protokolldatei plötzlich beendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="1833d-417">-537</span><span class="sxs-lookup"><span data-stu-id="1833d-417">-537</span></span></p></td>
<td><p><span data-ttu-id="1833d-418">Dieses Flag ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="1833d-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="1833d-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="1833d-420">-538</span><span class="sxs-lookup"><span data-stu-id="1833d-420">-538</span></span></p></td>
<td><p><span data-ttu-id="1833d-421">Die feste Wiederherstellung hat erkannt, dass eine datenbankpatchdatei im Sicherungs Satz fehlt.</span><span class="sxs-lookup"><span data-stu-id="1833d-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="1833d-423">-539</span><span class="sxs-lookup"><span data-stu-id="1833d-423">-539</span></span></p></td>
<td><p><span data-ttu-id="1833d-424">Die Datenbank gehört nicht zum aktuellen Satz von Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="1833d-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="1833d-426">-540</span><span class="sxs-lookup"><span data-stu-id="1833d-426">-540</span></span></p></td>
<td><p><span data-ttu-id="1833d-427">Dieses Flag ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="1833d-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="1833d-429">-541</span><span class="sxs-lookup"><span data-stu-id="1833d-429">-541</span></span></p></td>
<td><p><span data-ttu-id="1833d-430">Die tatsächliche Protokolldatei Größe entspricht nicht <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="1833d-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="1833d-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="1833d-432">-542</span><span class="sxs-lookup"><span data-stu-id="1833d-432">-542</span></span></p></td>
<td><p><span data-ttu-id="1833d-433">Die Prüf Punkt Datei konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="1833d-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="1833d-435">-543</span><span class="sxs-lookup"><span data-stu-id="1833d-435">-543</span></span></p></td>
<td><p><span data-ttu-id="1833d-436">Die für die Wiederherstellung erforderlichen Protokolldateien fehlen.</span><span class="sxs-lookup"><span data-stu-id="1833d-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="1833d-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="1833d-438">-544</span><span class="sxs-lookup"><span data-stu-id="1833d-438">-544</span></span></p></td>
<td><p><span data-ttu-id="1833d-439">Eine weiche Wiederherstellung wird in der Regel für eine Sicherungs Datenbank verwendet, wenn stattdessen eine Wiederherstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1833d-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="1833d-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="1833d-441">-545</span><span class="sxs-lookup"><span data-stu-id="1833d-441">-545</span></span></p></td>
<td><p><span data-ttu-id="1833d-442">Die Datenbanken wurden wieder hergestellt, die Protokolldatei Größe, die während der Wiederherstellung verwendet wird, stimmt jedoch nicht mit <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="1833d-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="1833d-444">-546</span><span class="sxs-lookup"><span data-stu-id="1833d-444">-546</span></span></p></td>
<td><p><span data-ttu-id="1833d-445">Die Sektorgröße der Protokolldatei stimmt nicht mit der Sektorgröße des aktuellen Volumes identisch.</span><span class="sxs-lookup"><span data-stu-id="1833d-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="1833d-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="1833d-447">-547</span><span class="sxs-lookup"><span data-stu-id="1833d-447">-547</span></span></p></td>
<td><p><span data-ttu-id="1833d-448">Die Datenbanken wurden wieder hergestellt, aber die Sektorgröße der Protokolldatei (die während der Wiederherstellung verwendet wird) entspricht nicht der Sektorgröße des aktuellen Volumes.</span><span class="sxs-lookup"><span data-stu-id="1833d-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="1833d-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="1833d-450">-548</span><span class="sxs-lookup"><span data-stu-id="1833d-450">-548</span></span></p></td>
<td><p><span data-ttu-id="1833d-451">Die Datenbanken wurden wieder hergestellt, aber alle möglichen Protokoll Generierungen in der aktuellen Sequenz wurden verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="1833d-452">Alle Protokolldateien und die Prüf Punkt Datei müssen gelöscht werden, und die Datenbanken müssen gesichert werden, bevor Sie fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="1833d-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="1833d-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="1833d-454">-549</span><span class="sxs-lookup"><span data-stu-id="1833d-454">-549</span></span></p></td>
<td><p><span data-ttu-id="1833d-455">Es wurde ein unzulässiger Versuch unternommen, einen Vorgang zum Streamen von Dateien wiederzugeben, bei dem die Daten nicht protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="1833d-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="1833d-456">Dies wird wahrscheinlich durch einen Roll Forward-Versuch verursacht, bei dem die zirkuläre Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="1833d-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="1833d-458">-550</span><span class="sxs-lookup"><span data-stu-id="1833d-458">-550</span></span></p></td>
<td><p><span data-ttu-id="1833d-459">Die Datenbank wurde nicht ordnungsgemäß heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="1833d-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="1833d-460">Eine Wiederherstellung muss zuerst ausgeführt werden, um Daten Bank Vorgänge für das vorherige Herunterfahren ordnungsgemäß abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1833d-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="1833d-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="1833d-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="1833d-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="1833d-463">Dieser Fehler ist veraltet und wurde durch JET_errDatabaseDirtyShutdown ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1833d-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="1833d-465">-551</span><span class="sxs-lookup"><span data-stu-id="1833d-465">-551</span></span></p></td>
<td><p><span data-ttu-id="1833d-466">Der letzte konsistente Zeitpunkt für die Datenbank wurde nicht abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="1833d-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="1833d-468">-552</span><span class="sxs-lookup"><span data-stu-id="1833d-468">-552</span></span></p></td>
<td><p><span data-ttu-id="1833d-469">Die Datenbank-Patchdatei wird nicht aus dieser Sicherung generiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="1833d-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="1833d-471">-553</span><span class="sxs-lookup"><span data-stu-id="1833d-471">-553</span></span></p></td>
<td><p><span data-ttu-id="1833d-472">Die Start Protokollnummer ist zu niedrig für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="1833d-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="1833d-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="1833d-474">-554</span><span class="sxs-lookup"><span data-stu-id="1833d-474">-554</span></span></p></td>
<td><p><span data-ttu-id="1833d-475">Die Start Protokollnummer ist zu hoch für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="1833d-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="1833d-477">-555</span><span class="sxs-lookup"><span data-stu-id="1833d-477">-555</span></span></p></td>
<td><p><span data-ttu-id="1833d-478">Die Wiederherstellungs Protokolldatei hat eine ungültige Signatur.</span><span class="sxs-lookup"><span data-stu-id="1833d-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="1833d-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="1833d-480">-556</span><span class="sxs-lookup"><span data-stu-id="1833d-480">-556</span></span></p></td>
<td><p><span data-ttu-id="1833d-481">Die Wiederherstellungs Protokolldatei ist nicht zusammenhängend.</span><span class="sxs-lookup"><span data-stu-id="1833d-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="1833d-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="1833d-483">-557</span><span class="sxs-lookup"><span data-stu-id="1833d-483">-557</span></span></p></td>
<td><p><span data-ttu-id="1833d-484">Einige Wiederherstellungs Protokolldateien fehlen.</span><span class="sxs-lookup"><span data-stu-id="1833d-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="1833d-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="1833d-486">-560</span><span class="sxs-lookup"><span data-stu-id="1833d-486">-560</span></span></p></td>
<td><p><span data-ttu-id="1833d-487">Die Datenbank hat vor dem Versuch, eine inkrementelle Sicherung auszuführen, eine vorherige vollständige Sicherung verpasst.</span><span class="sxs-lookup"><span data-stu-id="1833d-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="1833d-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="1833d-489">-561</span><span class="sxs-lookup"><span data-stu-id="1833d-489">-561</span></span></p></td>
<td><p><span data-ttu-id="1833d-490">Die Größe der Sicherungs Datenbank ist kein Vielfaches der Seitengröße der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1833d-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="1833d-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="1833d-492">-562</span><span class="sxs-lookup"><span data-stu-id="1833d-492">-562</span></span></p></td>
<td><p><span data-ttu-id="1833d-493">Der aktuelle Versuch, eine Datenbank zu aktualisieren, wurde angehalten, da die Datenbank bereits aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="1833d-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="1833d-495">-563</span><span class="sxs-lookup"><span data-stu-id="1833d-495">-563</span></span></p></td>
<td><p><span data-ttu-id="1833d-496">Die Datenbank wurde nur teilweise in das aktuelle Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="1833d-497">Die Datenbank muss von der Sicherung wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="1833d-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="1833d-499">-565</span><span class="sxs-lookup"><span data-stu-id="1833d-499">-565</span></span></p></td>
<td><p><span data-ttu-id="1833d-500">Einige aktuelle Protokolldateien fehlen für die fortlaufende Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="1833d-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="1833d-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="1833d-502">-566</span><span class="sxs-lookup"><span data-stu-id="1833d-502">-566</span></span></p></td>
<td><p><span data-ttu-id="1833d-503">Der dbtime fest-Wert auf einer Seite ist kleiner als der dbtimebefore-Wert, der im Datensatz liegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="1833d-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="1833d-505">-567</span><span class="sxs-lookup"><span data-stu-id="1833d-505">-567</span></span></p></td>
<td><p><span data-ttu-id="1833d-506">Der dbtime fest-Wert auf einer Seite liegt vor dem dbtimebefore-Wert, der im Datensatz liegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="1833d-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="1833d-508">-569</span><span class="sxs-lookup"><span data-stu-id="1833d-508">-569</span></span></p></td>
<td><p><span data-ttu-id="1833d-509">Einige Protokolldateien oder Datenbank-Patchdateien fehlten während der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="1833d-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="1833d-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="1833d-511">-570</span><span class="sxs-lookup"><span data-stu-id="1833d-511">-570</span></span></p></td>
<td><p><span data-ttu-id="1833d-512">Ein zerrissener Schreibvorgang wurde in einer Sicherung erkannt, die während einer fest Wiederherstellung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="1833d-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="1833d-514">-571</span><span class="sxs-lookup"><span data-stu-id="1833d-514">-571</span></span></p></td>
<td><p><span data-ttu-id="1833d-515">Während einer fest Wiederherstellung wurde ein zerrissener Schreibvorgang erkannt (das Protokoll war nicht Teil eines Sicherungs Satzes).</span><span class="sxs-lookup"><span data-stu-id="1833d-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="1833d-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="1833d-517">-573</span><span class="sxs-lookup"><span data-stu-id="1833d-517">-573</span></span></p></td>
<td><p><span data-ttu-id="1833d-518">Während einer fest Wiederherstellung wurde in einem Sicherungs Satz eine Beschädigung festgestellt.</span><span class="sxs-lookup"><span data-stu-id="1833d-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="1833d-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="1833d-520">-574</span><span class="sxs-lookup"><span data-stu-id="1833d-520">-574</span></span></p></td>
<td><p><span data-ttu-id="1833d-521">Während der fest Wiederherstellung wurde eine Beschädigung festgestellt (das Protokoll war nicht Teil eines Sicherungs Satzes).</span><span class="sxs-lookup"><span data-stu-id="1833d-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="1833d-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="1833d-523">-575</span><span class="sxs-lookup"><span data-stu-id="1833d-523">-575</span></span></p></td>
<td><p><span data-ttu-id="1833d-524">Beim Upgraden einer Datenbank kann die Protokollierung nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="1833d-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="1833d-526">-577</span><span class="sxs-lookup"><span data-stu-id="1833d-526">-577</span></span></p></td>
<td><p><span data-ttu-id="1833d-527">Entweder wurde die für die Wiederherstellung angegebene TargetInstance nicht gefunden, oder die Protokolldateien stimmen nicht ab.</span><span class="sxs-lookup"><span data-stu-id="1833d-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="1833d-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="1833d-529">-579</span><span class="sxs-lookup"><span data-stu-id="1833d-529">-579</span></span></p></td>
<td><p><span data-ttu-id="1833d-530">Die Datenbank-Engine hat alle Vorgänge im Transaktionsprotokoll wiedergegeben, um eine Wiederherstellung durchzuführen, aber der Aufrufer hat die Wiederherstellung beendet, ohne dass ein Rollback für nicht ausgeführten Updates</span><span class="sxs-lookup"><span data-stu-id="1833d-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="1833d-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="1833d-532">-580</span><span class="sxs-lookup"><span data-stu-id="1833d-532">-580</span></span></p></td>
<td><p><span data-ttu-id="1833d-533">Die wiederherzustellenden Datenbanken stammen nicht aus derselben Schattenkopiesicherung.</span><span class="sxs-lookup"><span data-stu-id="1833d-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="1833d-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="1833d-535">-581</span><span class="sxs-lookup"><span data-stu-id="1833d-535">-581</span></span></p></td>
<td><p><span data-ttu-id="1833d-536">Es gibt eine weiche Wiederherstellung einer Datenbank aus einem schattenkopiesicherungssatz.</span><span class="sxs-lookup"><span data-stu-id="1833d-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="1833d-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="1833d-538">-601</span><span class="sxs-lookup"><span data-stu-id="1833d-538">-601</span></span></p></td>
<td><p><span data-ttu-id="1833d-539">Der Unicode-Übersetzungs Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="1833d-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="1833d-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="1833d-541">-602</span><span class="sxs-lookup"><span data-stu-id="1833d-541">-602</span></span></p></td>
<td><p><span data-ttu-id="1833d-542">Die Unicode-Normalisierung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1833d-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="1833d-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="1833d-544">-603</span><span class="sxs-lookup"><span data-stu-id="1833d-544">-603</span></span></p></td>
<td><p><span data-ttu-id="1833d-545">Das Betriebssystem bietet keine Unterstützung für die Unicode-Normalisierung, und es wurde kein normalisierungs Rückruf angegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="1833d-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="1833d-547">-610</span><span class="sxs-lookup"><span data-stu-id="1833d-547">-610</span></span></p></td>
<td><p><span data-ttu-id="1833d-548">Die vorhandene Protokolldatei hat eine ungültige Signatur.</span><span class="sxs-lookup"><span data-stu-id="1833d-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="1833d-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="1833d-550">-611</span><span class="sxs-lookup"><span data-stu-id="1833d-550">-611</span></span></p></td>
<td><p><span data-ttu-id="1833d-551">Eine vorhandene Protokolldatei ist nicht zusammenhängend.</span><span class="sxs-lookup"><span data-stu-id="1833d-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="1833d-553">-612</span><span class="sxs-lookup"><span data-stu-id="1833d-553">-612</span></span></p></td>
<td><p><span data-ttu-id="1833d-554">In der Protokolldatei wurde während der Sicherung ein Prüfsummen Fehler gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="1833d-556">-613</span><span class="sxs-lookup"><span data-stu-id="1833d-556">-613</span></span></p></td>
<td><p><span data-ttu-id="1833d-557">Dieses Flag ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="1833d-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="1833d-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="1833d-559">-614</span><span class="sxs-lookup"><span data-stu-id="1833d-559">-614</span></span></p></td>
<td><p><span data-ttu-id="1833d-560">Zwischen dem Prüfpunkt und der aktuellen Generierung sind zu viele ausstehende Generationen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="1833d-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="1833d-562">-615</span><span class="sxs-lookup"><span data-stu-id="1833d-562">-615</span></span></p></td>
<td><p><span data-ttu-id="1833d-563">Für eine Datenbank, die keine Sicherungs Datenbank war, wurde eine harte Wiederherstellung versucht.</span><span class="sxs-lookup"><span data-stu-id="1833d-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1833d-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="1833d-565">-900</span><span class="sxs-lookup"><span data-stu-id="1833d-565">-900</span></span></p></td>
<td><p><span data-ttu-id="1833d-566">Es ist ein ungültiger grbit-Parameter vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1833d-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="1833d-568">-1000</span><span class="sxs-lookup"><span data-stu-id="1833d-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="1833d-569">Die Beendigung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1833d-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="1833d-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="1833d-571">-1001</span><span class="sxs-lookup"><span data-stu-id="1833d-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="1833d-572">Dieses API-Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1833d-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="1833d-574">-1002</span><span class="sxs-lookup"><span data-stu-id="1833d-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="1833d-575">Ein ungültiger Name wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1833d-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="1833d-577">-1003</span><span class="sxs-lookup"><span data-stu-id="1833d-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="1833d-578">Ein ungültiger API-Parameter wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="1833d-580">-1008</span><span class="sxs-lookup"><span data-stu-id="1833d-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="1833d-581">Es wurde versucht, eine schreibgeschützte Datenbankdatei für Lese-/Schreibvorgänge anzufügen.</span><span class="sxs-lookup"><span data-stu-id="1833d-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="1833d-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="1833d-583">-1010</span><span class="sxs-lookup"><span data-stu-id="1833d-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="1833d-584">Es ist eine ungültige Datenbank-ID vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1833d-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="1833d-586">-1011</span><span class="sxs-lookup"><span data-stu-id="1833d-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="1833d-587">Das System verfügt nicht über genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1833d-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="1833d-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="1833d-589">-1012</span><span class="sxs-lookup"><span data-stu-id="1833d-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="1833d-590">Die maximale Datenbankgröße wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="1833d-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="1833d-592">-1013</span><span class="sxs-lookup"><span data-stu-id="1833d-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="1833d-593">Die Tabelle ist nicht von den Cursorn.</span><span class="sxs-lookup"><span data-stu-id="1833d-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="1833d-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="1833d-595">-1014</span><span class="sxs-lookup"><span data-stu-id="1833d-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="1833d-596">Die Datenbank befindet sich nicht im Seiten Puffer.</span><span class="sxs-lookup"><span data-stu-id="1833d-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="1833d-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="1833d-598">-1015</span><span class="sxs-lookup"><span data-stu-id="1833d-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="1833d-599">Es sind zu viele Indizes vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="1833d-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="1833d-601">-1016</span><span class="sxs-lookup"><span data-stu-id="1833d-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="1833d-602">Es gibt zu viele Spalten in einem Index.</span><span class="sxs-lookup"><span data-stu-id="1833d-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="1833d-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="1833d-604">-1017</span><span class="sxs-lookup"><span data-stu-id="1833d-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="1833d-605">Der Datensatz wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1833d-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="1833d-607">-1018</span><span class="sxs-lookup"><span data-stu-id="1833d-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="1833d-608">Prüfsummen Fehler auf einer Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="1833d-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1833d-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="1833d-610">-1019</span><span class="sxs-lookup"><span data-stu-id="1833d-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="1833d-611">Es gibt eine leere Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="1833d-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="1833d-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="1833d-613">-1020</span><span class="sxs-lookup"><span data-stu-id="1833d-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="1833d-614">Es sind keine Datei Handles vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="1833d-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="1833d-616">-1022</span><span class="sxs-lookup"><span data-stu-id="1833d-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="1833d-617">Ein Datenträger-e/a-Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1833d-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="1833d-619">-1023</span><span class="sxs-lookup"><span data-stu-id="1833d-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="1833d-620">Ungültiger Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="1833d-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="1833d-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="1833d-622">-1024</span><span class="sxs-lookup"><span data-stu-id="1833d-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="1833d-623">Es ist ein ungültiger Systempfad vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="1833d-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="1833d-625">-1025</span><span class="sxs-lookup"><span data-stu-id="1833d-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="1833d-626">Es ist ein ungültiges Protokoll Verzeichnis vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="1833d-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="1833d-628">-1026</span><span class="sxs-lookup"><span data-stu-id="1833d-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="1833d-629">Der Datensatz ist größer als die maximale Größe.</span><span class="sxs-lookup"><span data-stu-id="1833d-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="1833d-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="1833d-631">-1027</span><span class="sxs-lookup"><span data-stu-id="1833d-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="1833d-632">Es sind zu viele geöffnete Datenbanken vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="1833d-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="1833d-634">-1028</span><span class="sxs-lookup"><span data-stu-id="1833d-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="1833d-635">Dabei handelt es sich nicht um eine Datenbankdatei.</span><span class="sxs-lookup"><span data-stu-id="1833d-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1833d-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="1833d-637">-1029</span><span class="sxs-lookup"><span data-stu-id="1833d-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="1833d-638">Die Datenbank-Engine wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="1833d-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="1833d-640">-1030</span><span class="sxs-lookup"><span data-stu-id="1833d-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="1833d-641">Die Datenbank-Engine ist bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="1833d-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="1833d-643">-1031</span><span class="sxs-lookup"><span data-stu-id="1833d-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="1833d-644">Die Datenbank-Engine wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="1833d-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="1833d-646">-1032</span><span class="sxs-lookup"><span data-stu-id="1833d-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="1833d-647">Auf die Datei kann nicht zugegriffen werden, da die Datei gesperrt ist oder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="1833d-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="1833d-649">-1038</span><span class="sxs-lookup"><span data-stu-id="1833d-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="1833d-650">Der Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="1833d-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="1833d-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="1833d-652">-1040</span><span class="sxs-lookup"><span data-stu-id="1833d-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="1833d-653">Es sind zu viele Spalten definiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="1833d-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="1833d-655">-1043</span><span class="sxs-lookup"><span data-stu-id="1833d-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="1833d-656">Der Container ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="1833d-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="1833d-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="1833d-658">-1044</span><span class="sxs-lookup"><span data-stu-id="1833d-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="1833d-659">Der Dateiname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="1833d-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="1833d-661">-1045</span><span class="sxs-lookup"><span data-stu-id="1833d-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="1833d-662">Es ist ein ungültiges Lesezeichen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="1833d-664">-1046</span><span class="sxs-lookup"><span data-stu-id="1833d-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="1833d-665">Die verwendete Spalte befindet sich in einem Index.</span><span class="sxs-lookup"><span data-stu-id="1833d-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="1833d-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="1833d-667">-1047</span><span class="sxs-lookup"><span data-stu-id="1833d-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="1833d-668">Der Datenpuffer stimmt nicht mit der Spaltengröße identisch.</span><span class="sxs-lookup"><span data-stu-id="1833d-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="1833d-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="1833d-670">-1048</span><span class="sxs-lookup"><span data-stu-id="1833d-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="1833d-671">Der Spaltenwert kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="1833d-673">-1051</span><span class="sxs-lookup"><span data-stu-id="1833d-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="1833d-674">Der Index wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="1833d-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="1833d-676">-1052</span><span class="sxs-lookup"><span data-stu-id="1833d-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="1833d-677">Die Link Unterstützung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1833d-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="1833d-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="1833d-679">-1053</span><span class="sxs-lookup"><span data-stu-id="1833d-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="1833d-680">NULL-Schlüssel sind für einen Index nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="1833d-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="1833d-682">-1054</span><span class="sxs-lookup"><span data-stu-id="1833d-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="1833d-683">Der Vorgang muss innerhalb einer Transaktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="1833d-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="1833d-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="1833d-685">-1059</span><span class="sxs-lookup"><span data-stu-id="1833d-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="1833d-686">Es sind zu viele aktive Datenbankbenutzer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="1833d-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="1833d-688">-1061</span><span class="sxs-lookup"><span data-stu-id="1833d-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="1833d-689">Es ist ein ungültiger oder unbekannter Ländercode vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1833d-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="1833d-691">-1062</span><span class="sxs-lookup"><span data-stu-id="1833d-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="1833d-692">Es ist eine ungültige oder unbekannte Sprach-ID vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="1833d-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="1833d-694">-1063</span><span class="sxs-lookup"><span data-stu-id="1833d-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="1833d-695">Es ist eine ungültige oder unbekannte Codepage vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="1833d-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="1833d-697">-1064</span><span class="sxs-lookup"><span data-stu-id="1833d-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="1833d-698">Es werden ungültige Flags für " <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="1833d-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="1833d-700">-1065</span><span class="sxs-lookup"><span data-stu-id="1833d-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="1833d-701">Es wurde versucht, einen Versionsspeicher Eintrag (RCE) zu erstellen, der größer als ein versionsbucket war.</span><span class="sxs-lookup"><span data-stu-id="1833d-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="1833d-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="1833d-703">-1066</span><span class="sxs-lookup"><span data-stu-id="1833d-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="1833d-704">Der Versionsspeicher weist nicht genügend Arbeitsspeicher auf, und der Bereinigungs Versuch konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1833d-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="1833d-706">-1069</span><span class="sxs-lookup"><span data-stu-id="1833d-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="1833d-707">Der Versionsspeicher weist nicht genügend Arbeitsspeicher auf, und es wurde bereits versucht, eine Bereinigung auszuführen.)</span><span class="sxs-lookup"><span data-stu-id="1833d-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="1833d-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="1833d-709">-1071</span><span class="sxs-lookup"><span data-stu-id="1833d-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="1833d-710">Die Spalten "hinterlegter" und "SLV" können nicht indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="1833d-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="1833d-712">-1072</span><span class="sxs-lookup"><span data-stu-id="1833d-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="1833d-713">Der Datensatz wurde nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1833d-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="1833d-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="1833d-715">-1073</span><span class="sxs-lookup"><span data-stu-id="1833d-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="1833d-716">Es wurden zu viele mempool-Einträge angefordert.</span><span class="sxs-lookup"><span data-stu-id="1833d-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="1833d-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="1833d-718">-1074</span><span class="sxs-lookup"><span data-stu-id="1833d-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="1833d-719">Die Datenbank befindet sich außerhalb der B +-Struktur-ObjectIDs, sodass eine Offline Defragmentierung ausgeführt werden muss, um freigegebene oder nicht verwendete ObjectIDs freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="1833d-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="1833d-721">-1075</span><span class="sxs-lookup"><span data-stu-id="1833d-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="1833d-722">Der lange Wert-ID-Leistungs Bewert hat den maximalen Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="1833d-723">Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete longvalueids freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="1833d-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="1833d-725">-1076</span><span class="sxs-lookup"><span data-stu-id="1833d-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="1833d-726">Der Wert für automatische Inkrement hat den maximalen Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="1833d-727">Eine Offline Defragmentierung kann keine freien oder nicht genutzten automatischen Inkrement-Werte freigeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="1833d-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="1833d-729">-1077</span><span class="sxs-lookup"><span data-stu-id="1833d-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="1833d-730">Der dbtime-Leistungswert hat den maximalen Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="1833d-731">Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete dbtime-Werte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="1833d-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="1833d-733">-1078</span><span class="sxs-lookup"><span data-stu-id="1833d-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="1833d-734">Ein sequenzieller Index Indikator hat den maximalen Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="1833d-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="1833d-735">Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete sequentialindex-Werte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1833d-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="1833d-737">-1080</span><span class="sxs-lookup"><span data-stu-id="1833d-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="1833d-738">Bei diesem multiinstanzaufruter ist der einzelinstanzmodus aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1833d-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1833d-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="1833d-740">-1081</span><span class="sxs-lookup"><span data-stu-id="1833d-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="1833d-741">Bei diesem einzelinstanzrückruf ist der Modus für mehrere Instanzen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1833d-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="1833d-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="1833d-743">-1082</span><span class="sxs-lookup"><span data-stu-id="1833d-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="1833d-744">Die globalen Systemparameter wurden bereits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="1833d-746">-1083</span><span class="sxs-lookup"><span data-stu-id="1833d-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="1833d-747">Der Systempfad wird bereits von einer anderen Daten Bank Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="1833d-749">-1084</span><span class="sxs-lookup"><span data-stu-id="1833d-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="1833d-750">Der Protokolldatei Pfad wird bereits von einer anderen Daten Bank Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="1833d-752">-1085</span><span class="sxs-lookup"><span data-stu-id="1833d-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="1833d-753">Der Pfad zur temporären Datenbank wird bereits von einer anderen Daten Bank Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="1833d-755">-1086</span><span class="sxs-lookup"><span data-stu-id="1833d-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="1833d-756">Der Instanzname wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1833d-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="1833d-758">-1090</span><span class="sxs-lookup"><span data-stu-id="1833d-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="1833d-759">Diese Instanz kann nicht verwendet werden, da ein schwerwiegender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="1833d-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="1833d-761">-1091</span><span class="sxs-lookup"><span data-stu-id="1833d-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="1833d-762">Diese Datenbank kann nicht verwendet werden, weil ein schwerwiegender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="1833d-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="1833d-764">-1092</span><span class="sxs-lookup"><span data-stu-id="1833d-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="1833d-765">Diese Instanz kann nicht verwendet werden, da beim Ausführen eines Vorgangs (z. b. einem Transaktionsrollback) ein Fehler aufgrund eines Protokoll Datenträgers aufgetreten ist, der einen Fehler nicht tolerieren konnte.</span><span class="sxs-lookup"><span data-stu-id="1833d-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="1833d-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="1833d-767">-1101</span><span class="sxs-lookup"><span data-stu-id="1833d-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="1833d-768">Die Datenbank ist nicht in der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1833d-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="1833d-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="1833d-770">-1102</span><span class="sxs-lookup"><span data-stu-id="1833d-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="1833d-771">Fehler bei der Schreibsperre, weil eine ausstehende Schreibsperre vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="1833d-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="1833d-773">-1103</span><span class="sxs-lookup"><span data-stu-id="1833d-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="1833d-774">Die Transaktionen sind zu tief geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="1833d-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="1833d-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="1833d-776">-1104</span><span class="sxs-lookup"><span data-stu-id="1833d-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="1833d-777">Es ist ein ungültiges Sitzungs handle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="1833d-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="1833d-779">-1105</span><span class="sxs-lookup"><span data-stu-id="1833d-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="1833d-780">Es wurde versucht, einen nicht ausgeführtem primären Index zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1833d-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1833d-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="1833d-782">-1108</span><span class="sxs-lookup"><span data-stu-id="1833d-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="1833d-783">Der Vorgang ist innerhalb einer Transaktion nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="1833d-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="1833d-785">-1109</span><span class="sxs-lookup"><span data-stu-id="1833d-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="1833d-786">Für die aktuelle Transaktion muss ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="1833d-787">Ein Commit kann nicht ausgeführt werden, und ein neuer kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="1833d-789">-1110</span><span class="sxs-lookup"><span data-stu-id="1833d-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="1833d-790">Eine schreibgeschützte Transaktion hat versucht, die Datenbank zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1833d-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="1833d-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="1833d-792">-1111</span><span class="sxs-lookup"><span data-stu-id="1833d-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="1833d-793">Es wurde versucht, denselben Datensatz durch zwei verschiedene Cursor in derselben Sitzung zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1833d-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="1833d-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="1833d-795">-1112</span><span class="sxs-lookup"><span data-stu-id="1833d-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="1833d-796">Der Datensatz wäre zu groß, wenn er in einem Datenbankformat aus einer früheren Version von Jet dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="1833d-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="1833d-798">-1113</span><span class="sxs-lookup"><span data-stu-id="1833d-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="1833d-799">Die temporäre Tabelle konnte aufgrund von Parametern, die mit JET_bitTTForwardOnly in Konflikt stehen, nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="1833d-801">-1114</span><span class="sxs-lookup"><span data-stu-id="1833d-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="1833d-802">Das Sitzungs Handle kann nicht mit der Tabellen-ID verwendet werden, da es nicht zum Erstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="1833d-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="1833d-804">-1115</span><span class="sxs-lookup"><span data-stu-id="1833d-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="1833d-805">Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1833d-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="1833d-807">-1119</span><span class="sxs-lookup"><span data-stu-id="1833d-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="1833d-808">Auf der vom Datenträger gelesenen Datenbankseite wurde ein vorheriger Schreibvorgang auf der Seite nicht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1833d-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="1833d-809">Verfügbar unter Windows 8 und höher für den-Client und Windows Server 2012 und höher für den-Server.</span><span class="sxs-lookup"><span data-stu-id="1833d-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="1833d-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="1833d-811">-1201</span><span class="sxs-lookup"><span data-stu-id="1833d-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="1833d-812">Die Datenbank ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="1833d-814">-1202</span><span class="sxs-lookup"><span data-stu-id="1833d-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="1833d-815">Die verwendete Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1833d-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="1833d-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="1833d-817">-1203</span><span class="sxs-lookup"><span data-stu-id="1833d-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="1833d-818">Diese Datenbank ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="1833d-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="1833d-820">-1204</span><span class="sxs-lookup"><span data-stu-id="1833d-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="1833d-821">Der Datenbankname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="1833d-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="1833d-823">-1205</span><span class="sxs-lookup"><span data-stu-id="1833d-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="1833d-824">Es ist eine ungültige Anzahl von Seiten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="1833d-826">-1206</span><span class="sxs-lookup"><span data-stu-id="1833d-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="1833d-827">Es ist eine nicht-Datenbankdatei oder eine beschädigte Datenbank vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="1833d-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="1833d-829">-1207</span><span class="sxs-lookup"><span data-stu-id="1833d-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="1833d-830">Die Datenbank ist exklusiv gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1833d-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="1833d-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="1833d-832">-1208</span><span class="sxs-lookup"><span data-stu-id="1833d-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="1833d-833">Die Versionsverwaltung für diese Datenbank kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="1833d-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="1833d-835">-1209</span><span class="sxs-lookup"><span data-stu-id="1833d-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="1833d-836">Die Datenbank-Engine ist nicht mit der Datenbank kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1833d-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="1833d-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="1833d-838">-1210</span><span class="sxs-lookup"><span data-stu-id="1833d-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="1833d-839">Die Datenbank weist ein älteres Format (200) auf.</span><span class="sxs-lookup"><span data-stu-id="1833d-839">The database is in an older (200) format.</span></span> <span data-ttu-id="1833d-840">Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="1833d-841">Nur Windows NT-Client.</span><span class="sxs-lookup"><span data-stu-id="1833d-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="1833d-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="1833d-843">-1211</span><span class="sxs-lookup"><span data-stu-id="1833d-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="1833d-844">Die Datenbank weist ein älteres Format (400) auf.</span><span class="sxs-lookup"><span data-stu-id="1833d-844">The database is in an older (400) format.</span></span> <span data-ttu-id="1833d-845">Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="1833d-846">Nur Windows NT-Client.</span><span class="sxs-lookup"><span data-stu-id="1833d-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="1833d-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="1833d-848">-1212</span><span class="sxs-lookup"><span data-stu-id="1833d-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="1833d-849">Die Datenbank weist ein älteres Format (500) auf.</span><span class="sxs-lookup"><span data-stu-id="1833d-849">The database is in an older (500) format.</span></span> <span data-ttu-id="1833d-850">Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="1833d-851">Nur Windows NT-Client.</span><span class="sxs-lookup"><span data-stu-id="1833d-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="1833d-853">-1213</span><span class="sxs-lookup"><span data-stu-id="1833d-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="1833d-854">Die Seitengröße der Datenbank stimmt nicht mit der Engine identisch.</span><span class="sxs-lookup"><span data-stu-id="1833d-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="1833d-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="1833d-856">-1214</span><span class="sxs-lookup"><span data-stu-id="1833d-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="1833d-857">Es können keine weiteren Datenbankinstanzen gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1833d-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="1833d-859">-1215</span><span class="sxs-lookup"><span data-stu-id="1833d-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="1833d-860">Diese Datenbank wird von einer anderen Daten Bank Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="1833d-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="1833d-862">-1216</span><span class="sxs-lookup"><span data-stu-id="1833d-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="1833d-863">Am Anfang oder Ende der Wiederherstellung wurde eine ausstehende Daten Bank Anlage erkannt, die Datenbank ist jedoch nicht vorhanden oder entspricht nicht den Informationen zur Anlage.</span><span class="sxs-lookup"><span data-stu-id="1833d-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1833d-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="1833d-865">-1217</span><span class="sxs-lookup"><span data-stu-id="1833d-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="1833d-866">Der angegebene Pfad zur Datenbankdatei ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="1833d-868">-1218</span><span class="sxs-lookup"><span data-stu-id="1833d-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="1833d-869">Einer Datenbank wird eine ID zugewiesen, die bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1833d-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="1833d-871">-1219</span><span class="sxs-lookup"><span data-stu-id="1833d-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="1833d-872">Das Erzwingen von Trenn Einheiten ist nur zulässig, nachdem der normale Trennvorgang aufgrund eines Fehlers beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="1833d-874">-1220</span><span class="sxs-lookup"><span data-stu-id="1833d-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="1833d-875">Im Katalog wurde eine Beschädigung festgestellt.</span><span class="sxs-lookup"><span data-stu-id="1833d-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="1833d-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="1833d-877">-1221</span><span class="sxs-lookup"><span data-stu-id="1833d-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="1833d-878">Die Datenbank ist nur teilweise angefügt, und der Anfüge Vorgang kann nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="1833d-880">-1222</span><span class="sxs-lookup"><span data-stu-id="1833d-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="1833d-881">Die Datenbank mit der gleichen Signatur wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="1833d-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="1833d-883">-1224</span><span class="sxs-lookup"><span data-stu-id="1833d-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="1833d-884">Die Datenbank ist beschädigt, aber eine Reparatur ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="1833d-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="1833d-886">-1225</span><span class="sxs-lookup"><span data-stu-id="1833d-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="1833d-887">Die Datenbank-Engine hat versucht, einen CREATE DATABASE-Vorgang aus dem Transaktionsprotokoll wiederzugeben, konnte jedoch aufgrund einer inkompatiblen Version dieses Vorgangs nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="1833d-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="1833d-889">-1302</span><span class="sxs-lookup"><span data-stu-id="1833d-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="1833d-890">Die Tabelle ist exklusiv gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1833d-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="1833d-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="1833d-892">-1303</span><span class="sxs-lookup"><span data-stu-id="1833d-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="1833d-893">Die Tabelle ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="1833d-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="1833d-895">-1304</span><span class="sxs-lookup"><span data-stu-id="1833d-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="1833d-896">Die Tabelle wird verwendet und kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="1833d-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="1833d-898">-1305</span><span class="sxs-lookup"><span data-stu-id="1833d-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="1833d-899">Eine solche Tabelle oder ein solches Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="1833d-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="1833d-901">-1307</span><span class="sxs-lookup"><span data-stu-id="1833d-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="1833d-902">Es ist eine ungültige Datei-oder Index Dichte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="1833d-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="1833d-904">-1308</span><span class="sxs-lookup"><span data-stu-id="1833d-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="1833d-905">Die Tabelle ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="1833d-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="1833d-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="1833d-907">-1310</span><span class="sxs-lookup"><span data-stu-id="1833d-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="1833d-908">Die Tabellen-ID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="1833d-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="1833d-910">-1311</span><span class="sxs-lookup"><span data-stu-id="1833d-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="1833d-911">Es können keine weiteren Tabellen geöffnet werden, auch nachdem die interne Bereinigungs Aufgabe ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="1833d-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="1833d-913">-1312</span><span class="sxs-lookup"><span data-stu-id="1833d-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="1833d-914">Der Vorgang wird für die Tabelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="1833d-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="1833d-916">-1313</span><span class="sxs-lookup"><span data-stu-id="1833d-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="1833d-917">Es können keine weiteren Tabellen geöffnet werden, da der Cleanupversuch nicht durchgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1833d-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="1833d-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="1833d-919">-1314</span><span class="sxs-lookup"><span data-stu-id="1833d-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="1833d-920">Der Tabellen-oder Objektname wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="1833d-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="1833d-922">-1316</span><span class="sxs-lookup"><span data-stu-id="1833d-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="1833d-923">Das Objekt ist für den Vorgang ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="1833d-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="1833d-925">-1317</span><span class="sxs-lookup"><span data-stu-id="1833d-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="1833d-926"><a href="gg294087(v=exchg.10).md">Jetclosetable</a> muss anstelle von <a href="gg294128(v=exchg.10).md">jetdeletetable</a> verwendet werden, um eine temporäre Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1833d-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="1833d-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="1833d-928">-1318</span><span class="sxs-lookup"><span data-stu-id="1833d-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="1833d-929">Es wurde ein unzulässiger Versuch unternommen, eine Systemtabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1833d-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="1833d-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="1833d-931">-1319</span><span class="sxs-lookup"><span data-stu-id="1833d-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="1833d-932">Es wurde ein unzulässiger Versuch unternommen, eine Vorlagen Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1833d-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="1833d-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="1833d-934">-1322</span><span class="sxs-lookup"><span data-stu-id="1833d-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="1833d-935">Es muss eine exklusive Sperre für die Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1833d-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="1833d-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="1833d-937">-1323</span><span class="sxs-lookup"><span data-stu-id="1833d-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="1833d-938">DDL-Vorgänge sind in dieser Tabelle nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="1833d-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="1833d-940">-1324</span><span class="sxs-lookup"><span data-stu-id="1833d-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="1833d-941">Für eine abgeleitete Tabelle sind DDL-Vorgänge für den geerbten Teil der DDL unzulässig.</span><span class="sxs-lookup"><span data-stu-id="1833d-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="1833d-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="1833d-943">-1325</span><span class="sxs-lookup"><span data-stu-id="1833d-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="1833d-944">Das Schachteln der hierarchischen DDL wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="1833d-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="1833d-946">-1326</span><span class="sxs-lookup"><span data-stu-id="1833d-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="1833d-947">Es wurde versucht, eine DDL von einer Tabelle zu erben, die nicht als Vorlagen Tabelle gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="1833d-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="1833d-949">-1328</span><span class="sxs-lookup"><span data-stu-id="1833d-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="1833d-950">Die Systemparameter wurden nicht ordnungsgemäß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1833d-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="1833d-952">-1329</span><span class="sxs-lookup"><span data-stu-id="1833d-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="1833d-953">Der Client hat angefordert, dass der Dienst beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="1833d-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="1833d-955">-1330</span><span class="sxs-lookup"><span data-stu-id="1833d-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="1833d-956">Die Vorlagen Tabelle wurde erstellt, wobei das nofixedvarcolumnsinderivedtables-Flag festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="1833d-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="1833d-958">-1401</span><span class="sxs-lookup"><span data-stu-id="1833d-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="1833d-959">Der indexbuild ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1833d-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="1833d-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="1833d-961">-1402</span><span class="sxs-lookup"><span data-stu-id="1833d-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="1833d-962">Der primäre Index ist bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="1833d-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="1833d-964">-1403</span><span class="sxs-lookup"><span data-stu-id="1833d-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="1833d-965">Der Index ist bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="1833d-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="1833d-967">-1404</span><span class="sxs-lookup"><span data-stu-id="1833d-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="1833d-968">Es ist kein solcher Index vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="1833d-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="1833d-970">-1405</span><span class="sxs-lookup"><span data-stu-id="1833d-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="1833d-971">Der gruppierte Index kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1833d-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="1833d-973">-1406</span><span class="sxs-lookup"><span data-stu-id="1833d-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="1833d-974">Die Index Definition ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="1833d-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="1833d-976">-1409</span><span class="sxs-lookup"><span data-stu-id="1833d-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="1833d-977">Die Index Beschreibung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="1833d-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="1833d-979">-1410</span><span class="sxs-lookup"><span data-stu-id="1833d-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="1833d-980">Die Datenbank weist keine Index Beschreibungs Blöcke auf.</span><span class="sxs-lookup"><span data-stu-id="1833d-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="1833d-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="1833d-982">-1411</span><span class="sxs-lookup"><span data-stu-id="1833d-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="1833d-983">Für einen mehrwertigen Index wurden nicht eindeutige Index Schlüssel für den zwischen Daten Satz generiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="1833d-985">-1412</span><span class="sxs-lookup"><span data-stu-id="1833d-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="1833d-986">Ein sekundärer Index, der den primären Index korrekt widerspiegelt, konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="1833d-988">-1413</span><span class="sxs-lookup"><span data-stu-id="1833d-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="1833d-989">Der primäre Index ist beschädigt, und die Datenbank muss zerlegt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="1833d-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="1833d-991">-1414</span><span class="sxs-lookup"><span data-stu-id="1833d-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="1833d-992">Der sekundäre Index ist beschädigt, und die Datenbank muss zerlegt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="1833d-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="1833d-994">-1416</span><span class="sxs-lookup"><span data-stu-id="1833d-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="1833d-995">Die Index-ID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="1833d-997">-1430</span><span class="sxs-lookup"><span data-stu-id="1833d-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="1833d-998">Der Tupelindex kann nur für einen sekundären Index festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="1833d-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="1833d-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="1833d-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="1833d-1001">Die Index Definition für den Tupelindex enthält mehr Schlüssel Spalten, die von der Datenbank-Engine unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="1833d-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="1833d-1002"><strong>Hinweis  </strong> Der JET_errIndexTuplesOneColumnOnly Fehler ist veraltet und wurde durch JET_errIndexTuplesTooManyColumns ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="1833d-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="1833d-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="1833d-1005">Der Tupelindex muss ein nicht eindeutiger Index sein.</span><span class="sxs-lookup"><span data-stu-id="1833d-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1833d-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="1833d-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="1833d-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="1833d-1008">Eine tupelindexdefinition kann nur Schlüssel Spalten mit Text-oder Binär Spaltentypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1833d-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="1833d-1009"><strong>Hinweis  </strong> Der JET_errIndexTuplesTextColumnsOnly Fehler ist veraltet und wurde durch JET_errIndexTuplesTextBinaryColumnsOnly ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1833d-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="1833d-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="1833d-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="1833d-1012">Der Tupelindex lässt das Festlegen von cbvarsegmac nicht zu.</span><span class="sxs-lookup"><span data-stu-id="1833d-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="1833d-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="1833d-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="1833d-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="1833d-1015">Die minimale/maximale tupellänge oder die maximale Anzahl von Zeichen, die für einen Index angegeben sind, sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="1833d-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="1833d-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="1833d-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="1833d-1018"><a href="gg269198(v=exchg.10).md">Jetretrievecolenn</a> kann nicht mit dem JET_bitRetrieveFromIndex Flag aufgerufen werden, wenn eine Spalte für einen Tupelindex abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="1833d-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="1833d-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="1833d-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="1833d-1021">Der angegebene Schlüssel entspricht nicht der minimalen tupellänge.</span><span class="sxs-lookup"><span data-stu-id="1833d-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="1833d-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="1833d-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="1833d-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="1833d-1024">Der Spaltenwert ist Long.</span><span class="sxs-lookup"><span data-stu-id="1833d-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="1833d-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="1833d-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="1833d-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="1833d-1027">Es gibt keinen solchen Block in einem Long-Wert.</span><span class="sxs-lookup"><span data-stu-id="1833d-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="1833d-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="1833d-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="1833d-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="1833d-1030">Das Feld passt nicht in den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="1833d-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="1833d-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="1833d-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="1833d-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="1833d-1033">NULL ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="1833d-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="1833d-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="1833d-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="1833d-1036">NULL ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1036">Null is not valid.</span></span> <span data-ttu-id="1833d-1037">Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1833d-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="1833d-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="1833d-1039">Die Spalte ist indiziert und kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="1833d-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="1833d-1041">Die Feldlänge ist größer als die maximal zulässige Länge.</span><span class="sxs-lookup"><span data-stu-id="1833d-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="1833d-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="1833d-1043">Diese Spalte ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="1833d-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="1833d-1045">Dieses Feld ist bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="1833d-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="1833d-1047">Es wurde versucht, eine mehrwertige Spalte zu erstellen, aber die Spalte wurde nicht markiert.</span><span class="sxs-lookup"><span data-stu-id="1833d-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="1833d-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="1833d-1049">Es gab eine zweite Spalte mit automatischer Inkrement oder Version.</span><span class="sxs-lookup"><span data-stu-id="1833d-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="1833d-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="1833d-1051">Der Spaltendatentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="1833d-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="1833d-1053">Es sind keine markierten Spalten ungleich NULL vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="1833d-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="1833d-1055">Die Datenbank ist ungültig, da Sie keinen aktuellen Index enthält.</span><span class="sxs-lookup"><span data-stu-id="1833d-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="1833d-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="1833d-1057">Der Schlüssel wird vollständig erstellt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="1833d-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="1833d-1059">Die Spalten-ID ist falsch.</span><span class="sxs-lookup"><span data-stu-id="1833d-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="1833d-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="1833d-1061">Für die markierte Spalte ist eine ungültige itagsequence vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="1833d-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="1833d-1063">Eine Spalte kann nicht gelöscht werden, da Sie Teil einer Beziehung ist.</span><span class="sxs-lookup"><span data-stu-id="1833d-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="1833d-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="1833d-1065">Das automatische Inkrement und die Version können nicht markiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="1833d-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="1833d-1067">Der Standardwert überschreitet die maximale Größe.</span><span class="sxs-lookup"><span data-stu-id="1833d-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="1833d-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="1833d-1069">Ein doppelter Wert wurde für eine eindeutige mehrwertige Spalte erkannt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="1833d-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="1833d-1071">In einer lange Wert Struktur ist eine Beschädigung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="1833d-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="1833d-1073">Ein doppelter Wert wurde für eine eindeutige mehrwertige Spalte erkannt, nachdem die Daten normalisiert wurden, und Sie normalisiert die Daten vor dem Vergleich.</span><span class="sxs-lookup"><span data-stu-id="1833d-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="1833d-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="1833d-1075">In der abgeleiteten Tabelle ist eine ungültige Spalte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="1833d-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="1833d-1077">Es wurde versucht, eine Spalte in einen primären Index Platzhalter zu konvertieren, aber die Spalte erfüllt nicht die erforderlichen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="1833d-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="1833d-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="1833d-1079">Der Schlüssel wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="1833d-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="1833d-1081">Es ist kein Arbeits Puffer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="1833d-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="1833d-1083">Es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="1833d-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="1833d-1085">Der Primärschlüssel kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="1833d-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="1833d-1087">Es ist ein ungültiger doppelter Schlüssel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="1833d-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="1833d-1089">Es wurde versucht, einen Datensatz zu aktualisieren, während bereits eine Daten Satz Aktualisierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="1833d-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="1833d-1091">Es wurde kein " <a href="gg269329(v=exchg.10).md">jetmakekey</a>" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="1833d-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="1833d-1093">Es wurde kein " <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="1833d-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="1833d-1095">Die Daten wurden geändert, und der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="1833d-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="1833d-1097">Die ausgewählte Sprache wird von dieser Windows-Installation nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="1833d-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="1833d-1099">Es sind zu viele Sortier Prozesse vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="1833d-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="1833d-1101">Beim Sortieren ist ein ungültiger Vorgang aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1833d-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="1833d-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="1833d-1103">Die temporäre Datei konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="1833d-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="1833d-1105">Zu viele Datenbanken sind geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1833d-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="1833d-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="1833d-1107">Auf dem Datenträger ist kein Speicherplatz mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="1833d-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="1833d-1109">Die Berechtigung wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="1833d-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="1833d-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="1833d-1111">Die Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="1833d-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="1833d-1113">Der Dateityp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="1833d-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="1833d-1115">Eine Wiederherstellung kann nach der Initialisierung nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="1833d-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="1833d-1117">Die Protokolle konnten nicht interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="1833d-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="1833d-1119">Der Vorgang ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1833d-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="1833d-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="1833d-1121">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="1833d-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="1833d-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="1833d-1123">Eine unendliche Teilung.</span><span class="sxs-lookup"><span data-stu-id="1833d-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="1833d-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="1833d-1125">Mehrere Threads verwenden dieselbe Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1833d-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="1833d-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="1833d-1127">Ein Einstiegspunkt in einer erforderlichen dll konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="1833d-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="1833d-1129">Für die angegebene Sitzung ist bereits ein Sitzungs Kontext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="1833d-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="1833d-1131">Es wurde versucht, den Sitzungs Kontext zurückzusetzen, aber der aktuelle Thread war nicht der ursprüngliche Thread, der den Sitzungs Kontext festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="1833d-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="1833d-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="1833d-1133">Es wurde versucht, die derzeit verwendete Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="1833d-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="1833d-1135">Interner Fehler bei der Konvertierung von dynamischen Daten Satz Formaten.</span><span class="sxs-lookup"><span data-stu-id="1833d-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="1833d-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="1833d-1137">Pro Sitzung ist nur eine geöffnete Benutzerdatenbank zulässig (wie durch Festlegen des <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> Flags während der Erstellung der Datenbank angegeben).</span><span class="sxs-lookup"><span data-stu-id="1833d-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="1833d-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="1833d-1139">Fehler beim Rollback.</span><span class="sxs-lookup"><span data-stu-id="1833d-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="1833d-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="1833d-1141">Fehler beim Rückruf Funktionsaufrufs.</span><span class="sxs-lookup"><span data-stu-id="1833d-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="1833d-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="1833d-1143">Eine Rückruffunktion wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="1833d-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="1833d-1145">Die schattenkopieapi des Betriebssystems wurde in einer ungültigen Sequenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="1833d-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="1833d-1147">Die Schatten Kopie des Betriebssystems wurde mit einem Timeout beendet.</span><span class="sxs-lookup"><span data-stu-id="1833d-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="1833d-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="1833d-1149">Die Schatten Kopie des Betriebssystems ist nicht zulässig, da eine Sicherung oder Wiederherstellung in ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1833d-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="1833d-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="1833d-1151">Der Vorgang ist fehlgeschlagen, weil das angegebene Schatten Kopie-Handle des Betriebssystems ungültig war.</span><span class="sxs-lookup"><span data-stu-id="1833d-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="1833d-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="1833d-1153">Es wurde versucht, den lokalen Speicher zu verwenden, ohne dass eine Rückruffunktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="1833d-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="1833d-1155">Es wurde versucht, den lokalen Speicher für ein Objekt festzulegen, das bereits festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="1833d-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="1833d-1157">Es wurde versucht, den lokalen Speicher von einem Objekt abzurufen, für das es nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1833d-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="1833d-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="1833d-1159">Bei einem e/a-Vorgang ist ein Fehler aufgetreten, da versucht wurde, einen nicht zugeordneten Bereich einer Datei zu haben.</span><span class="sxs-lookup"><span data-stu-id="1833d-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="1833d-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="1833d-1161">Ein Lesevorgang wurde für einen Speicherort außerhalb der EOF-Anweisung ausgegeben (die Datei wird von den Schreibvorgängen erweitert).</span><span class="sxs-lookup"><span data-stu-id="1833d-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="1833d-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="1833d-1163">Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="1833d-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="1833d-1165">Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Vorgang zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="1833d-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="1833d-1167">Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Fehler zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="1833d-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="1833d-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="1833d-1169">Der Lese-/Schreibzugriff wird für komprimierte Dateien nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1833d-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="1833d-1170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1833d-1170">Remarks</span></span>

<span data-ttu-id="1833d-1171">Im Allgemeinen sollte ein Wert, der größer als 0 (null) ist, als Warnung interpretiert werden. der Wert 0 (null) sollte als Success interpretiert werden, und ein Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1833d-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="1833d-1172">Keine anderen Muster in diesen Werten, z. b. Wertebereiche, sollten von einer Anwendung abhängig sein.</span><span class="sxs-lookup"><span data-stu-id="1833d-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="1833d-1173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1833d-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1174"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1833d-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1833d-1175">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1833d-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1833d-1176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1833d-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1833d-1177">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1833d-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1833d-1178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1833d-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1833d-1179">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1833d-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1833d-1180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1833d-1180">See Also</span></span>

[<span data-ttu-id="1833d-1181">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="1833d-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="1833d-1182">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="1833d-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="1833d-1183">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="1833d-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
