---
description: 'Weitere Informationen finden Sie hier: JET_ERRCAT-Enumeration'
title: JET_ERRCAT-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216308"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="36769-103">JET_ERRCAT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="36769-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="36769-104">Die Fehler Kategorie.</span><span class="sxs-lookup"><span data-stu-id="36769-104">The error category.</span></span> <span data-ttu-id="36769-105">Die Hierarchie lautet wie folgt: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//ungültige e/a-Probleme, möglicherweise nicht vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="36769-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="36769-106">| |--JET_errcatResource | |--JET_errcatMemory//nicht genügend Arbeitsspeicher (alle Varianten) | |--JET_errcatQuota | |--JET_errcatDisk//nicht genügend Speicherplatz (alle Varianten) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//in der Regel aufgrund von Benutzer-mishandeln | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="36769-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="36769-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36769-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="36769-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36769-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36769-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="36769-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="36769-110">Member</span><span class="sxs-lookup"><span data-stu-id="36769-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="36769-111">Membername</span><span class="sxs-lookup"><span data-stu-id="36769-111">Member name</span></span></th>
<th><span data-ttu-id="36769-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36769-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-113">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="36769-113">Unknown</span></span></td>
<td><span data-ttu-id="36769-114">Unbekannte Kategorie.</span><span class="sxs-lookup"><span data-stu-id="36769-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="36769-115">Error</span></span></td>
<td><span data-ttu-id="36769-116">Eine generische Kategorie.</span><span class="sxs-lookup"><span data-stu-id="36769-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-117">Vorgang</span><span class="sxs-lookup"><span data-stu-id="36769-117">Operation</span></span></td>
<td><span data-ttu-id="36769-118">Fehler, die in der Regel aufgrund von unkontrollierbaren Bedingungen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="36769-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="36769-119">Häufig temporär, aber nicht immer.</span><span class="sxs-lookup"><span data-stu-id="36769-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="36769-120">Wiederherstellung: Wiederholen Sie den Vorgang, oder Benachrichtigen Sie den Operator schließlich.</span><span class="sxs-lookup"><span data-stu-id="36769-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-121">FAT</span><span class="sxs-lookup"><span data-stu-id="36769-121">Fatal</span></span></td>
<td><span data-ttu-id="36769-122">Dieser Sortier Fehler tritt nur dann auf, wenn ESE auf eine Fehlerbedingung trifft, die nicht in einer sicheren (häufig transaktionalen) Weise fortgesetzt werden kann, und nicht zu beschädigten Daten, da wir Fehler dieser Kategorie auslösen.</span><span class="sxs-lookup"><span data-stu-id="36769-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="36769-123">Wiederherstellung: Starten Sie die Instanz oder den Prozess neu.</span><span class="sxs-lookup"><span data-stu-id="36769-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="36769-124">Wenn das Problem weiterhin besteht, informieren Sie den-Operator.</span><span class="sxs-lookup"><span data-stu-id="36769-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-125">IO</span><span class="sxs-lookup"><span data-stu-id="36769-125">IO</span></span></td>
<td><span data-ttu-id="36769-126">O-Fehler stammen aus dem Betriebssystem und liegen außerhalb der ESE-Kontrolle. diese Art von Fehler ist möglicherweise temporär, möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="36769-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="36769-127">Wiederherstellung: versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="36769-127">Recovery: Retry.</span></span> <span data-ttu-id="36769-128">Wenn das Problem nicht behoben ist, bitten Sie den Operator um Datenträger.</span><span class="sxs-lookup"><span data-stu-id="36769-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-129">Resource</span><span class="sxs-lookup"><span data-stu-id="36769-129">Resource</span></span></td>
<td><span data-ttu-id="36769-130">Dabei handelt es sich um eine Kategorie, die einen von vielen potenziellen Bedingungen außerhalb der Ressourcen angibt.</span><span class="sxs-lookup"><span data-stu-id="36769-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-131">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="36769-131">Memory</span></span></td>
<td><span data-ttu-id="36769-132">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="36769-132">Classic out of memory condition.</span></span> <span data-ttu-id="36769-133">Wiederherstellung: warten Sie einen Moment, und wiederholen Sie den Vorgang, oder beenden Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="36769-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-134">Kontingent</span><span class="sxs-lookup"><span data-stu-id="36769-134">Quota</span></span></td>
<td><span data-ttu-id="36769-135">Bestimmte &quot; spezialisierte &quot; Ressourcen befinden sich in Pools mit einer bestimmten Größe, sodass Sie Verluste dieser Ressourcen leichter erkennen können.</span><span class="sxs-lookup"><span data-stu-id="36769-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="36769-136">Wiederherstellung: erfordert möglicherweise einige geringfügige Codeänderungen.</span><span class="sxs-lookup"><span data-stu-id="36769-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="36769-137">Die Anwendung sollte über eine Debugaktion (z. b. eine Assert-Aktion) für diese Bedingungen verfügen, um Sie während der Entwicklung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="36769-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="36769-138">Für den Einzelhandels Code empfiehlt es sich, diesen Fehler wie den Fehler der Arbeitsspeicher Kategorie zu behandeln und entweder einen Wiederholungsversuch auszuführen, Arbeitsspeicher freizugeben oder den Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="36769-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-139">Datenträger</span><span class="sxs-lookup"><span data-stu-id="36769-139">Disk</span></span></td>
<td><span data-ttu-id="36769-140">Nicht genügend Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="36769-140">Out of disk conditions.</span></span> <span data-ttu-id="36769-141">Wiederherstellung: Wiederholen Sie den Vorgang später in der Hoffnung, dass mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="36769-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-142">Daten</span><span class="sxs-lookup"><span data-stu-id="36769-142">Data</span></span></td>
<td><span data-ttu-id="36769-143">Ein Daten bezogener Fehler.</span><span class="sxs-lookup"><span data-stu-id="36769-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-144">Bnis</span><span class="sxs-lookup"><span data-stu-id="36769-144">Corruption</span></span></td>
<td><span data-ttu-id="36769-145">Meine Festplatte meine Hausaufgaben.</span><span class="sxs-lookup"><span data-stu-id="36769-145">My hard drive ate my homework.</span></span> <span data-ttu-id="36769-146">Klassische Beschädigungs Probleme, häufig permanent ohne Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="36769-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="36769-147">Wiederherstellung: Stellen Sie eine Wiederherstellung von einer Sicherung wieder her, u. u. den ESE-Hilfsprogramme-Reparaturvorgang (der nur die verbleibenden und verlustfreien Daten Im Fall einer Wiederherstellung kann eine Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="36769-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-148">Einheitlich</span><span class="sxs-lookup"><span data-stu-id="36769-148">Inconsistent</span></span></td>
<td><span data-ttu-id="36769-149">Dies ähnelt der Beschädigung, dass sich die Datenbank und/oder die Protokolldateien in einem Zustand befinden, der inkonsistent ist und nicht miteinander zu vereinbaren ist.</span><span class="sxs-lookup"><span data-stu-id="36769-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="36769-150">Dies wird häufig durch eine Anwendungs-/administratormishandelung verursacht.</span><span class="sxs-lookup"><span data-stu-id="36769-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="36769-151">Wiederherstellung: Stellen Sie eine Wiederherstellung von einer Sicherung wieder her, u. u. den ESE-Hilfsprogramme-Reparaturvorgang (der nur die verbleibenden und verlustfreien Daten</span><span class="sxs-lookup"><span data-stu-id="36769-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="36769-152">Im Fall einer Wiederherstellung kann eine Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="36769-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-153">Fragmentierung</span><span class="sxs-lookup"><span data-stu-id="36769-153">Fragmentation</span></span></td>
<td><span data-ttu-id="36769-154">Dabei handelt es sich um eine Klasse von Fehlern, bei denen einige persistente interne Ressourcen abgelaufen sind. Wiederherstellung: bei Daten Bank Fehlern wird das Problem durch die Offline Defragmentierung behoben, und für die Protokolldateien werden _zuerst_ alle angefügten Datenbanken in einem fehlerfreien Herunterfahren wieder hergestellt. Anschließend werden alle Protokolldateien und Prüfpunkte gelöscht.</span><span class="sxs-lookup"><span data-stu-id="36769-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-155">Found</span><span class="sxs-lookup"><span data-stu-id="36769-155">Api</span></span></td>
<td><span data-ttu-id="36769-156">Ein Container für die Verwendung und den Status.</span><span class="sxs-lookup"><span data-stu-id="36769-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-157">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="36769-157">Usage</span></span></td>
<td><span data-ttu-id="36769-158">Klassischer Verwendungs Fehler. Dies bedeutet, dass der Client Code keine korrekten Argumente an die Jet-API übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="36769-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="36769-159">Dieser Fehler wird bei einem Wiederholungsversuch wahrscheinlich nicht fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="36769-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="36769-160">Wiederherstellung: im Allgemeinen sollte der Client Code Assert () diese Fehler Klasse wird nicht zurückgegeben, sodass Probleme während der Entwicklung abgefangen werden können.</span><span class="sxs-lookup"><span data-stu-id="36769-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="36769-161">Im Einzelhandel hat die APP wahrscheinlich nur wenig Optionen, aber das Problem an den Operator zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="36769-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-162">State</span><span class="sxs-lookup"><span data-stu-id="36769-162">State</span></span></td>
<td><span data-ttu-id="36769-163">Dies ist die Klassifizierung für verschiedene Signale, die die API zurückgeben könnte, die den Status der Datenbank beschreiben. ein klassischer Fall ist JET_errRecordNotFound, der von JetSeek () zurückgegeben werden kann, wenn der von Ihnen angeforderte Datensatz nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="36769-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="36769-164">Wiederherstellung: nicht wirklich relevant, hängt stark von der API ab.</span><span class="sxs-lookup"><span data-stu-id="36769-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="36769-165">Veraltet</span><span class="sxs-lookup"><span data-stu-id="36769-165">Obsolete</span></span></td>
<td><span data-ttu-id="36769-166">Der Fehler wird als gültiger Fehler erkannt, es wird jedoch davon ausgegangen, dass er von dieser Version der API nicht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="36769-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="36769-167">Max.</span><span class="sxs-lookup"><span data-stu-id="36769-167">Max</span></span></td>
<td><span data-ttu-id="36769-168">Der Höchstwert für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="36769-168">The maximum value for the enum.</span></span> <span data-ttu-id="36769-169">Dies sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36769-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="36769-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36769-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36769-171">Referenz</span><span class="sxs-lookup"><span data-stu-id="36769-171">Reference</span></span>

[<span data-ttu-id="36769-172">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="36769-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
