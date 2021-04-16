---
description: 'Weitere Informationen finden Sie hier: SystemParameters-Member'
title: SystemParameters-Member
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e317ef4e63a33951dc55e030718d226ae3eaeec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571060"
---
# <a name="systemparameters-members"></a><span data-ttu-id="3e628-103">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="3e628-103">SystemParameters members</span></span>

<span data-ttu-id="3e628-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="3e628-104">Include protected members</span></span>  
<span data-ttu-id="3e628-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="3e628-105">Include inherited members</span></span>  

<span data-ttu-id="3e628-106">Konstanten für die ESENT-API.</span><span class="sxs-lookup"><span data-stu-id="3e628-106">Constants for the ESENT API.</span></span> <span data-ttu-id="3e628-107">Diese müssen nicht über Systemparameter gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="3e628-107">These don't have to be looked up via system parameters.</span></span> <span data-ttu-id="3e628-108">Diese Klasse stellt statische Eigenschaften zum Festlegen und erhalten globaler ESENT-Systemparameter bereit.</span><span class="sxs-lookup"><span data-stu-id="3e628-108">This class provides static properties to set and get global ESENT system parameters.</span></span> <span data-ttu-id="3e628-109">Diese Klasse stellt statische Eigenschaften zum Festlegen und erhalten globaler ESENT-Systemparameter bereit.</span><span class="sxs-lookup"><span data-stu-id="3e628-109">This class provides static properties to set and get global ESENT system parameters.</span></span>

<span data-ttu-id="3e628-110">Der [System Parameters](./systemparameters-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e628-110">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="3e628-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e628-111">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3e628-112">Name</span><span class="sxs-lookup"><span data-stu-id="3e628-112">Name</span></span></th>
<th><span data-ttu-id="3e628-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e628-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-116"><a href="dn351215(v=exchg.10).md">Bookmarkmost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="3e628-117">Ruft die maximale Größe eines Lesezeichens ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-117">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="3e628-118"><a href="dn292149(v=exchg.10).md">Jetgetbookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="3e628-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="3e628-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="3e628-122">Ruft die Größe des Daten Bank Caches in Seiten ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-122">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="3e628-123">Standardmäßig wird der Daten Bank Cache automatisch seine Größe optimieren. wenn diese Eigenschaft auf einen Wert ungleich NULL festgelegt wird, wird der Cache an die Zielgröße angepasst.</span><span class="sxs-lookup"><span data-stu-id="3e628-123">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-126"><a href="dn351149(v=exchg.10).md">Cachesizemax</a></span><span class="sxs-lookup"><span data-stu-id="3e628-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="3e628-127">Ruft die maximale Größe des Cache für die Datenbankseite ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-127">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="3e628-128">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="3e628-128">The size is in database pages.</span></span> <span data-ttu-id="3e628-129">Wenn dieser Parameter auf seinen Standardwert zurückgesetzt wird, wird die maximale Cache Größe auf die Größe des physischen Arbeitsspeichers festgelegt, wenn jetinit aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3e628-129">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-132"><a href="dn351216(v=exchg.10).md">Cachesizemin</a></span><span class="sxs-lookup"><span data-stu-id="3e628-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="3e628-133">Ruft die Mindestgröße des Datenbankseiten Caches in Datenbankseiten ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-133">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-136"><a href="dn351151(v=exchg.10).md">Columnskeymost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="3e628-137">Ruft die maximale Anzahl von Komponenten in einem Sortier-oder Index Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-137">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="3e628-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="3e628-141">Ruft einen Wert ab, der die Standardwerte für den gesamten Satz von Systemparametern angibt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-141">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="3e628-142">Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3e628-142">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="3e628-143">Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3e628-143">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="3e628-144">Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.</span><span class="sxs-lookup"><span data-stu-id="3e628-144">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="3e628-145">Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3e628-145">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="3e628-146">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="3e628-146">Supported on Windows Vista and up.</span></span> <span data-ttu-id="3e628-147">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3e628-147">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-150"><a href="dn351153(v=exchg.10).md">Databasepagesize</a></span><span class="sxs-lookup"><span data-stu-id="3e628-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="3e628-151">Ruft die Größe der Datenbankseiten in Bytes ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-151">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-154"><a href="dn351221(v=exchg.10).md">Enableadvanced</a></span><span class="sxs-lookup"><span data-stu-id="3e628-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="3e628-155">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="3e628-155">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="3e628-156">Dieser Parameter wird zusammen mit der <a href="dn351218(v=exchg.10).md">Konfiguration</a> verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3e628-156">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="3e628-157">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="3e628-157">Supported on Windows Vista and up.</span></span> <span data-ttu-id="3e628-158">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3e628-158">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-161"><a href="dn351152(v=exchg.10).md">Enablefilecache</a></span><span class="sxs-lookup"><span data-stu-id="3e628-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="3e628-162">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine den Dateicache für alle verwalteten Dateien verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="3e628-162">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-165"><a href="dn351220(v=exchg.10).md">Enableviewcache</a></span><span class="sxs-lookup"><span data-stu-id="3e628-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="3e628-166">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine für Datenbankdateien Datei-e/a für den Speicher</span><span class="sxs-lookup"><span data-stu-id="3e628-166">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-169"><a href="dn351223(v=exchg.10).md">Eventlogginglevel</a></span><span class="sxs-lookup"><span data-stu-id="3e628-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="3e628-170">Ruft die Detailebene von EventLog-Meldungen ab, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-170">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="3e628-171">Höhere Zahlen führen zu ausführlicheren Ereignisprotokoll Meldungen.</span><span class="sxs-lookup"><span data-stu-id="3e628-171">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-174"><a href="dn351154(v=exchg.10).md">Exceptionaction</a></span><span class="sxs-lookup"><span data-stu-id="3e628-174"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="3e628-175">Ruft den Wert ab oder legt ihn fest, was mit in Jet generierten Ausnahmen zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="3e628-175">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-178"><a href="dn351227(v=exchg.10).md">Hungioactions</a></span><span class="sxs-lookup"><span data-stu-id="3e628-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="3e628-179">Ruft den Satz von Aktionen ab, die für IOS ausgeführt werden sollen, der nicht reagiert hat, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="3e628-179">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-182"><a href="dn351155(v=exchg.10).md">Hungiothreshold</a></span><span class="sxs-lookup"><span data-stu-id="3e628-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="3e628-183">Ruft den Schwellenwert für das, was als nicht reagierender e/a angesehen wird, ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-183">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-186"><a href="dn351156(v=exchg.10).md">Keymost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-186"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="3e628-187">Ruft die maximale Schlüsselgröße ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-187">Gets the maximum key size.</span></span> <span data-ttu-id="3e628-188">Dies hängt von der ESENT-Version und der Datenbankseiten Größe ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-188">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-191"><a href="dn351229(v=exchg.10).md">Legacyfile-Namen</a></span><span class="sxs-lookup"><span data-stu-id="3e628-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="3e628-192">Ruft die Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-192">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-195"><a href="dn351157(v=exchg.10).md">Lvchunksizemost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="3e628-196">Ruft die Größe des LV-Blöcken ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-196">Gets the lv chunks size.</span></span> <span data-ttu-id="3e628-197">Dies hängt von der Größe der Datenbankseite ab.</span><span class="sxs-lookup"><span data-stu-id="3e628-197">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-200"><a href="dn351230(v=exchg.10).md">Maxinstance</a></span><span class="sxs-lookup"><span data-stu-id="3e628-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="3e628-201">Ruft die maximale Anzahl von Instanzen ab, die erstellt werden können, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-201">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-204"><a href="dn351160(v=exchg.10).md">Mindataforxpress</a></span><span class="sxs-lookup"><span data-stu-id="3e628-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="3e628-205">Ruft die kleinste Datenmenge ab, die mit der Xpress-Komprimierung komprimiert werden soll, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-205">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-208"><a href="dn351159(v=exchg.10).md">Outstandingiomax</a></span><span class="sxs-lookup"><span data-stu-id="3e628-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="3e628-209">Mit diesem Parameter wird gesteuert, wie viele Datenbankdatei-e/a-Vorgänge pro Datenträger im Host Betriebssystem gleichzeitig in eine Warteschlange eingereiht werden können.</span><span class="sxs-lookup"><span data-stu-id="3e628-209">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="3e628-210">Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e628-210">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-213"><a href="dn351158(v=exchg.10).md">Processfriendlyname</a></span><span class="sxs-lookup"><span data-stu-id="3e628-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="3e628-214">Ruft den anzeigen Amen für diese Instanz des Prozesses ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-214">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-217"><a href="dn351161(v=exchg.10).md">Startflushthreshold</a></span><span class="sxs-lookup"><span data-stu-id="3e628-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="3e628-218">Ruft den Schwellenwert ab oder legt diesen fest, an dem der Datenbankseiten Cache mit der Überprüfung von Seiten aus dem Cache beginnt, um Platz für nicht zwischengespeicherte Seiten zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="3e628-218">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="3e628-219">Wenn die Anzahl der Seiten Puffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um den Pool der verfügbaren Puffer aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="3e628-219">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="3e628-220">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3e628-220">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="3e628-221">Dieser Schwellenwert muss auch immer niedriger als der von JET_paramStopFlushThreshold festgelegte Schwellenwert sein.</span><span class="sxs-lookup"><span data-stu-id="3e628-221">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="3e628-222">Die Entfernungs Höhe des Start Schwellenwerts bestimmt die Antwortzeit, die der Datenbankseiten Cache aufweisen muss, damit verfügbare Puffer erstellt werden, bevor die Anwendung Sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="3e628-222">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="3e628-223">Ein Schwellenwert für hohe Starts gibt dem Hintergrundprozess mehr Zeit für die Reaktion.</span><span class="sxs-lookup"><span data-stu-id="3e628-223">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="3e628-224">Ein Schwellenwert für hohe Starts impliziert jedoch einen höheren Schwellenwert für die Beendigung, wodurch die effektive Größe des Datenbankseiten Caches verringert wird.</span><span class="sxs-lookup"><span data-stu-id="3e628-224">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-227"><a href="dn351231(v=exchg.10).md">Stopflushthreshold</a></span><span class="sxs-lookup"><span data-stu-id="3e628-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="3e628-228">Ruft den Schwellenwert ab, an dem der Datenbankseiten Cache die Überprüfung von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3e628-228">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="3e628-229">Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="3e628-229">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="3e628-230">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3e628-230">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="3e628-231">Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch JET_paramStartFlushThreshold festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3e628-231">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="3e628-232">Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden.</span><span class="sxs-lookup"><span data-stu-id="3e628-232">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="3e628-233">Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="3e628-233">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="3e628-234">Ein Schwellenwert für hohe Beendigung verringert jedoch die effektive Größe des Datenbankseiten Caches.</span><span class="sxs-lookup"><span data-stu-id="3e628-234">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e628-235">Oben</span><span class="sxs-lookup"><span data-stu-id="3e628-235">Top</span></span>

## <a name="fields"></a><span data-ttu-id="3e628-236">Felder</span><span class="sxs-lookup"><span data-stu-id="3e628-236">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3e628-237">Name</span><span class="sxs-lookup"><span data-stu-id="3e628-237">Name</span></span></th>
<th><span data-ttu-id="3e628-238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e628-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-241"><a href="dn351208(v=exchg.10).md">Basenamelength</a></span><span class="sxs-lookup"><span data-stu-id="3e628-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span></span></td>
<td><span data-ttu-id="3e628-242">Die Länge des Präfixes, das verwendet wird, um die von der Datenbank-Engine verwendeten Dateien zu benennen.</span><span class="sxs-lookup"><span data-stu-id="3e628-242">The length of the prefix used to name files used by the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-245"><a href="dn351146(v=exchg.10).md">Columlichlichste</a></span><span class="sxs-lookup"><span data-stu-id="3e628-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span></span></td>
<td><span data-ttu-id="3e628-246">Maximale Größe für Spalten, die nicht JET_coltyp werden. LONGBINARY oder JET_coltyp. LongText.</span><span class="sxs-lookup"><span data-stu-id="3e628-246">Maximum size for columns which are not JET_coltyp.LongBinary or JET_coltyp.LongText.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-249"><a href="dn351210(v=exchg.10).md">Columnsfixedmost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span></span></td>
<td><span data-ttu-id="3e628-250">Die maximal zulässige Anzahl fester Spalten in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e628-250">Maximum number of fixed columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-253"><a href="dn351140(v=exchg.10).md">Columnsmost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span></span></td>
<td><span data-ttu-id="3e628-254">Die maximal zulässige Anzahl von Spalten in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e628-254">Maximum number of columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-257"><a href="dn351148(v=exchg.10).md">Columnstaggedmost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span></span></td>
<td><span data-ttu-id="3e628-258">Die maximal zulässige Anzahl von markierten Spalten in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e628-258">Maximum number of tagged columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-261"><a href="dn351212(v=exchg.10).md">Columnsvarmost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span></span></td>
<td><span data-ttu-id="3e628-262">Maximale Anzahl von Spalten variabler Länge, die in einer Tabelle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3e628-262">Maximum number of variable-length columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-265"><a href="dn351141(v=exchg.10).md">Localenamemaxlength</a></span><span class="sxs-lookup"><span data-stu-id="3e628-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span></span></td>
<td><span data-ttu-id="3e628-266">Die maximale Länge eines Gebiets Schema namens (LOCALE_NAME_MAX_LENGTH aus "Winnt. h").</span><span class="sxs-lookup"><span data-stu-id="3e628-266">The maximum length of a locale name (LOCALE_NAME_MAX_LENGTH from winnt.h).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-269"><a href="dn351213(v=exchg.10).md">Namemost</a></span><span class="sxs-lookup"><span data-stu-id="3e628-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span></span></td>
<td><span data-ttu-id="3e628-270">Maximale Größe eines Tabellen-/Spalten-/Indexnamens.</span><span class="sxs-lookup"><span data-stu-id="3e628-270">Maximum size of a table/column/index name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="3e628-273"><a href="dn351211(v=exchg.10).md">Pagetempdbkleinsten</a></span><span class="sxs-lookup"><span data-stu-id="3e628-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span></span></td>
<td><span data-ttu-id="3e628-274">Die Anzahl der Seiten, die die kleinstmögliche temporäre Datenbank liefert.</span><span class="sxs-lookup"><span data-stu-id="3e628-274">The number of pages that gives the smallest possible temporary database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e628-275">Oben</span><span class="sxs-lookup"><span data-stu-id="3e628-275">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3e628-276">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e628-276">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e628-277">Referenz</span><span class="sxs-lookup"><span data-stu-id="3e628-277">Reference</span></span>

[<span data-ttu-id="3e628-278">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e628-278">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="3e628-279">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3e628-279">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
