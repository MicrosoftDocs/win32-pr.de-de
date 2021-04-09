---
description: 'Weitere Informationen: Ereignisprotokoll Parameter'
title: Ereignisprotokoll Parameter
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042443"
---
# <a name="event-log-parameters"></a><span data-ttu-id="2f30d-103">Ereignisprotokoll Parameter</span><span class="sxs-lookup"><span data-stu-id="2f30d-103">Event Log Parameters</span></span>


<span data-ttu-id="2f30d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f30d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="2f30d-105">Ereignisprotokoll Parameter</span><span class="sxs-lookup"><span data-stu-id="2f30d-105">Event Log Parameters</span></span>

<span data-ttu-id="2f30d-106">Dieses Thema enthält Parameter, die für das Ereignisprotokoll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f30d-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="2f30d-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="2f30d-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="2f30d-108">Dieser Parameter steuert die Größe (in Bytes) eines EventLog-Nachrichten Caches, der Ereignisprotokoll Meldungen enthält, die von der Datenbank-Engine ausgegeben werden, während der EventLog-Dienst beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f30d-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="2f30d-109">Diese zwischengespeicherten Nachrichten werden in das Ereignisprotokoll geleert, wenn der Dienst betriebsbereit ist.</span><span class="sxs-lookup"><span data-stu-id="2f30d-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="2f30d-110">Alle Nachrichten, die den Cache überlaufen, werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2f30d-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-111">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="2f30d-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-112">0</span><span class="sxs-lookup"><span data-stu-id="2f30d-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="2f30d-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-114">Integer</span><span class="sxs-lookup"><span data-stu-id="2f30d-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-115">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f30d-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-116">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="2f30d-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-117">Umfang:</span><span class="sxs-lookup"><span data-stu-id="2f30d-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-118">Global</span><span class="sxs-lookup"><span data-stu-id="2f30d-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-119">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-120">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-121">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-122">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-123">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="2f30d-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-124">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-125">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-126">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-127">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="2f30d-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-128">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-129">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-130">Ja</span><span class="sxs-lookup"><span data-stu-id="2f30d-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-131">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-132">Alle</span><span class="sxs-lookup"><span data-stu-id="2f30d-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f30d-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="2f30d-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="2f30d-134">Dieser Parameter konfiguriert die Detailebene von EventLog-Nachrichten, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f30d-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="2f30d-135">Höhere Zahlen führen zu ausführlicheren Ereignisprotokoll Meldungen.</span><span class="sxs-lookup"><span data-stu-id="2f30d-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-136">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="2f30d-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="2f30d-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-138">Typ:</span><span class="sxs-lookup"><span data-stu-id="2f30d-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-139">Integer</span><span class="sxs-lookup"><span data-stu-id="2f30d-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-140">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f30d-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="2f30d-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-142">Umfang:</span><span class="sxs-lookup"><span data-stu-id="2f30d-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-143">Instanz</span><span class="sxs-lookup"><span data-stu-id="2f30d-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-144">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-145">Ja</span><span class="sxs-lookup"><span data-stu-id="2f30d-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-146">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-147">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-148">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="2f30d-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-149">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-150">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-151">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-152">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="2f30d-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-153">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-154">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-155">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-156">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-157">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="2f30d-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f30d-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="2f30d-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="2f30d-159">4</span><span class="sxs-lookup"><span data-stu-id="2f30d-159">4</span></span>  

<span data-ttu-id="2f30d-160">Dieser Parameter stellt eine anwendungsspezifische Zeichenfolge bereit, die allen Ereignisprotokoll Meldungen hinzugefügt wird, die von der Datenbank-Engine ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f30d-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="2f30d-161">Dies ermöglicht eine einfache Korrelation von Ereignisprotokoll Meldungen mit der Quell Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2f30d-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="2f30d-162">Wenn eine leere Zeichenfolge (wie die Standardeinstellung) angegeben wird, wird der Name der ausführbaren Datei der Host Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f30d-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-163">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="2f30d-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-164">Typ:</span><span class="sxs-lookup"><span data-stu-id="2f30d-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-165">String</span><span class="sxs-lookup"><span data-stu-id="2f30d-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-166">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f30d-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-167">0 – 259 Zeichen</span><span class="sxs-lookup"><span data-stu-id="2f30d-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-168">Umfang:</span><span class="sxs-lookup"><span data-stu-id="2f30d-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-169">Instanz</span><span class="sxs-lookup"><span data-stu-id="2f30d-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-170">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-171">Ja</span><span class="sxs-lookup"><span data-stu-id="2f30d-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-172">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-173">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-174">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="2f30d-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-175">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-176">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-177">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-178">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="2f30d-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-179">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-180">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-181">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-182">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-183">Alle</span><span class="sxs-lookup"><span data-stu-id="2f30d-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f30d-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="2f30d-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="2f30d-185">49</span><span class="sxs-lookup"><span data-stu-id="2f30d-185">49</span></span>  

<span data-ttu-id="2f30d-186">Dieser Parameter kann verwendet werden, um zu steuern, welches Ereignisprotokoll die Datenbank-Engine für die Ereignisprotokoll Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f30d-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="2f30d-187">Standardmäßig werden alle Ereignisprotokoll Meldungen an das Anwendungs Ereignisprotokoll gesendet.</span><span class="sxs-lookup"><span data-stu-id="2f30d-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="2f30d-188">Wenn der Registrierungsschlüssel Name für ein anderes Ereignisprotokoll konfiguriert ist, werden stattdessen die Ereignisprotokoll Meldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f30d-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-189">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="2f30d-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-190">Typ:</span><span class="sxs-lookup"><span data-stu-id="2f30d-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-191">String</span><span class="sxs-lookup"><span data-stu-id="2f30d-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-192">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f30d-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-193">0 – 259 Zeichen</span><span class="sxs-lookup"><span data-stu-id="2f30d-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-194">Umfang:</span><span class="sxs-lookup"><span data-stu-id="2f30d-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-195">Instanz</span><span class="sxs-lookup"><span data-stu-id="2f30d-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-196">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-197">Ja</span><span class="sxs-lookup"><span data-stu-id="2f30d-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-198">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-199">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-200">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="2f30d-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-201">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-202">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-203">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-204">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="2f30d-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-205">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-206">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-207">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-208">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-209">Alle</span><span class="sxs-lookup"><span data-stu-id="2f30d-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f30d-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="2f30d-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="2f30d-211">50</span><span class="sxs-lookup"><span data-stu-id="2f30d-211">50</span></span>  

<span data-ttu-id="2f30d-212">Wenn dieser Parameter true ist, werden Informations Ereignisprotokoll Meldungen, die normalerweise von der Datenbank-Engine generiert werden, unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="2f30d-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-213">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="2f30d-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-214">False</span><span class="sxs-lookup"><span data-stu-id="2f30d-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-215">Typ:</span><span class="sxs-lookup"><span data-stu-id="2f30d-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="2f30d-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-217">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f30d-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-218">False, True</span><span class="sxs-lookup"><span data-stu-id="2f30d-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-219">Umfang:</span><span class="sxs-lookup"><span data-stu-id="2f30d-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-220">Instanz</span><span class="sxs-lookup"><span data-stu-id="2f30d-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-221">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-222">Ja</span><span class="sxs-lookup"><span data-stu-id="2f30d-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-223">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-224">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-225">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="2f30d-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-226">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-227">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-228">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-229">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="2f30d-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-230">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-231">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="2f30d-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-232">Nein</span><span class="sxs-lookup"><span data-stu-id="2f30d-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-233">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="2f30d-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2f30d-234">Alle</span><span class="sxs-lookup"><span data-stu-id="2f30d-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="2f30d-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f30d-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-236"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2f30d-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f30d-237">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2f30d-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f30d-238"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2f30d-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f30d-239">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2f30d-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f30d-240"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2f30d-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f30d-241">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="2f30d-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2f30d-242">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f30d-242">See Also</span></span>

[<span data-ttu-id="2f30d-243">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="2f30d-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="2f30d-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="2f30d-244">JetInit</span></span>](./jetinit-function.md)
