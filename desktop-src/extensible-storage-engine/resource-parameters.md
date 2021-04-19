---
description: 'Weitere Informationen zu: Ressourcen Parametern'
title: Ressourcenparameter
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362517"
---
# <a name="resource-parameters"></a><span data-ttu-id="3a870-103">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="3a870-103">Resource Parameters</span></span>


<span data-ttu-id="3a870-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3a870-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="3a870-105">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="3a870-105">Resource Parameters</span></span>

<span data-ttu-id="3a870-106">Dieses Thema enthält Parameter, die für Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="3a870-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="3a870-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="3a870-108">125</span><span class="sxs-lookup"><span data-stu-id="3a870-108">125</span></span>  

<span data-ttu-id="3a870-109">Dieser Parameter steuert die Anzahl der B +-strukturressourcen, die von der-Instanz zwischengespeichert wurden, nachdem die Tabellen, die Sie darstellen, von der Anwendung geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="3a870-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="3a870-110">Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a870-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="3a870-111">Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a870-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-112">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-113">64</span><span class="sxs-lookup"><span data-stu-id="3a870-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-114">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-115">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-116">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-117">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-118">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-119">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-120">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-121">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-122">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-123">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-124">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-125">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-126">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-127">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-128">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-129">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-130">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-131">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-132">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-133">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="3a870-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="3a870-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="3a870-135">107</span><span class="sxs-lookup"><span data-stu-id="3a870-135">107</span></span>  

<span data-ttu-id="3a870-136">Dieser Parameter kann verwendet werden, um zu verhindern, dass die Datenbank-Engine Daten über seine Leistung in Windows veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3a870-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="3a870-137">Dies kann erreicht werden, um die Dienst Thread Aktivität der Datenbank-Engine zu verringern.</span><span class="sxs-lookup"><span data-stu-id="3a870-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-138">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-139">False</span><span class="sxs-lookup"><span data-stu-id="3a870-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-140">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="3a870-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-142">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-143">False, True</span><span class="sxs-lookup"><span data-stu-id="3a870-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-144">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-145">Global</span><span class="sxs-lookup"><span data-stu-id="3a870-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-146">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-147">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-148">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-149">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-150">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-151">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-152">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-153">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-154">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-155">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-156">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-157">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-158">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-159">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="3a870-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="3a870-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="3a870-161">81</span><span class="sxs-lookup"><span data-stu-id="3a870-161">81</span></span>  

<span data-ttu-id="3a870-162">Dieser Parameter ermöglicht es Anwendungen, die im Modus für mehrere Instanzen arbeiten, Arbeitsspeicher für Versions Seiten in einem globalen Pool vorab zuzuweisen, um das ältere Verhalten zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="3a870-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="3a870-163">Dies ist nützlich für den Fall, dass die Anwendung sicherstellen möchte, dass Transaktionen einer bestimmten Größe später auch dann erfolgreich ausgeführt werden können, wenn der Arbeitsspeicher knapp wird.</span><span class="sxs-lookup"><span data-stu-id="3a870-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="3a870-164">**Windows 2000:**  Genügend Arbeitsspeicher für alle Versions Seiten ist immer zur [jetinit](./jetinit-function.md) -Zeit reserviert.</span><span class="sxs-lookup"><span data-stu-id="3a870-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="3a870-165">**Windows XP:**  Ab Windows XP ist dies im Einzel Instanzmodus immer noch true.</span><span class="sxs-lookup"><span data-stu-id="3a870-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="3a870-166">Der Arbeitsspeicher der Versions Seite wird jedoch im Modus für mehrere Instanzen dynamisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3a870-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-167">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-168">64</span><span class="sxs-lookup"><span data-stu-id="3a870-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-169">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-170">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-171">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-172">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-173">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-174">Global</span><span class="sxs-lookup"><span data-stu-id="3a870-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-175">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-176">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-177">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-178">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-179">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-180">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-181">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-182">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-183">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-184">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-185">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-186">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-187">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-188">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="3a870-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="3a870-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="3a870-190">8</span><span class="sxs-lookup"><span data-stu-id="3a870-190">8</span></span>  

<span data-ttu-id="3a870-191">Dieser Parameter reserviert die angeforderte Anzahl von Cursor Ressourcen für die Verwendung durch eine-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a870-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="3a870-192">Eine Cursor Ressource entspricht direkt einem [JET_TABLEID](./jet-tableid.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3a870-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="3a870-193">Diese Einstellung wirkt sich darauf aus, wie viele Cursor gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="3a870-194">Eine Cursor Ressource kann nicht von verschiedenen Sitzungen gemeinsam genutzt werden, daher muss dieser Parameter auf einen ausreichend großen Wert festgelegt werden, damit jede Sitzung beliebig viele Cursor verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="3a870-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="3a870-195">**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter belegen Adressraum und können die Speicherauslastung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3a870-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-196">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-197">1024</span><span class="sxs-lookup"><span data-stu-id="3a870-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-198">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-199">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-200">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-201">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-202">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-203">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-204">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-205">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-206">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-207">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-208">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-209">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-210">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-211">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-212">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-213">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-214">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-215">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-216">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-217">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="3a870-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="3a870-219">104</span><span class="sxs-lookup"><span data-stu-id="3a870-219">104</span></span>  

<span data-ttu-id="3a870-220">Dieser Parameter steuert die maximale Anzahl von Instanzen, die in einem einzelnen Prozess erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-221">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-222">16</span><span class="sxs-lookup"><span data-stu-id="3a870-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-223">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-224">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-225">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="3a870-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-227">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-228">Global</span><span class="sxs-lookup"><span data-stu-id="3a870-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-229">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-230">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-231">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-232">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-233">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-234">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-235">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-236">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-237">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-238">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-239">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-240">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-241">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-242">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="3a870-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="3a870-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="3a870-244">6</span><span class="sxs-lookup"><span data-stu-id="3a870-244">6</span></span>  

<span data-ttu-id="3a870-245">Dieser Parameter reserviert die angeforderte Anzahl von B +-strukturressourcen für die Verwendung durch eine-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a870-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="3a870-246">Diese Einstellung wirkt sich darauf aus, wie viele Tabellen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="3a870-247">Dieser Parameter muss relativ zum physischen Schema der Datenbanken festgelegt werden, die von der Datenbank-Engine verwendet werden. Daher ist diese Einstellung nicht so einfach wie möglich.</span><span class="sxs-lookup"><span data-stu-id="3a870-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="3a870-248">Im Allgemeinen benötigen Sie zwei Ressourcen und eine Ressource pro sekundärem Index pro Tabelle, die gleichzeitig von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a870-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="3a870-249">**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter belegen Adressraum und können die Speicherauslastung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3a870-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-250">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-251">300</span><span class="sxs-lookup"><span data-stu-id="3a870-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-252">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-253">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-254">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-255">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-256">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-257">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-258">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-259">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-260">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-261">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-262">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-263">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-264">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-265">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-266">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-267">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-268">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-269">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-270">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-271">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="3a870-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="3a870-273">5</span><span class="sxs-lookup"><span data-stu-id="3a870-273">5</span></span>  

<span data-ttu-id="3a870-274">Dieser Parameter reserviert die angeforderte Anzahl von Sitzungs Ressourcen für die Verwendung durch eine Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a870-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="3a870-275">Eine Sitzungs Ressource entspricht direkt einem [JET_SESID](./jet-sesid.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3a870-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="3a870-276">Diese Einstellung wirkt sich darauf aus, wie viele Sitzungen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="3a870-277">**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter belegen Adressraum und können die Speicherauslastung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3a870-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-278">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-279">16</span><span class="sxs-lookup"><span data-stu-id="3a870-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-280">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-281">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-282">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-283">0 – 30000</span><span class="sxs-lookup"><span data-stu-id="3a870-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-284">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-285">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-286">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-287">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-288">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-289">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-290">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-291">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-292">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-293">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-294">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-295">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-296">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-297">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-298">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-299">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="3a870-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="3a870-301">10</span><span class="sxs-lookup"><span data-stu-id="3a870-301">10</span></span>  

<span data-ttu-id="3a870-302">Dieser Parameter reserviert die angeforderte Anzahl von temporären Tabellen Ressourcen für die Verwendung durch eine Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a870-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="3a870-303">Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="3a870-304">**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter belegen Adressraum und können die Speicherauslastung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3a870-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="3a870-305">**Windows XP und höher:**  Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die temporäre Datenbank benötigt, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="3a870-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="3a870-306">Diese Einstellung kann hilfreich sein, um die e/a-Vorgänge zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich sind, wenn bekannt ist, dass Sie nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a870-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="3a870-307">**Hinweis**  Die Verwendung einer temporären Tabelle erfordert auch eine Cursor Ressource.</span><span class="sxs-lookup"><span data-stu-id="3a870-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-308">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-309">20</span><span class="sxs-lookup"><span data-stu-id="3a870-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-310">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-311">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-312">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-313">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-314">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-315">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-316">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-317">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-318">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-319">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-320">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-321">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-322">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-323">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-324">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-325">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-326">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-327">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-328">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-329">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="3a870-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="3a870-331">9</span><span class="sxs-lookup"><span data-stu-id="3a870-331">9</span></span>  

<span data-ttu-id="3a870-332">Dieser Parameter reserviert die angeforderte Anzahl von Versionsspeicher Seiten für die Verwendung durch eine Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a870-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="3a870-333">Der Versionsspeicher enthält einen Live Datensatz aller verschiedenen Versionen der einzelnen Datensatz-oder Indexeinträge in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="3a870-334">Diese Versionen werden zur Unterstützung der Parallelitäts Steuerung mit mehreren Versionsverwaltung verwendet, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahme Isolation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a870-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="3a870-335">Diese Einstellung wirkt sich darauf aus, wie viele Updates gleichzeitig im Arbeitsspeicher gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="3a870-336">Dies wirkt sich wiederum auf die maximale Anzahl von Updates aus, die eine einzelne Transaktion ausführen kann, die maximale Dauer, die eine Transaktion geöffnet werden kann, die maximale gleichzeitige Auslastung der Aktualisierung von Transaktionen im System oder eine Kombination daraus.</span><span class="sxs-lookup"><span data-stu-id="3a870-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="3a870-337">Jede Versionsspeicher Seite, die von diesem Parameter konfiguriert wurde, beträgt 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.</span><span class="sxs-lookup"><span data-stu-id="3a870-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="3a870-338">**Windows Vista und höher:**  Die Seitengröße des Versionsspeicher kann über JET_paramVerPageSize gelesen und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="3a870-339">**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter belegen Adressraum und können die Speicherauslastung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3a870-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="3a870-340">**Hinweis**  Dabei handelt es sich um die weit verbreiteten Ressourcen, die von der Datenbank-Engine aufgebraucht werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="3a870-341">Die Einstellung des System Parameters und die transaktionale Auslastung der Anwendung müssen sorgfältig beachtet werden, um zu vermeiden, dass diese Ressource im normalen Betrieb erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="3a870-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="3a870-342">Wenn diese Ressource erschöpft ist, werden Updates der Datenbank mit Jet_errVersionStoreOutOfMemory zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="3a870-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="3a870-343">Um einige dieser Ressourcen freizugeben, muss die älteste ausstehende Transaktion abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-344">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-345">64</span><span class="sxs-lookup"><span data-stu-id="3a870-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-346">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-347">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-348">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-349">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-350">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-351">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-352">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-353">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-354">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-355">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-356">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-357">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-358">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-359">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-360">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-361">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-362">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-363">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-364">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-365">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="3a870-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="3a870-367">101</span><span class="sxs-lookup"><span data-stu-id="3a870-367">101</span></span>  

<span data-ttu-id="3a870-368">Dieser Parameter steuert die Größe eines speziellen Caches, der verwendet wird, um die Suche nach untergeordneten Seiten Zeigern der B +-Struktur im Datenbankseiten Cache zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="3a870-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="3a870-369">Die Größe des Caches beträgt bytes.</span><span class="sxs-lookup"><span data-stu-id="3a870-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-370">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-371">262144</span><span class="sxs-lookup"><span data-stu-id="3a870-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-372">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-373">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-374">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-375">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-376">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-377">Global</span><span class="sxs-lookup"><span data-stu-id="3a870-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-378">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-379">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-380">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-381">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-382">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-383">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-384">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-385">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-386">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-387">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-388">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-389">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-390">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-391">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="3a870-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="3a870-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="3a870-393">7</span><span class="sxs-lookup"><span data-stu-id="3a870-393">7</span></span>  

<span data-ttu-id="3a870-394">Dieser Parameter versucht, die Anzahl von B +-strukturressourcen unterhalb des angegebenen Schwellenwerts beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3a870-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="3a870-395">Wenn dieser Parameter auf 0 (null) festgelegt ist, wird standardmäßig 100% der **JET_paramMaxOpenTables** verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a870-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="3a870-396">**Windows Vista und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.</span><span class="sxs-lookup"><span data-stu-id="3a870-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="3a870-397">Anwendungen sollten stattdessen JET_paramMaxCachedClosedTables verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a870-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-398">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-399">0 (100% der <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="3a870-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-400">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-401">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-402">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-403">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-404">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-405">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-406">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-407">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-408">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-409">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-410">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-411">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-412">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-413">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-414">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-415">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-416">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-417">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-418">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-419">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="3a870-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="3a870-421">63</span><span class="sxs-lookup"><span data-stu-id="3a870-421">63</span></span>  

<span data-ttu-id="3a870-422">Dieser Parameter stellt einen Schwellenwert relativ zu **JET_paramMaxVerPages** dar, der die freigegebene Verwendung von Versions Seiten durch die Datenbank-Engine steuert.</span><span class="sxs-lookup"><span data-stu-id="3a870-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="3a870-423">Wenn die Größe des Versionsspeicher diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. b. das Freigeben von gelöschtem Speicherplatz in der Datenbank, stattdessen geopfert, um Platz für Transaktionsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a870-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="3a870-424">**Windows 2000, Windows XP und Windows Server 2003:**  Wenn Sie diesen Parameter auf NULL festlegen, wird der Schwellenwert auf 90% der **JET_paramMaxVerPages** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a870-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="3a870-425">**Windows Vista und höher:**  Dies wird nicht mehr unterstützt, und der Standardwert dieses Parameters wurde geändert, um sein Verhalten zu verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="3a870-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="3a870-426">Jede Versionsspeicher Seite, die von diesem Parameter konfiguriert wurde, beträgt 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.</span><span class="sxs-lookup"><span data-stu-id="3a870-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="3a870-427">**Windows Vista und höher:**  Die Seitengröße des Versionsspeicher kann über JET_paramVerPageSize gelesen und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="3a870-428">**Hinweis**  Wenn die Datenbank-Engine zu häufig über diesem Schwellenwert arbeitet, kann die Leistung der Datenbank beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="3a870-429">Dies liegt daran, dass die Hintergrundprozesse, die die Datenbank bereinigen, ohne die optionalen Informationen, die in diesem Szenario verworfen werden, funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="3a870-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="3a870-430">Die Online-oder Offline Defragmentierung wirkt sich gegen diesen Effekt aus.</span><span class="sxs-lookup"><span data-stu-id="3a870-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-431">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-432"><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  0 (90% der JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="3a870-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="3a870-433"><strong>Windows Vista:</strong>  58</span><span class="sxs-lookup"><span data-stu-id="3a870-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-434">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-435">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-436">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-437">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="3a870-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-438">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-439">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-440">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-441">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-442">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-443">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-444">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-445">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-446">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-447">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-448">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-449">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-450">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-451">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-452">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-453">Alle</span><span class="sxs-lookup"><span data-stu-id="3a870-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="3a870-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="3a870-455">128</span><span class="sxs-lookup"><span data-stu-id="3a870-455">128</span></span>  

<span data-ttu-id="3a870-456">Dieser Parameter steuert die Größe der Versionsspeicher Seiten, die von der Datenbank-Engine zum Speichern von Transaktionsinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a870-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="3a870-457">Der Wert dieses Parameters ist die Einheiten Größe für alle anderen Systemparameter, die auf Versions Seiten (z. b. JET_paramMaxVerPages) liegen.</span><span class="sxs-lookup"><span data-stu-id="3a870-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="3a870-458">Die Datenbank-Engine kann eine größere Seitengröße als die angeforderte Größe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a870-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-459">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-460">16384</span><span class="sxs-lookup"><span data-stu-id="3a870-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-461">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-462">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-463">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="3a870-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-465">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-466">Global</span><span class="sxs-lookup"><span data-stu-id="3a870-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-467">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-468">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-469">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-470">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-471">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-472">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-473">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-474">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-475">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-476">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-477">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-478">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-479">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-480">Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="3a870-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a870-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="3a870-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="3a870-482">105</span><span class="sxs-lookup"><span data-stu-id="3a870-482">105</span></span>  

<span data-ttu-id="3a870-483">Dieser Parameter steuert die Anzahl der Arbeitsaufgaben im Hintergrund Bereinigung, die zu einem beliebigen Zeitpunkt in die Warteschlange des Thread Pools der Datenbank-Engine eingereiht werden können.</span><span class="sxs-lookup"><span data-stu-id="3a870-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-484">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="3a870-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3a870-485">32</span><span class="sxs-lookup"><span data-stu-id="3a870-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-486">Typ:</span><span class="sxs-lookup"><span data-stu-id="3a870-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="3a870-487">Integer</span><span class="sxs-lookup"><span data-stu-id="3a870-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-488">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a870-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3a870-489"><strong>Windows XP und Windows Server 2003:  </strong>  1 – 63</span><span class="sxs-lookup"><span data-stu-id="3a870-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="3a870-490"><strong>Windows Vista:</strong>  1 – 127</span><span class="sxs-lookup"><span data-stu-id="3a870-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-491">Umfang:</span><span class="sxs-lookup"><span data-stu-id="3a870-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3a870-492">Instanz</span><span class="sxs-lookup"><span data-stu-id="3a870-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-493">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-494">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-495">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="3a870-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3a870-496"><strong>Windows XP und Windows Server 2003:  </strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="3a870-497"><strong>Windows Vista:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="3a870-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-498">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="3a870-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3a870-499">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-500">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-501">Nein</span><span class="sxs-lookup"><span data-stu-id="3a870-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-502">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="3a870-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3a870-503">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-504">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3a870-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3a870-505">Ja</span><span class="sxs-lookup"><span data-stu-id="3a870-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-506">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="3a870-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3a870-507">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="3a870-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="3a870-508">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a870-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a870-509"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3a870-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3a870-510">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3a870-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a870-511"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3a870-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3a870-512">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3a870-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a870-513"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3a870-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3a870-514">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3a870-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3a870-515">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a870-515">See Also</span></span>

[<span data-ttu-id="3a870-516">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="3a870-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="3a870-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="3a870-517">JetInit</span></span>](./jetinit-function.md)
