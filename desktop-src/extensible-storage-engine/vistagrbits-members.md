---
description: 'Weitere Informationen finden Sie hier: vistagrbits-Member'
title: Vistagrbits-Member (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551812"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="276f9-103">Vistagrbits-Member</span><span class="sxs-lookup"><span data-stu-id="276f9-103">VistaGrbits members</span></span>

<span data-ttu-id="276f9-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="276f9-104">Include protected members</span></span>  
<span data-ttu-id="276f9-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="276f9-105">Include inherited members</span></span>  

<span data-ttu-id="276f9-106">Grbits, die der Vista-Version von ESENT hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="276f9-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="276f9-107">Der [vistagrbits](./vistagrbits-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="276f9-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="276f9-108">Felder</span><span class="sxs-lookup"><span data-stu-id="276f9-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="276f9-109">Name</span><span class="sxs-lookup"><span data-stu-id="276f9-109">Name</span></span></th>
<th><span data-ttu-id="276f9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="276f9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-113"><a href="dn351283(v=exchg.10).md">Continueafterthaw</a></span><span class="sxs-lookup"><span data-stu-id="276f9-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="276f9-114">Die Momentaufnahme Sitzung wird nach jedessnapshotthaw fortgesetzt, und es wird ein jedessnapshotend-Funktions aufrufbedarf benötigt.</span><span class="sxs-lookup"><span data-stu-id="276f9-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-117"><a href="dn335364(v=exchg.10).md">Indexcrossproduct</a></span><span class="sxs-lookup"><span data-stu-id="276f9-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="276f9-118">Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="276f9-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="276f9-119">Andernfalls würde der Index nur einen Eintrag für jeden multiwert in der signifikantesten Schlüssel Spalte enthalten, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten mehrwertigen Wert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind.</span><span class="sxs-lookup"><span data-stu-id="276f9-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="276f9-120">Wenn Sie z. B. dieses Flag für einen Index über Spalte a mit den Werten &quot; rot &quot; und &quot; blau &quot; und over column B mit den Werten 1 und 2 angegeben haben, &quot; &quot; &quot; &quot; werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blau &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="276f9-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="276f9-121">Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="276f9-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-124"><a href="dn335368(v=exchg.10).md">Indexdisallowtrunation</a></span><span class="sxs-lookup"><span data-stu-id="276f9-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="276f9-125">Die Angabe dieses Flags führt dazu, dass ein Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit <a href="hh564840(v=exchg.10).md">keytruncated</a>fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="276f9-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="276f9-126">Andernfalls werden Schlüssel automatisch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="276f9-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-129"><a href="dn351285(v=exchg.10).md">Indexnetstedtable</a></span><span class="sxs-lookup"><span data-stu-id="276f9-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="276f9-130">Indizieren Sie mehr als mehrere mehrwertige Spalten, aber nur mit Werten derselben itagsequence.</span><span class="sxs-lookup"><span data-stu-id="276f9-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-133"><a href="dn335282(v=exchg.10).md">Logstreammustexist</a></span><span class="sxs-lookup"><span data-stu-id="276f9-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="276f9-134">Transaktionsprotokolle müssen im Protokoll Dateiverzeichnis vorhanden sein (d. h., ein neuer Stream kann nicht automatisch gestartet werden).</span><span class="sxs-lookup"><span data-stu-id="276f9-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-137"><a href="dn335367(v=exchg.10).md">Wiederherstellenrückgängigmachen</a></span><span class="sxs-lookup"><span data-stu-id="276f9-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="276f9-138">Führen Sie die Wiederherstellung aus, aber stoppen Sie die Roll Back Phase.</span><span class="sxs-lookup"><span data-stu-id="276f9-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="276f9-139">Ermöglicht, dass die Protokolle wiedergegeben werden können. später können zusätzliche Protokolle kopiert und wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="276f9-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-142"><a href="dn335375(v=exchg.10).md">Replaymissingmapentrydb</a></span><span class="sxs-lookup"><span data-stu-id="276f9-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="276f9-143">Fehlender Daten Bank Zuordnungs Eintrag ist standardmäßig derselbe Speicherort.</span><span class="sxs-lookup"><span data-stu-id="276f9-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-146"><a href="dn335283(v=exchg.10).md">Trunalisiedone</a></span><span class="sxs-lookup"><span data-stu-id="276f9-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="276f9-147">Die Engine kann die Daten Bank Header nach Bedarf markieren (z. b. eine vollständige Sicherung abgeschlossen), obwohl der Abschneidevorgang nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="276f9-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="276f9-150"><a href="dn335371(v=exchg.10).md">Trungatelogsafterrecovery</a></span><span class="sxs-lookup"><span data-stu-id="276f9-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="276f9-151">Bei erfolgreicher Soft-Wiederherstellung kürzen Sie die Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="276f9-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="276f9-152">Oben</span><span class="sxs-lookup"><span data-stu-id="276f9-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="276f9-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="276f9-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="276f9-154">Referenz</span><span class="sxs-lookup"><span data-stu-id="276f9-154">Reference</span></span>

[<span data-ttu-id="276f9-155">Vistagrbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="276f9-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="276f9-156">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="276f9-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
