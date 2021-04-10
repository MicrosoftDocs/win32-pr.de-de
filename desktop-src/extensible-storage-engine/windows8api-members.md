---
description: 'Weitere Informationen finden Sie hier: Windows8Api Members'
title: Windows8Api-Member (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: Windows8Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_members(v=EXCHG.10)
ms:contentKeyID: 55104331
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21167b66736e5bc05ec14f32cb715226264d2757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959201"
---
# <a name="windows8api-members"></a><span data-ttu-id="ad639-103">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="ad639-103">Windows8Api members</span></span>

<span data-ttu-id="ad639-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ad639-104">Include protected members</span></span>  
<span data-ttu-id="ad639-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ad639-105">Include inherited members</span></span>  

<span data-ttu-id="ad639-106">In Windows 8 eingeführte API-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="ad639-106">Api calls introduced in Windows 8.</span></span>

<span data-ttu-id="ad639-107">Der [Windows8Api](./windows8api-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad639-107">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="ad639-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ad639-108">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ad639-109">Name</span><span class="sxs-lookup"><span data-stu-id="ad639-109">Name</span></span></th>
<th><span data-ttu-id="ad639-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad639-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="ad639-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="ad639-114">Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad639-114">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="ad639-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="ad639-118">Führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt.</span><span class="sxs-lookup"><span data-stu-id="ad639-118">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="ad639-119">Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen in den Zustand der Datenbank übertragen, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="ad639-119">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="ad639-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="ad639-123">Erstellt Indizes für Daten in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ad639-123">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="ad639-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="ad639-127">Erstellt eine Tabelle, fügt der Tabelle Spalten und Indizes hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad639-127">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="ad639-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="ad639-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-131"><a href="dn335493(v=exchg.10).md">Jetgeterrorinfo</a></span><span class="sxs-lookup"><span data-stu-id="ad639-131"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="ad639-132">Ruft erweiterte Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="ad639-132">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="ad639-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="ad639-136">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="ad639-136">Creates a temporary table with a single index.</span></span> <span data-ttu-id="ad639-137">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad639-137">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="ad639-138">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="ad639-138">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="ad639-139">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="ad639-139">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="ad639-140">Siehe auch <a href="dn292231(v=exchg.10).md">jetopentemptable (JET_SESID, [], Int32, temptablegrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="ad639-140">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="ad639-141"><a href="dn335326(v=exchg.10).md">Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="ad639-141"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-144"><a href="dn335382(v=exchg.10).md">Jetprereadindexbereiche</a></span><span class="sxs-lookup"><span data-stu-id="ad639-144"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="ad639-145">Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ad639-145">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-148"><a href="dn335496(v=exchg.10).md">Jetresizedatabase</a></span><span class="sxs-lookup"><span data-stu-id="ad639-148"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="ad639-149">Ändert die Größe einer aktuell geöffneten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ad639-149">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-152"><a href="dn335383(v=exchg.10).md">Jetsetcurrsorfilter</a></span><span class="sxs-lookup"><span data-stu-id="ad639-152"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="ad639-153">Legen Sie ein Array einfacher Filter für <a href="dn292217(v=exchg.10).md">jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)</a>fest.</span><span class="sxs-lookup"><span data-stu-id="ad639-153">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-156"><a href="dn335495(v=exchg.10).md">Jetabessionparameter</a></span><span class="sxs-lookup"><span data-stu-id="ad639-156"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="ad639-157">Legt einen Parameter für den bereitgestellten Sitzungszustand fest, der für die Lebensdauer dieser Sitzung oder bis zur zurück Setzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad639-157">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="ad639-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="ad639-161">Bereitet eine Instanz für die Beendigung vor.</span><span class="sxs-lookup"><span data-stu-id="ad639-161">Prepares an instance for termination.</span></span> <span data-ttu-id="ad639-162">Kann auch verwendet werden, um ein vorheriges versetzen wieder aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ad639-162">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-165"><a href="dn335386(v=exchg.10).md">Jettryprereadindexranges</a></span><span class="sxs-lookup"><span data-stu-id="ad639-165"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="ad639-166">Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ad639-166">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ad639-169"><a href="dn335499(v=exchg.10).md">Prereadkeyranges</a></span><span class="sxs-lookup"><span data-stu-id="ad639-169"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="ad639-170">Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ad639-170">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad639-171">Oben</span><span class="sxs-lookup"><span data-stu-id="ad639-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ad639-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad639-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad639-173">Referenz</span><span class="sxs-lookup"><span data-stu-id="ad639-173">Reference</span></span>

[<span data-ttu-id="ad639-174">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad639-174">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="ad639-175">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad639-175">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
