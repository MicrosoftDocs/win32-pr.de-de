---
description: Weitere Informationen zu instanceparameters-Membern
title: Instanceparameters-Elemente
TOCTitle: InstanceParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_members(v=EXCHG.10)
ms:contentKeyID: 55103286
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8d52035b7473c17f9278a0343d12d957b2970349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552408"
---
# <a name="instanceparameters-members"></a><span data-ttu-id="84a97-103">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="84a97-103">InstanceParameters members</span></span>

<span data-ttu-id="84a97-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="84a97-104">Include protected members</span></span>  
<span data-ttu-id="84a97-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="84a97-105">Include inherited members</span></span>  

<span data-ttu-id="84a97-106">Diese Klasse stellt Eigenschaften bereit, um Systemparameter für eine ESENT-Instanz festzulegen und zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84a97-106">This class provides properties to set and get system parameters on an ESENT instance.</span></span> <span data-ttu-id="84a97-107">Diese Klasse stellt statische Eigenschaften bereit, um ESENT-Systemparameter pro Instanz festzulegen und zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84a97-107">This class provides static properties to set and get per-instance ESENT system parameters.</span></span>

<span data-ttu-id="84a97-108">Der [instanceparameters](./instanceparameters-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84a97-108">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="84a97-109">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="84a97-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="84a97-110">Name</span><span class="sxs-lookup"><span data-stu-id="84a97-110">Name</span></span></th>
<th><span data-ttu-id="84a97-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84a97-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="84a97-113"><a href="dn350965(v=exchg.10).md">Instanceparameters</a></span><span class="sxs-lookup"><span data-stu-id="84a97-113"><a href="dn350965(v=exchg.10).md">InstanceParameters</a></span></span></td>
<td><span data-ttu-id="84a97-114">Initialisiert eine neue Instanz der instanceparameters-Klasse.</span><span class="sxs-lookup"><span data-stu-id="84a97-114">Initializes a new instance of the InstanceParameters class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84a97-115">Oben</span><span class="sxs-lookup"><span data-stu-id="84a97-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="84a97-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84a97-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="84a97-117">Name</span><span class="sxs-lookup"><span data-stu-id="84a97-117">Name</span></span></th>
<th><span data-ttu-id="84a97-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84a97-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-120"><a href="dn350971(v=exchg.10).md">"Alternativen databaserecoverydirectory"</a></span><span class="sxs-lookup"><span data-stu-id="84a97-120"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="84a97-121">Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, in dem die Absturz Wiederherstellung oder ein Wiederherstellungs Vorgang die Datenbanken finden kann, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-121">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-123"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="84a97-123"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="84a97-124">Ruft das drei Buchstabe-Präfix für viele der Dateien ab, die von der Datenbank-Engine verwendet werden, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-124">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="84a97-125">Beispielsweise wird die Prüf Punkt Datei als EDB bezeichnet. Standardmäßig chk, da EDB der Standardbasis Name ist.</span><span class="sxs-lookup"><span data-stu-id="84a97-125">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-127"><a href="dn350951(v=exchg.10).md">Cachedclosedtables</a></span><span class="sxs-lookup"><span data-stu-id="84a97-127"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="84a97-128">Ruft einen Wert ab, der die Anzahl der B +-strukturressourcen angibt, die von der-Instanz zwischengespeichert wurden, nachdem die von Ihnen dargestellten Tabellen von der Anwendung geschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="84a97-128">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="84a97-129">Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="84a97-129">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="84a97-130">Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="84a97-130">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="84a97-131">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="84a97-131">Supported on Windows Vista and up.</span></span> <span data-ttu-id="84a97-132">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="84a97-132">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-134"><a href="dn350974(v=exchg.10).md">Cachepriority</a></span><span class="sxs-lookup"><span data-stu-id="84a97-134"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="84a97-135">Ruft die Eigenschaft pro Instanz für relative Cache Prioritäten (Standardwert = 100) ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-135">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-137"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="84a97-137"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="84a97-138">Ruft den Schwellenwert in Bytes für die Anzahl der Transaktionsprotokoll Dateien ab, die nach einem Absturz wiedergegeben werden müssen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-138">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="84a97-139">Wenn die zirkuläre Protokollierung mithilfe von circularlog aktiviert wird, steuert dieser Parameter auch die ungefähre Menge an Transaktionsprotokoll Dateien, die auf dem Datenträger aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="84a97-139">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-141"><a href="dn350977(v=exchg.10).md">Circularlog</a></span><span class="sxs-lookup"><span data-stu-id="84a97-141"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="84a97-142">Ruft einen Wert ab, der angibt, ob die zirkuläre Protokollierung on ist</span><span class="sxs-lookup"><span data-stu-id="84a97-142">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="84a97-143">Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokoll Dateien auf dem Datenträger gespeichert, bis Sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="84a97-143">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="84a97-144">Wenn die zirkuläre Protokollierung auf on festgehalten wird, werden nur Transaktionsprotokoll Dateien auf dem Datenträger beibehalten</span><span class="sxs-lookup"><span data-stu-id="84a97-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="84a97-145">Der Vorteil dieses Modus besteht darin, dass keine Sicherungen erforderlich sind, um alte Transaktionsprotokoll Dateien abzukoppeln.</span><span class="sxs-lookup"><span data-stu-id="84a97-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-147"><a href="dn350955(v=exchg.10).md">Cleanupmismatchedlogfiles</a></span><span class="sxs-lookup"><span data-stu-id="84a97-147"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="84a97-148">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob jetinit fehlschlägt, wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte</span><span class="sxs-lookup"><span data-stu-id="84a97-148">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="84a97-149">Normalerweise stellt <a href="dn292210(v=exchg.10).md">jetinit (JET_INSTANCE)</a> die Datenbanken erfolgreich wieder her, schlägt jedoch mit <a href="hh564840(v=exchg.10).md">logfilesizemismatchdatabaseskonsistente</a> fehl, um anzugeben, dass die Protokolldatei Größe falsch konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="84a97-149">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="84a97-150">Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien und startet mithilfe der konfigurierten Protokolldatei Größe einen neuen Satz von Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="84a97-150">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="84a97-151">Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="84a97-151">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-153"><a href="dn350978(v=exchg.10).md">"Kreatepthifnotexist"</a></span><span class="sxs-lookup"><span data-stu-id="84a97-153"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="84a97-154">Ruft einen Wert ab, der angibt, ob ESENT automatisch Ordner erstellt, die in den Dateisystem Pfaden fehlen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-154">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-156"><a href="dn350957(v=exchg.10).md">Dbextensionsize</a></span><span class="sxs-lookup"><span data-stu-id="84a97-156"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="84a97-157">Ruft die Anzahl der Seiten ab, die einer Datenbankdatei hinzugefügt werden, wenn Sie vergrößert werden muss, um mehr Daten aufzunehmen, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-157">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-159"><a href="dn350980(v=exchg.10).md">Dbscanintervalmaxsec</a></span><span class="sxs-lookup"><span data-stu-id="84a97-159"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="84a97-160">Dient zum Abrufen oder Festlegen des maximalen Intervalls, in dem der Datenbankscan abgeschlossen werden kann (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="84a97-160">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-162"><a href="dn350959(v=exchg.10).md">Dbscanintervalminsec</a></span><span class="sxs-lookup"><span data-stu-id="84a97-162"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="84a97-163">Ruft das Mindestintervall zum Wiederholen des Daten Bank Scans in Sekunden ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-163">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-165"><a href="dn350982(v=exchg.10).md">Dbscanthrottle</a></span><span class="sxs-lookup"><span data-stu-id="84a97-165"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="84a97-166">Ruft die Drosselung des Daten Bank Scans in Millisekunden ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-166">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-168"><a href="dn350961(v=exchg.10).md">Enabledbscaninrecovery</a></span><span class="sxs-lookup"><span data-stu-id="84a97-168"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="84a97-169">Ruft einen Wert ab, der angibt, ob die Datenbankwartung während der Wiederherstellung ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="84a97-169">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-171"><a href="dn350984(v=exchg.10).md">Enabledbscanserialization</a></span><span class="sxs-lookup"><span data-stu-id="84a97-171"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="84a97-172">Ruft einen Wert ab, der angibt, ob die Serialisierung der Datenbankwartung für Datenbanken aktiviert ist, die denselben Datenträger gemeinsam nutzen</span><span class="sxs-lookup"><span data-stu-id="84a97-172">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-174"><a href="dn350986(v=exchg.10).md">Enableindexcheck</a></span><span class="sxs-lookup"><span data-stu-id="84a97-174"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="84a97-175">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob <a href="dn292096(v=exchg.10).md">jetattachdatabase (JET_SESID, String, attachdatabasegrbit)</a> auf Indizes überprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="84a97-175">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-177"><a href="dn350963(v=exchg.10).md">Enableonlinedefrag</a></span><span class="sxs-lookup"><span data-stu-id="84a97-177"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="84a97-178">Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob die Online Defragmentierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="84a97-178">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-180"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="84a97-180"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="84a97-181">Ruft eine anwendungsspezifische Zeichenfolge ab oder legt diese fest, die beliebigen Ereignisprotokoll Meldungen hinzugefügt wird, die von der Datenbank-Engine ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="84a97-181">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="84a97-182">Dies ermöglicht eine einfache Korrelation von Ereignisprotokoll Meldungen mit der Quell Anwendung.</span><span class="sxs-lookup"><span data-stu-id="84a97-182">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="84a97-183">Standardmäßig wird der Name der ausführbaren Datei der Host Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="84a97-183">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-185"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="84a97-185"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="84a97-186">Ruft den Namen des Ereignis Protokolls ab, das von der Datenbank-Engine für seine Ereignisprotokoll Meldungen verwendet wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-186">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="84a97-187">Standardmäßig werden alle Ereignisprotokoll Meldungen an das Anwendungs Ereignisprotokoll gesendet.</span><span class="sxs-lookup"><span data-stu-id="84a97-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="84a97-188">Wenn der Registrierungsschlüssel Name für ein anderes Ereignisprotokoll konfiguriert ist, werden stattdessen die Ereignisprotokoll Meldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84a97-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-190"><a href="dn350968(v=exchg.10).md">Protokollpuffer</a></span><span class="sxs-lookup"><span data-stu-id="84a97-190"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="84a97-191">Dient zum Abrufen oder Festlegen des Speichers, der zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="84a97-191">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="84a97-192">Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="84a97-192">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="84a97-193">Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="84a97-193">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="84a97-194">Dieser Parameter wirkt sich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="84a97-194">This parameter has an impact on performance.</span></span> <span data-ttu-id="84a97-195">Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden.</span><span class="sxs-lookup"><span data-stu-id="84a97-195">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="84a97-196">Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung.</span><span class="sxs-lookup"><span data-stu-id="84a97-196">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="84a97-197">Der Standardwert ist für diesen Fall zu klein.</span><span class="sxs-lookup"><span data-stu-id="84a97-197">The default is known to be too small for this case.</span></span> <span data-ttu-id="84a97-198">Legen Sie diesen Parameter nicht auf eine größere Anzahl von Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-198">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-200"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span><span class="sxs-lookup"><span data-stu-id="84a97-200"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="84a97-201">Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Transaktionsprotokolle für die-Instanz enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-201">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-203"><a href="dn350969(v=exchg.10).md">Logfile size</a></span><span class="sxs-lookup"><span data-stu-id="84a97-203"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="84a97-204">Ruft die Größe der Transaktionsprotokoll Dateien ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-204">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="84a97-205">Dieser Parameter sollte in Einheiten von 1024 Bytes festgelegt werden (z. b. eine Einstellung von 2048 gibt 2 MB Protokolldateien aus).</span><span class="sxs-lookup"><span data-stu-id="84a97-205">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-207"><a href="dn350993(v=exchg.10).md">Maxcursors</a></span><span class="sxs-lookup"><span data-stu-id="84a97-207"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="84a97-208">Ruft die Anzahl der für diese Instanz reservierten Cursor Ressourcen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-208">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="84a97-209">Eine Cursor Ressource entspricht direkt einer JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="84a97-209">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-211"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="84a97-211"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="84a97-212">Ruft die Anzahl der für diese Instanz reservierten B +-strukturressourcen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-212">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-214"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="84a97-214"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="84a97-215">Ruft die Anzahl der für diese Instanz reservierten Sitzungs Ressourcen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-215">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="84a97-216">Eine Sitzungs Ressource entspricht direkt einer JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="84a97-216">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-218"><a href="dn350997(v=exchg.10).md">Maxtemporarytables</a></span><span class="sxs-lookup"><span data-stu-id="84a97-218"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="84a97-219">Ruft die Anzahl der temporären Tabellen Ressourcen für die Verwendung durch eine-Instanz ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-219">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="84a97-220">Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="84a97-220">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="84a97-221">Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die temporäre Datenbank benötigt, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="84a97-221">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="84a97-222">Diese Einstellung kann hilfreich sein, um die e/a-Vorgänge zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich sind, wenn bekannt ist, dass Sie nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84a97-222">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-224"><a href="dn350973(v=exchg.10).md">Maxtransaktionsize</a></span><span class="sxs-lookup"><span data-stu-id="84a97-224"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="84a97-225">Ruft den Prozentsatz des Versions Speichers ab, der von der ältesten Transaktion vor ' <a href="hh564840(v=exchg.10).md">versionstoreoudebmemory</a> ' (Standard = 100) verwendet werden kann, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-225">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-227"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="84a97-227"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="84a97-228">Ruft die maximale Anzahl von Versionsspeicher Seiten ab, die für diese Instanz reserviert sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-228">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-230"><a href="dn351001(v=exchg.10).md">Noinformationevent</a></span><span class="sxs-lookup"><span data-stu-id="84a97-230"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="84a97-231">Ruft einen Wert ab, der angibt, ob Informations Ereignisprotokoll-Meldungen, die normalerweise von der Datenbank-Engine generiert werden, unterdrückt werden</span><span class="sxs-lookup"><span data-stu-id="84a97-231">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-233"><a href="dn350976(v=exchg.10).md">Onedatabasepersession</a></span><span class="sxs-lookup"><span data-stu-id="84a97-233"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="84a97-234">Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob nur eine Datenbank gleichzeitig von einer bestimmten Sitzung geöffnet werden darf.</span><span class="sxs-lookup"><span data-stu-id="84a97-234">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="84a97-235">Die temporäre Datenbank wird von dieser Einschränkung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="84a97-235">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-237"><a href="dn351002(v=exchg.10).md">Pagetempdbmin</a></span><span class="sxs-lookup"><span data-stu-id="84a97-237"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="84a97-238">Ruft die Anfangs Größe der temporären Datenbank ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-238">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="84a97-239">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="84a97-239">The size is in database pages.</span></span> <span data-ttu-id="84a97-240">Eine Größe von NULL gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84a97-240">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="84a97-241">Häufig ist es wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="84a97-241">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="84a97-242">Wenn Sie diesen Parameter auf <a href="dn351211(v=exchg.10).md">pagetempdbkleinsten</a> festlegen, wird die kleinste temporäre Datenbank erreicht.</span><span class="sxs-lookup"><span data-stu-id="84a97-242">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-244"><a href="dn350979(v=exchg.10).md">Preferredverpages</a></span><span class="sxs-lookup"><span data-stu-id="84a97-244"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="84a97-245">Ruft die bevorzugte Anzahl von Versionsspeicher Seiten ab, die für diese Instanz reserviert sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-245">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="84a97-246">Wenn die Größe des Versionsspeicher diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. b. das Freigeben von gelöschtem Speicherplatz in der Datenbank, stattdessen geopfert, um Platz für Transaktionsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84a97-246">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-248"><a href="dn351004(v=exchg.10).md">Vorabversion</a></span><span class="sxs-lookup"><span data-stu-id="84a97-248"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="84a97-249">Dient zum Abrufen oder Festlegen der maximalen Anzahl von e/a-Vorgängen, die für einen bestimmten Zweck gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="84a97-249">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-251"><a href="dn350981(v=exchg.10).md">Wiederherstellung</a></span><span class="sxs-lookup"><span data-stu-id="84a97-251"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="84a97-252">Ruft einen Wert ab, der angibt, ob die Wiederherstellung von Abstürzen ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="84a97-252">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-254"><a href="dn351007(v=exchg.10).md">System Directory</a></span><span class="sxs-lookup"><span data-stu-id="84a97-254"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="84a97-255">Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Prüf Punkt Datei für die-Instanz enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-255">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-257"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="84a97-257"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="84a97-258">Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die temporäre Datenbank für die-Instanz enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-258">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-260"><a href="dn351008(v=exchg.10).md">Versionstoretaskqueuemax</a></span><span class="sxs-lookup"><span data-stu-id="84a97-260"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="84a97-261">Dient zum Abrufen oder Festlegen der Anzahl von Arbeitsaufgaben im Hintergrund Bereinigung, die zu einem beliebigen Zeitpunkt in die Warteschlange des Thread Pools der Datenbank-Engine eingereiht werden können.</span><span class="sxs-lookup"><span data-stu-id="84a97-261">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="84a97-263"><a href="dn350985(v=exchg.10).md">Waypointlatency</a></span><span class="sxs-lookup"><span data-stu-id="84a97-263"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="84a97-264">Ruft die Anzahl der Protokolle ab, für die ESENT Daten Bank Leerungen zurück stellt, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="84a97-264">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="84a97-265">Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler beim Verlust von Protokolldateien auftreten.</span><span class="sxs-lookup"><span data-stu-id="84a97-265">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="84a97-266">Unter Windows 7 und aufwärts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84a97-266">Supported on Windows 7 and up.</span></span> <span data-ttu-id="84a97-267">Wird unter Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="84a97-267">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84a97-268">Oben</span><span class="sxs-lookup"><span data-stu-id="84a97-268">Top</span></span>

## <a name="methods"></a><span data-ttu-id="84a97-269">Methoden</span><span class="sxs-lookup"><span data-stu-id="84a97-269">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="84a97-270">Name</span><span class="sxs-lookup"><span data-stu-id="84a97-270">Name</span></span></th>
<th><span data-ttu-id="84a97-271">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84a97-271">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="84a97-273"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="84a97-273"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="84a97-274">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="84a97-274">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="84a97-276"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="84a97-276"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="84a97-277">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="84a97-277">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="84a97-279"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="84a97-279"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="84a97-280">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="84a97-280">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="84a97-282"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="84a97-282"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="84a97-283">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="84a97-283">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="84a97-285"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="84a97-285"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="84a97-286">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="84a97-286">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="84a97-288"><a href="dn350967(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="84a97-288"><a href="dn350967(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="84a97-289">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuellen <a href="dn350942(v=exchg.10).md">instanceparameters</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="84a97-289">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350942(v=exchg.10).md">InstanceParameters</a>.</span></span> <span data-ttu-id="84a97-290">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="84a97-290">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84a97-291">Oben</span><span class="sxs-lookup"><span data-stu-id="84a97-291">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="84a97-292">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a97-292">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84a97-293">Referenz</span><span class="sxs-lookup"><span data-stu-id="84a97-293">Reference</span></span>

[<span data-ttu-id="84a97-294">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="84a97-294">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="84a97-295">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="84a97-295">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
