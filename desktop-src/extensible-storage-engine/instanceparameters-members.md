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
# <a name="instanceparameters-members"></a>Instanceparameters-Elemente

Geschützte Member einschließen  
Geerbte Member einschließen  

Diese Klasse stellt Eigenschaften bereit, um Systemparameter für eine ESENT-Instanz festzulegen und zu erhalten. Diese Klasse stellt statische Eigenschaften bereit, um ESENT-Systemparameter pro Instanz festzulegen und zu erhalten.

Der [instanceparameters](./instanceparameters-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="constructors"></a>Konstruktoren

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350965(v=exchg.10).md">Instanceparameters</a></td>
<td>Initialisiert eine neue Instanz der instanceparameters-Klasse.</td>
</tr>
</tbody>
</table>


Oben

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">"Alternativen databaserecoverydirectory"</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, in dem die Absturz Wiederherstellung oder ein Wiederherstellungs Vorgang die Datenbanken finden kann, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird, oder legt ihn fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>Ruft das drei Buchstabe-Präfix für viele der Dateien ab, die von der Datenbank-Engine verwendet werden, oder legt dieses fest. Beispielsweise wird die Prüf Punkt Datei als EDB bezeichnet. Standardmäßig chk, da EDB der Standardbasis Name ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">Cachedclosedtables</a></td>
<td>Ruft einen Wert ab, der die Anzahl der B +-strukturressourcen angibt, die von der-Instanz zwischengespeichert wurden, nachdem die von Ihnen dargestellten Tabellen von der Anwendung geschlossen wurden Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen. Unterstützt unter Windows Vista und up. Wird unter Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">Cachepriority</a></td>
<td>Ruft die Eigenschaft pro Instanz für relative Cache Prioritäten (Standardwert = 100) ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Ruft den Schwellenwert in Bytes für die Anzahl der Transaktionsprotokoll Dateien ab, die nach einem Absturz wiedergegeben werden müssen, oder legt diesen fest. Wenn die zirkuläre Protokollierung mithilfe von circularlog aktiviert wird, steuert dieser Parameter auch die ungefähre Menge an Transaktionsprotokoll Dateien, die auf dem Datenträger aufbewahrt werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">Circularlog</a></td>
<td>Ruft einen Wert ab, der angibt, ob die zirkuläre Protokollierung on ist Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokoll Dateien auf dem Datenträger gespeichert, bis Sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank ausgeführt wurde. Wenn die zirkuläre Protokollierung auf on festgehalten wird, werden nur Transaktionsprotokoll Dateien auf dem Datenträger beibehalten Der Vorteil dieses Modus besteht darin, dass keine Sicherungen erforderlich sind, um alte Transaktionsprotokoll Dateien abzukoppeln.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">Cleanupmismatchedlogfiles</a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob jetinit fehlschlägt, wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte Normalerweise stellt <a href="dn292210(v=exchg.10).md">jetinit (JET_INSTANCE)</a> die Datenbanken erfolgreich wieder her, schlägt jedoch mit <a href="hh564840(v=exchg.10).md">logfilesizemismatchdatabaseskonsistente</a> fehl, um anzugeben, dass die Protokolldatei Größe falsch konfiguriert ist. Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien und startet mithilfe der konfigurierten Protokolldatei Größe einen neuen Satz von Transaktionsprotokoll Dateien. Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">"Kreatepthifnotexist"</a></td>
<td>Ruft einen Wert ab, der angibt, ob ESENT automatisch Ordner erstellt, die in den Dateisystem Pfaden fehlen, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">Dbextensionsize</a></td>
<td>Ruft die Anzahl der Seiten ab, die einer Datenbankdatei hinzugefügt werden, wenn Sie vergrößert werden muss, um mehr Daten aufzunehmen, oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">Dbscanintervalmaxsec</a></td>
<td>Dient zum Abrufen oder Festlegen des maximalen Intervalls, in dem der Datenbankscan abgeschlossen werden kann (in Sekunden).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">Dbscanintervalminsec</a></td>
<td>Ruft das Mindestintervall zum Wiederholen des Daten Bank Scans in Sekunden ab oder legt es fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">Dbscanthrottle</a></td>
<td>Ruft die Drosselung des Daten Bank Scans in Millisekunden ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">Enabledbscaninrecovery</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbankwartung während der Wiederherstellung ausgeführt werden soll</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">Enabledbscanserialization</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Serialisierung der Datenbankwartung für Datenbanken aktiviert ist, die denselben Datenträger gemeinsam nutzen</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">Enableindexcheck</a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob <a href="dn292096(v=exchg.10).md">jetattachdatabase (JET_SESID, String, attachdatabasegrbit)</a> auf Indizes überprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">Enableonlinedefrag</a></td>
<td>Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob die Online Defragmentierung aktiviert ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Ruft eine anwendungsspezifische Zeichenfolge ab oder legt diese fest, die beliebigen Ereignisprotokoll Meldungen hinzugefügt wird, die von der Datenbank-Engine ausgegeben werden. Dies ermöglicht eine einfache Korrelation von Ereignisprotokoll Meldungen mit der Quell Anwendung. Standardmäßig wird der Name der ausführbaren Datei der Host Anwendung verwendet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Ruft den Namen des Ereignis Protokolls ab, das von der Datenbank-Engine für seine Ereignisprotokoll Meldungen verwendet wird, oder legt diesen fest. Standardmäßig werden alle Ereignisprotokoll Meldungen an das Anwendungs Ereignisprotokoll gesendet. Wenn der Registrierungsschlüssel Name für ein anderes Ereignisprotokoll konfiguriert ist, werden stattdessen die Ereignisprotokoll Meldungen angezeigt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">Protokollpuffer</a></td>
<td>Dient zum Abrufen oder Festlegen des Speichers, der zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird. Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden. Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung. Der Standardwert ist für diesen Fall zu klein. Legen Sie diesen Parameter nicht auf eine größere Anzahl von Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Transaktionsprotokolle für die-Instanz enthält, oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">Logfile size</a></td>
<td>Ruft die Größe der Transaktionsprotokoll Dateien ab oder legt Sie fest. Dieser Parameter sollte in Einheiten von 1024 Bytes festgelegt werden (z. b. eine Einstellung von 2048 gibt 2 MB Protokolldateien aus).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">Maxcursors</a></td>
<td>Ruft die Anzahl der für diese Instanz reservierten Cursor Ressourcen ab oder legt Sie fest. Eine Cursor Ressource entspricht direkt einer JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Ruft die Anzahl der für diese Instanz reservierten B +-strukturressourcen ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Ruft die Anzahl der für diese Instanz reservierten Sitzungs Ressourcen ab oder legt Sie fest. Eine Sitzungs Ressource entspricht direkt einer JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">Maxtemporarytables</a></td>
<td>Ruft die Anzahl der temporären Tabellen Ressourcen für die Verwendung durch eine-Instanz ab oder legt diese fest. Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können. Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die temporäre Datenbank benötigt, schlägt fehl. Diese Einstellung kann hilfreich sein, um die e/a-Vorgänge zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich sind, wenn bekannt ist, dass Sie nicht verwendet wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">Maxtransaktionsize</a></td>
<td>Ruft den Prozentsatz des Versions Speichers ab, der von der ältesten Transaktion vor ' <a href="hh564840(v=exchg.10).md">versionstoreoudebmemory</a> ' (Standard = 100) verwendet werden kann, oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Ruft die maximale Anzahl von Versionsspeicher Seiten ab, die für diese Instanz reserviert sind, oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">Noinformationevent</a></td>
<td>Ruft einen Wert ab, der angibt, ob Informations Ereignisprotokoll-Meldungen, die normalerweise von der Datenbank-Engine generiert werden, unterdrückt werden</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">Onedatabasepersession</a></td>
<td>Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob nur eine Datenbank gleichzeitig von einer bestimmten Sitzung geöffnet werden darf. Die temporäre Datenbank wird von dieser Einschränkung ausgeschlossen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">Pagetempdbmin</a></td>
<td>Ruft die Anfangs Größe der temporären Datenbank ab oder legt Sie fest. Die Größe befindet sich auf Datenbankseiten. Eine Größe von NULL gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll. Häufig ist es wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren. Wenn Sie diesen Parameter auf <a href="dn351211(v=exchg.10).md">pagetempdbkleinsten</a> festlegen, wird die kleinste temporäre Datenbank erreicht.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">Preferredverpages</a></td>
<td>Ruft die bevorzugte Anzahl von Versionsspeicher Seiten ab, die für diese Instanz reserviert sind, oder legt Sie fest. Wenn die Größe des Versionsspeicher diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. b. das Freigeben von gelöschtem Speicherplatz in der Datenbank, stattdessen geopfert, um Platz für Transaktionsinformationen zu erhalten.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">Vorabversion</a></td>
<td>Dient zum Abrufen oder Festlegen der maximalen Anzahl von e/a-Vorgängen, die für einen bestimmten Zweck gesendet werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Wiederherstellung</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Wiederherstellung von Abstürzen ausgeführt wird</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">System Directory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Prüf Punkt Datei für die-Instanz enthält, oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die temporäre Datenbank für die-Instanz enthält, oder legt ihn fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">Versionstoretaskqueuemax</a></td>
<td>Dient zum Abrufen oder Festlegen der Anzahl von Arbeitsaufgaben im Hintergrund Bereinigung, die zu einem beliebigen Zeitpunkt in die Warteschlange des Thread Pools der Datenbank-Engine eingereiht werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">Waypointlatency</a></td>
<td>Ruft die Anzahl der Protokolle ab, für die ESENT Daten Bank Leerungen zurück stellt, oder legt Sie fest. Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler beim Verlust von Protokolldateien auftreten. Unter Windows 7 und aufwärts unterstützt. Wird unter Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 ignoriert.</td>
</tr>
</tbody>
</table>


Oben

## <a name="methods"></a>Methoden

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350967(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuellen <a href="dn350942(v=exchg.10).md">instanceparameters</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
