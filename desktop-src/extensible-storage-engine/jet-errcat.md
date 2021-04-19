---
description: 'Weitere Informationen finden Sie hier: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350267"
---
# <a name="jet_errcat"></a><span data-ttu-id="81c56-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="81c56-103">JET_ERRCAT</span></span>


<span data-ttu-id="81c56-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="81c56-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="81c56-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="81c56-105">JET_ERRCAT</span></span>

<span data-ttu-id="81c56-106">Die **JET_ERRCAT** Gruppe von Konstanten beschreibt Klassifizierungen oder Kategorien von Fehlern auf höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="81c56-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="81c56-107">Diese Gruppe von Konstanten ermöglicht Anwendungen, die Standardbehandlung für eine Klassifizierung von Fehlern zu definieren, anstatt jeden einzelnen Fehlerfall einzeln zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="81c56-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="81c56-108">Außerdem wird sichergestellt, dass die Anwendung keine neuen Fehlerbedingungen behandelt, die in vorhandenen Klassifizierungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="81c56-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="81c56-109">Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine.</span><span class="sxs-lookup"><span data-stu-id="81c56-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="81c56-110">Diese Informationen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="81c56-110">This information is subject to change.</span></span>

<span data-ttu-id="81c56-111">Die **JET_ERRCAT** Konstanten werden wie folgt in einer bestimmten Hierarchie von Bedingungen und unter Bedingungen angeordnet:</span><span class="sxs-lookup"><span data-stu-id="81c56-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="81c56-112">|---Fehler |---Vorgang (Al) | |---schwerwiegend | |---IO | |---Ressource | |---Speicher | |---Kontingent | |---Datenträger | |---Daten | |---Beschädigung | |---inkonsistent | |---Fragmentierung | |---API |---Verwendung |---Status</span><span class="sxs-lookup"><span data-stu-id="81c56-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="81c56-113">In der folgenden Tabelle sind die **JET_ERRCAT** Konstanten aufgelistet, und es werden ggf. eine Beschreibung und Wiederherstellungs Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="81c56-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81c56-114">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="81c56-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="81c56-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81c56-115">Description</span></span></p></th>
<th><p><span data-ttu-id="81c56-116">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="81c56-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81c56-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="81c56-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="81c56-118">Ungültige Fehler Kategorie.</span><span class="sxs-lookup"><span data-stu-id="81c56-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="81c56-119">N/V.</span><span class="sxs-lookup"><span data-stu-id="81c56-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="81c56-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="81c56-121">Die Kategorie der obersten Ebene (keine Fehler sollten dieser Klasse unterliegen).</span><span class="sxs-lookup"><span data-stu-id="81c56-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="81c56-122">Weitere Informationen finden Sie unter den spezifischen Fehler Konstanten.</span><span class="sxs-lookup"><span data-stu-id="81c56-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="81c56-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="81c56-124">Stellt Fehler dar, die zu einem beliebigen Zeitpunkt aufgrund von unkontrollierbaren Bedingungen auftreten können und oft temporär sind.</span><span class="sxs-lookup"><span data-stu-id="81c56-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="81c56-125">Siehe Unterkategorien, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="81c56-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="81c56-126">Versuchen Sie es erneut, und informieren Sie den Operator, wenn der Fehler weiterhin auftritt.</span><span class="sxs-lookup"><span data-stu-id="81c56-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="81c56-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="81c56-128">Stellt schwerwiegende Fehler dar, die auftreten, wenn Sie auftreten, riskieren, dass ESE nicht in einer sicheren (häufig transaktionalen) Weise fortgesetzt werden kann und dass die Daten beschädigt werden können.</span><span class="sxs-lookup"><span data-stu-id="81c56-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="81c56-129">Starten Sie die Instanz oder den Prozess neu.</span><span class="sxs-lookup"><span data-stu-id="81c56-129">Restart the instance or process.</span></span> <span data-ttu-id="81c56-130">Wenn das Problem weiterhin besteht, informieren Sie den Operator.</span><span class="sxs-lookup"><span data-stu-id="81c56-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="81c56-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="81c56-132">Stellt e/a-Fehler dar, die vom Betriebssystem stammen und aus der ESE-Kontrolle bestehen.</span><span class="sxs-lookup"><span data-stu-id="81c56-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="81c56-133">Diese Art von Fehler kann temporär sein.</span><span class="sxs-lookup"><span data-stu-id="81c56-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="81c56-134">Versuchen Sie es erneut. wenn der Fehler weiterhin auftritt, bitten Sie den Operator, den Datenträger zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="81c56-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="81c56-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="81c56-136">Stellt eine Kategorie von Fehlern im Zusammenhang mit dem Mangel an Ressourcen Bedingungen dar.</span><span class="sxs-lookup"><span data-stu-id="81c56-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="81c56-137">Siehe Unterkategorien.</span><span class="sxs-lookup"><span data-stu-id="81c56-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="81c56-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="81c56-139">Stellt einen Fehler dar, der durch unzureichenden Arbeitsspeicher verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="81c56-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="81c56-140">Wiederholen Sie den Vorgang nach einer gewissen Zeit, geben Sie Arbeitsspeicher frei, oder beenden Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="81c56-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="81c56-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="81c56-142">Bestimmte &quot; spezialisierte &quot; Ressourcen befinden sich in Pools mit einer bestimmten Größe, sodass Sie Verluste dieser Ressourcen leichter erkennen können.</span><span class="sxs-lookup"><span data-stu-id="81c56-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="81c56-143">Die Anwendung sollte <strong>()</strong> bestätigen, um diese Probleme während der Entwicklung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="81c56-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="81c56-144">Im Einzelhandels Code sollte die Anwendung dies jedoch als Speicherfehler behandeln.</span><span class="sxs-lookup"><span data-stu-id="81c56-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="81c56-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="81c56-146">Stellt einen Fehler dar, der durch unzureichenden Speicherplatz verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="81c56-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="81c56-147">Versuchen Sie es später erneut, um zu ermitteln, ob mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="81c56-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="81c56-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="81c56-149">Stellt eine Kategorie der obersten Ebene für Fehler im Zusammenhang mit Daten dar.</span><span class="sxs-lookup"><span data-stu-id="81c56-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="81c56-150">Siehe Unterkategorien.</span><span class="sxs-lookup"><span data-stu-id="81c56-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="81c56-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="81c56-152">Stellt ein Beschädigungs Problem dar, das häufig ohne Korrekturmaßnahmen permanent ist.</span><span class="sxs-lookup"><span data-stu-id="81c56-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="81c56-153">Stellen Sie die Sicherung mithilfe des Reparatur Vorgangs für ESE-Hilfsprogramme wieder her (mit diesem Vorgang werden nur die Daten wieder hergestellt, die nach links/Verlust liegen).</span><span class="sxs-lookup"><span data-stu-id="81c56-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="81c56-154">Außerdem kann die Wiederherstellung durchgeführt werden, wenn die Wiederherstellungsmethode (jetinit) verwendet wird, um Datenverluste zuzulassen (Weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="81c56-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="81c56-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="81c56-156">Stellt einen Fehler dar, in dem sich die Datenbank und/oder die Protokolldateien in einem inkonsistenten Zustand befinden und nicht abgeglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="81c56-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="81c56-157">Dieser Fehler kann durch eine Anwendungs-/administratormishandelung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="81c56-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="81c56-158">Stellen Sie eine Wiederherstellung von einer Sicherung mit dem ESE-Hilfsprogramm-Reparaturvorgang durch</span><span class="sxs-lookup"><span data-stu-id="81c56-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="81c56-159">Im Fall des <strong>Wiederherstellungs Vorgangs (jetinit)</strong> kann die Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden. (Weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="81c56-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="81c56-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="81c56-161">Stellt eine Klasse von Fehlern dar, in denen einige beibehaltene interne Ressourcen aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="81c56-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="81c56-162">Bei Daten Bank Fehlern kann das Problem durch die Offline Defragmentierung behoben werden.</span><span class="sxs-lookup"><span data-stu-id="81c56-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="81c56-163">Stellen Sie für die Protokolldateien zunächst alle angefügten Datenbanken in einem sauberen Herunterfahren wieder her, und löschen Sie dann alle Protokolldateien und den Prüfpunkt.</span><span class="sxs-lookup"><span data-stu-id="81c56-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="81c56-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="81c56-165">Siehe Unterkategorien.</span><span class="sxs-lookup"><span data-stu-id="81c56-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="81c56-166">Siehe Unterkategorien.</span><span class="sxs-lookup"><span data-stu-id="81c56-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="81c56-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="81c56-168">Stellt einen Verwendungs Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="81c56-168">Represents a usage error.</span></span> <span data-ttu-id="81c56-169">Der Client Code hat nicht die richtigen Argumente an die <strong>Jet</strong> -API übergeben.</span><span class="sxs-lookup"><span data-stu-id="81c56-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="81c56-170">Dieser Fehler wird bei einem Wiederholungsversuch beibehalten.</span><span class="sxs-lookup"><span data-stu-id="81c56-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="81c56-171">Der Client Code sollte die <strong>Assert ()</strong> -Methode verwenden, um sicherzustellen, dass diese Fehler Klasse nicht zurückgegeben wird, sodass Probleme während der Entwicklung abgefangen werden können.</span><span class="sxs-lookup"><span data-stu-id="81c56-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="81c56-172">Im Einzelhandel sollte die Anwendung den Operator über den Fehler benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="81c56-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="81c56-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="81c56-174">Stellt eine Klasse von Nachrichten dar, die von der API zurückgegeben werden können, um den Status der Datenbank zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="81c56-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="81c56-175">Beispielsweise kann die <a href="gg294103(v=exchg.10).md">JetSeek ()</a> -Methode <strong>JET_errRecordNotFound</strong> zurückgeben, wenn der angeforderte Datensatz nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="81c56-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="81c56-176">Variiert je nach API.</span><span class="sxs-lookup"><span data-stu-id="81c56-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="81c56-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="81c56-178">Stellt Fehler dar, die von einer früheren Version der-Engine stammen.</span><span class="sxs-lookup"><span data-stu-id="81c56-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="81c56-179">Diese Fehler sollten nicht von der aktuellen Engine zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81c56-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="81c56-180">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="81c56-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="81c56-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="81c56-182">Eine-Konstante, die das Ende der-Enumeration angibt.</span><span class="sxs-lookup"><span data-stu-id="81c56-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="81c56-183">N/V.</span><span class="sxs-lookup"><span data-stu-id="81c56-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="81c56-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81c56-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81c56-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="81c56-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="81c56-186">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="81c56-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81c56-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="81c56-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="81c56-188">Erfordert Windows 8-Server.</span><span class="sxs-lookup"><span data-stu-id="81c56-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81c56-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="81c56-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="81c56-190">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="81c56-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

