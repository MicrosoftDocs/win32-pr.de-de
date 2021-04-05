---
description: 'Weitere Informationen zu: I/O-Parametern'
title: I/O-Parameter
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753985"
---
# <a name="io-parameters"></a><span data-ttu-id="a9343-103">I/O-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9343-103">I/O Parameters</span></span>


<span data-ttu-id="a9343-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a9343-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="a9343-105">I/O-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9343-105">I/O Parameters</span></span>

<span data-ttu-id="a9343-106">Dieses Thema enthält Parameter, die für die Eingabe und Ausgabe (e/a) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9343-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="a9343-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="a9343-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="a9343-108">53</span><span class="sxs-lookup"><span data-stu-id="a9343-108">53</span></span>  

<span data-ttu-id="a9343-109">**Windows XP und höher:**  Dieser Parameter konfiguriert die Dauer (in Millisekunden), die von der Datenbank-Engine für den Zugriff auf eine gesperrte Datei verwendet wird, bevor ein Fehler mit Jet_errFileAccessDenied auftritt.</span><span class="sxs-lookup"><span data-stu-id="a9343-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="a9343-110">Diese Zeitverzögerung ist so konzipiert, dass Antivirensoftware verwendet wird, die möglicherweise einige der Dateien der Datenbank-Engine kurz nach dem Schließen offen hält.</span><span class="sxs-lookup"><span data-stu-id="a9343-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="a9343-111">**Hinweis**  Aufgrund der obigen Wiederholungs Logik führt jeder Versuch, eine Datenbank anzufügen oder eine Protokolldatei zu verwenden, die bereits von der Datenbank-Engine verwendet wird, zu einer Verzögerung dieser Größe, bevor der API-Rückruf einen (legitimen) Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a9343-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="a9343-112">Dieser Parameter kann verwendet werden, um diese Verzögerung zu deaktivieren, falls es sich hierbei um ein häufiges Szenario handelt.</span><span class="sxs-lookup"><span data-stu-id="a9343-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-113">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-114">10000</span><span class="sxs-lookup"><span data-stu-id="a9343-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-115">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-116">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-117">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-118">0 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="a9343-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-119">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-120">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-121">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-122">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-123">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-124">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-125">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-126">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-127">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-128">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-129">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-130">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-131">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-132">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-133">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-134">Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="a9343-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="a9343-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="a9343-136">100</span><span class="sxs-lookup"><span data-stu-id="a9343-136">100</span></span>  

<span data-ttu-id="a9343-137">Wenn dieser Parameter auf true festgelegt ist, wird jeder Ordner, der in einem Dateisystempfad fehlt, der von der Datenbank-Engine verwendet wird, automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9343-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="a9343-138">Andernfalls schlägt der Vorgang, der den fehlenden Dateisystempfad verwendet, mit Jet_errInvalidPath fehl.</span><span class="sxs-lookup"><span data-stu-id="a9343-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-139">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-140">False</span><span class="sxs-lookup"><span data-stu-id="a9343-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-141">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="a9343-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-143">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-144">False, True</span><span class="sxs-lookup"><span data-stu-id="a9343-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-145">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-146">Instanz</span><span class="sxs-lookup"><span data-stu-id="a9343-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-147">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-148">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-149">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-150">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-151">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-152">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-153">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-154">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-155">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-156">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-157">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-158">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-159">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-160">Alle</span><span class="sxs-lookup"><span data-stu-id="a9343-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="a9343-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="a9343-162">126</span><span class="sxs-lookup"><span data-stu-id="a9343-162">126</span></span>  

<span data-ttu-id="a9343-163">Wenn dieser Parameter **true** ist, verwendet die Datenbank-Engine den Windows-Dateicache als Lese Cache für alle verschiedenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="a9343-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="a9343-164">Sie wird auch als Schreib Cache für die temporäre Datenbank oder für Datenbanken verwendet, die mit deaktivierter Wiederherstellung geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="a9343-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="a9343-165">Die Datenbank-Engine muss das Schreiben Zwischenspeichern für normale Datenbanken, Transaktionsprotokoll Dateien und Prüf Punkt Dateien deaktivieren, um die Transaktions Integrität der Datenbanken zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a9343-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="a9343-166">Beachten Sie, dass durch die Verwendung des Windows-Datei Caches eine zweite Schicht der Zwischenspeicherung für Datenbankdateien hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a9343-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="a9343-167">Der Daten Bank Cache verwendet weiterhin seinen eigenen Arbeitsspeicher, um die Datenbankdateien zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="a9343-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="a9343-168">Der Zweck dieses Modus besteht darin, die Anwendung zu ermöglichen, die Datenbank-Engine mit einem kleinen dedizierten Cache zu konfigurieren und Windows das Spenden von Speicherplatz zu ermöglichen, um das Zwischenspeichern von Datenbankdaten weiter zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a9343-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-169">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-170">False</span><span class="sxs-lookup"><span data-stu-id="a9343-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-171">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="a9343-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-173">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-174">False, True</span><span class="sxs-lookup"><span data-stu-id="a9343-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-175">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-176">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-177">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-178">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-179">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-180">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-181">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-182">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-183">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-184">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-185">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-186">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-187">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-188">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-189">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-190">Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="a9343-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="a9343-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="a9343-192">152</span><span class="sxs-lookup"><span data-stu-id="a9343-192">152</span></span>  

<span data-ttu-id="a9343-193">Dieser Parameter steuert, wie ESE e/a-Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="a9343-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="a9343-194">Die Werte können auf 0 (JET_IOPriorityNormal) für den normalen Betrieb oder 1 (JET_IOPriorityLow) für einen Vorgang mit niedriger Priorität festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9343-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="a9343-195">Wenn die Priorität auf JET_IOPriorityLow festgelegt ist, verwendet ESE die neue, in Windows Vista verfügbare Thread-e/a-Prioritäts Funktion, um die e/a-Priorität für den Thread zu verringern, sodass nachfolgende e/a-Vorgänge mit der neuen niedrigen Priorität ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9343-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="a9343-196">**Windows Vista:**  JET_paramIOPriority wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a9343-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-197">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-198">0</span><span class="sxs-lookup"><span data-stu-id="a9343-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-199">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-200">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-201">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="a9343-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-203">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-204">Instanz</span><span class="sxs-lookup"><span data-stu-id="a9343-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-205">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-206">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-207">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-208">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-209">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-210">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-211">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-212">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-213">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-214">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-215">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-216">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-217">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9343-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="a9343-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="a9343-220">30</span><span class="sxs-lookup"><span data-stu-id="a9343-220">30</span></span> 

<span data-ttu-id="a9343-221">Mit diesem Parameter wird gesteuert, wie viele Datenbankdatei-e/a-Vorgängen im Host Betriebssystem gleichzeitig in eine Warteschlange gestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="a9343-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="a9343-222">Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a9343-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="a9343-223">**Windows XP und Windows Server 2003:**  Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="a9343-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-224">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-225"><strong>Windows 2000: </strong>  64</span><span class="sxs-lookup"><span data-stu-id="a9343-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="a9343-226"><strong>Windows Vista:</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="a9343-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-227">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-228">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-229">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-230"><strong>Windows 2000:</strong>  8 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="a9343-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="a9343-231"><strong>Windows Vista:</strong>  0 – 65536</span><span class="sxs-lookup"><span data-stu-id="a9343-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-232">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-233">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-234">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-235">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-236">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-237">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-238">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-239">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-240">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-241">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-242">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-243">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-244">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-245">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-246">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-247">Alle</span><span class="sxs-lookup"><span data-stu-id="a9343-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="a9343-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="a9343-249">164</span><span class="sxs-lookup"><span data-stu-id="a9343-249">164</span></span>  

<span data-ttu-id="a9343-250">Maximale Anzahl von Bytes, die nach einem zusammengefügten Lesevorgang gruppiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9343-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-251">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-252">262144</span><span class="sxs-lookup"><span data-stu-id="a9343-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-253">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-254">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-255">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a9343-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-257">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-258">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-259">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-260">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-261">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-262">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-263">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-264">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-265">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-266">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-267">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-268">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-269">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-270">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-271">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9343-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="a9343-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="a9343-274">165</span><span class="sxs-lookup"><span data-stu-id="a9343-274">165</span></span>  

<span data-ttu-id="a9343-275">Maximale Anzahl von Bytes, die für einen zusammengefügten Schreibvorgang gruppiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9343-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-276">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-277">393216</span><span class="sxs-lookup"><span data-stu-id="a9343-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-278">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-279">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-280">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a9343-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-282">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-283">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-284">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-285">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-286">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-287">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-288">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-289">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-290">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-291">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-292">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-293">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-294">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-295">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-296">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9343-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="a9343-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="a9343-299">166</span><span class="sxs-lookup"><span data-stu-id="a9343-299">166</span></span>  

<span data-ttu-id="a9343-300">Maximale Anzahl von Bytes, die für einen zusammengefügten Schreib-e/a-Vorgang geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9343-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-301">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-302">262144</span><span class="sxs-lookup"><span data-stu-id="a9343-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-303">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-304">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-305">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a9343-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-307">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-308">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-309">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-310">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-311">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-312">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-313">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-314">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-315">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-316">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-317">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-318">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-319">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-320">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-321">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9343-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9343-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="a9343-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="a9343-324">167</span><span class="sxs-lookup"><span data-stu-id="a9343-324">167</span></span>  

<span data-ttu-id="a9343-325">Maximale Anzahl von Bytes, die für einen zusammengefügten Lese-e/a-Vorgang geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9343-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-326">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="a9343-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a9343-327">393216</span><span class="sxs-lookup"><span data-stu-id="a9343-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-328">Typ:</span><span class="sxs-lookup"><span data-stu-id="a9343-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="a9343-329">Integer</span><span class="sxs-lookup"><span data-stu-id="a9343-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-330">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9343-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a9343-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a9343-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-332">Umfang:</span><span class="sxs-lookup"><span data-stu-id="a9343-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a9343-333">Global</span><span class="sxs-lookup"><span data-stu-id="a9343-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-334">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-335">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-336">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9343-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a9343-337">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-338">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="a9343-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a9343-339">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-340">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-341">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-342">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="a9343-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a9343-343">Ja</span><span class="sxs-lookup"><span data-stu-id="a9343-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-344">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="a9343-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a9343-345">Nein</span><span class="sxs-lookup"><span data-stu-id="a9343-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-346">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="a9343-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a9343-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9343-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a9343-348">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9343-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9343-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a9343-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a9343-350">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a9343-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9343-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a9343-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a9343-352">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a9343-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9343-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a9343-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a9343-354">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a9343-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a9343-355">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9343-355">See Also</span></span>

[<span data-ttu-id="a9343-356">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="a9343-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a9343-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="a9343-357">JetInit</span></span>](./jetinit-function.md)
