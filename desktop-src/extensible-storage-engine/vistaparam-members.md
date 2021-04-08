---
description: 'Weitere Informationen finden Sie hier: vistaparam-Member'
title: Vistaparam-Member (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861928"
---
# <a name="vistaparam-members"></a><span data-ttu-id="62bf5-103">Vistaparam-Member</span><span class="sxs-lookup"><span data-stu-id="62bf5-103">VistaParam members</span></span>

<span data-ttu-id="62bf5-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="62bf5-104">Include protected members</span></span>  
<span data-ttu-id="62bf5-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="62bf5-105">Include inherited members</span></span>  

<span data-ttu-id="62bf5-106">System Parameter, die der Vista-Version von ESENT hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="62bf5-106">System parameters that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="62bf5-107">Der [vistaparam](./vistaparam-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="62bf5-107">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="62bf5-108">Felder</span><span class="sxs-lookup"><span data-stu-id="62bf5-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="62bf5-109">Name</span><span class="sxs-lookup"><span data-stu-id="62bf5-109">Name</span></span></th>
<th><span data-ttu-id="62bf5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62bf5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-113"><a href="dn335379(v=exchg.10).md">Cachedclosedtables</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="62bf5-114">Dieser Parameter steuert die Anzahl der B +-strukturressourcen, die von der-Instanz zwischengespeichert wurden, nachdem die Tabellen, die Sie darstellen, von der Anwendung geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="62bf5-114">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="62bf5-115">Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="62bf5-115">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="62bf5-116">Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="62bf5-116">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="62bf5-120">Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="62bf5-120">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="62bf5-121">Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="62bf5-121">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="62bf5-122">Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="62bf5-122">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="62bf5-123">Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.</span><span class="sxs-lookup"><span data-stu-id="62bf5-123">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="62bf5-124">Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="62bf5-124">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-127"><a href="dn335380(v=exchg.10).md">Enableadvanced</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="62bf5-128">Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="62bf5-128">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="62bf5-129">Dieser Parameter wird zusammen mit der <a href="dn335289(v=exchg.10).md">Konfiguration</a> verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="62bf5-129">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-132"><a href="dn335291(v=exchg.10).md">Enablefilecache</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="62bf5-133">Aktivieren Sie die Verwendung des Betriebssystem-Datei Caches für alle verwalteten Dateien.</span><span class="sxs-lookup"><span data-stu-id="62bf5-133">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-136"><a href="dn335381(v=exchg.10).md">Enableviewcache</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="62bf5-137">Aktivieren Sie die Verwendung von Datei-e/a mit Speicher Abbild für Datenbankdateien.</span><span class="sxs-lookup"><span data-stu-id="62bf5-137">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-140"><a href="dn335292(v=exchg.10).md">Keymost</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-140"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="62bf5-141">Dieser schreibgeschützte Parameter gibt die maximal zulässige Länge des Index Schlüssels an, die für die aktuelle Datenbankseiten Größe (wie von <a href="hh596135(v=exchg.10).md">databasepagesize</a>konfiguriert) ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="62bf5-141">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-144"><a href="dn335384(v=exchg.10).md">Legacyfile-Namen</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="62bf5-145">Dieser Parameter stellt Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine bereit.</span><span class="sxs-lookup"><span data-stu-id="62bf5-145">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="62bf5-149">Legen Sie den mit TABLE class 10 verknüpften Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-149">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="62bf5-153">Legen Sie den Namen der Tabellen Klasse 11 fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-153">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="62bf5-157">Legen Sie den der Table-Klasse 12 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-157">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="62bf5-161">Legen Sie den der Table-Klasse 13 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-161">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="62bf5-165">Legen Sie den der Table-Klasse 14 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-165">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="62bf5-169">Legen Sie den der Tabellen Klasse 15 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-169">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="62bf5-173">Legen Sie den mit Table Class 1 verknüpften Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-173">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="62bf5-177">Legen Sie den der Table-Klasse 2 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-177">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="62bf5-181">Legen Sie den Namen der Tabelle Class 3 fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-181">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="62bf5-185">Legen Sie den der Table-Klasse 4 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-185">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="62bf5-189">Legen Sie den der Table-Klasse 5 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-189">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="62bf5-193">Legen Sie den der Tabellen Klasse 6 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-193">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="62bf5-197">Legen Sie den der Tabelle Class 7 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-197">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="62bf5-201">Legen Sie den der Tabellen Klasse 8 zugeordneten Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-201">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="62bf5-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="62bf5-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="62bf5-205">Legen Sie den mit TABLE class 9 verknüpften Namen fest.</span><span class="sxs-lookup"><span data-stu-id="62bf5-205">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62bf5-206">Oben</span><span class="sxs-lookup"><span data-stu-id="62bf5-206">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="62bf5-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62bf5-207">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62bf5-208">Referenz</span><span class="sxs-lookup"><span data-stu-id="62bf5-208">Reference</span></span>

[<span data-ttu-id="62bf5-209">Vistaparam-Klasse</span><span class="sxs-lookup"><span data-stu-id="62bf5-209">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="62bf5-210">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="62bf5-210">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
