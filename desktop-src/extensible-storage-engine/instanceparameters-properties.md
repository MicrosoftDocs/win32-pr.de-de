---
description: 'Weitere Informationen zu: InstanceParameters-Eigenschaften'
title: InstanceParameters-Eigenschaften
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1db9933e6e0a14b770e4250fc7e1faf564d3266ee258bfa71671093dceee763a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721160"
---
# <a name="instanceparameters-properties"></a>InstanceParameters-Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [InstanceParameters-Typ](./instanceparameters-class.md) macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad eines Ordners ab, in dem die Absturzwiederherstellung oder ein Wiederherstellungsvorgang die Datenbanken finden kann, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird, oder legt den Pfad fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">Basename</a></td>
<td>Ruft das Präfix mit drei Buchstaben ab, das für viele der von der Datenbank-Engine verwendeten Dateien verwendet wird, oder legt dieses fest. Die Prüfpunktdatei heißt beispielsweise EDB. CHK standardmäßig, da EDB der Standardbasisname ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Ruft einen Wert ab, der die Anzahl der von der Instanz zwischengespeicherten B+-Strukturressourcen angibt, nachdem die von ihnen dargestellten Tabellen von der Anwendung geschlossen wurden, oder legt diesen fest. Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, erhöht jedoch die Geschwindigkeit, mit der eine große Anzahl von Tabellen von der Anwendung nach dem Zufallsprinzip geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen. Wird ab Windows Vista unterstützt. Wird auf Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Ruft die Instanzeigenschaft für relative Cacheprioritäten ab (Standardwert = 100), oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Ruft den Schwellenwert in Bytes ab, der angibt, wie viele Transaktionsprotokolldateien nach einem Absturz wiedergegeben werden müssen, oder legt diesen fest. Wenn die zirkuläre Protokollierung mit CircularLog aktiviert ist, steuert dieser Parameter auch die ungefähre Menge der Transaktionsprotokolldateien, die auf dem Datenträger beibehalten werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Ruft einen Wert ab, der angibt, ob die zirkuläre Protokollierung eingeschaltet ist, oder legt einen Wert fest. Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokolldateien auf dem Datenträger beibehalten, bis sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank durchgeführt wurde. Wenn die zirkuläre Protokollierung aktiviert ist, werden nur Transaktionsprotokolldateien, die älter als der aktuelle Prüfpunkt sind, auf dem Datenträger beibehalten. Der Vorteil dieses Modus besteht darin, dass sicherungen nicht erforderlich sind, um alte Transaktionsprotokolldateien abzumelden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Ruft einen Wert ab, der angibt, ob JetInit fehlschlägt, wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokolldateien auf datenträgern konfiguriert ist, die eine andere Größe als die konfigurierte aufweisen, oder legt diesen fest. Normalerweise stellt <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> die Datenbanken erfolgreich wieder her, schlägt jedoch mit <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> fehl, um anzugeben, dass die Größe der Protokolldatei falsch konfiguriert ist. Wenn dieser Parameter jedoch auf TRUE festgelegt ist, löscht die Datenbank-Engine im Hintergrund alle alten Protokolldateien. Starten Sie mithilfe der konfigurierten Protokolldateigröße einen neuen Satz von Transaktionsprotokolldateien. Dieser Parameter ist nützlich, wenn die Anwendung die Größe der Transaktionsprotokolldatei transparent ändern möchte, in Upgrade- und Wiederherstellungsszenarien aber trotzdem transparent funktioniert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Ruft einen Wert ab, der angibt, ob ESENT automatisch Ordner erstellt, die in den Dateisystempfaden fehlen, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Ruft die Anzahl der Seiten ab, die einer Datenbankdatei jedes Mal hinzugefügt werden, wenn sie vergrößert werden muss, um mehr Daten aufzunehmen, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Ruft das maximale Intervall in Sekunden ab, mit dem der Datenbankscan abgeschlossen werden kann, oder legt dieses fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Ruft das minimale Intervall für die Wiederholung des Datenbankscans in Sekunden ab oder legt dieses fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Ruft die Drosselung des Datenbankscans in Millisekunden ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbankwartung während der Wiederherstellung ausgeführt werden soll, oder legt einen Wert fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Serialisierung der Datenbankwartung für Datenbanken aktiviert ist, die denselben Datenträger gemeinsam nutzen, oder legt den Wert fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Ruft einen Wert ab, der angibt, ob <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> nach Indizes sucht, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Onlinedefragmentierung aktiviert ist, oder legt einen Wert fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Ruft eine anwendungsspezifische Zeichenfolge ab, die allen Ereignisprotokollmeldungen hinzugefügt wird, die von der Datenbank-Engine ausgegeben werden, oder legt diese fest. Dies ermöglicht eine einfache Korrelation von Ereignisprotokollmeldungen mit der Quellanwendung. Standardmäßig wird der ausführbare Name der Hostanwendung verwendet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Ruft den Namen des Ereignisprotokolls ab, das die Datenbank-Engine für die Ereignisprotokollmeldungen verwendet, oder legt dieses fest. Standardmäßig werden alle Ereignisprotokollmeldungen an das Anwendungsereignisprotokoll geleitet. Wenn der Registrierungsschlüsselname für ein anderes Ereignisprotokoll konfiguriert ist, werden die Ereignisprotokollmeldungen stattdessen dorthin verschoben.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>Ruft den Arbeitsspeicher ab, der zum Zwischenspeichern von Protokolldatensätzen verwendet wird, bevor sie in die Transaktionsprotokolldatei geschrieben werden, oder legt diesen fest. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokolldateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, daher ist es sicher, diese Größe für die Einheit anzunehmen. Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell voll werden. Eine größere Cachegröße für die Transaktionsprotokolldatei ist entscheidend für eine gute Updateleistung unter einem solchen hohen Auslastungszustand. Der Standardwert ist für diesen Fall bekanntlich zu klein. Legen Sie diesen Parameter nicht auf eine Anzahl von Puffern fest, die größer (in Bytes) als die Hälfte der Größe einer Transaktionsprotokolldatei ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Transaktionsprotokolle für die Instanz enthält, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Ruft die Größe der Transaktionsprotokolldateien ab oder legt diese fest. Dieser Parameter sollte in Einheiten von 1.024 Byte festgelegt werden (z.B. gibt eine Einstellung von 2048 2 MB Protokolldateien).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Ruft die Anzahl der cursor-Ressourcen ab, die für diese Instanz reserviert sind, oder legt diese fest. Eine Cursorressource entspricht direkt einem JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Ruft die Anzahl der für diese Instanz reservierten B+-Strukturressourcen ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Ruft die Anzahl der Sitzungsressourcen ab, die für diese Instanz reserviert sind, oder legt diese fest. Eine Sitzungsressource entspricht direkt einem JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Ruft die Anzahl der temporären Tabellenressourcen ab, die von einer -Instanz verwendet werden, oder legt diese fest. Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können. Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die Verwendung der temporären Datenbank erfordert, erzeugt einen Fehler. Diese Einstellung kann nützlich sein, um die E/A zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich ist, wenn bekannt ist, dass sie nicht verwendet wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Ruft den Prozentsatz des Versionsspeichers ab, der von der ältesten Transaktion vor <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (Standardwert = 100) verwendet werden kann, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Ruft die maximale Anzahl von Versionsspeicherseiten ab, die für diese Instanz reserviert sind, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Ruft einen Wert ab, der angibt, ob Informationsereignisprotokollmeldungen, die normalerweise von der Datenbank-Engine generiert werden, unterdrückt werden, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Ruft einen Wert ab, der angibt, ob nur eine Datenbank mit JetOpenDatabase von einer bestimmten Sitzung gleichzeitig geöffnet werden darf, oder legt einen Wert fest. Die temporäre Datenbank ist von dieser Einschränkung ausgeschlossen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Ruft die Anfangsgröße der temporären Datenbank ab oder legt diese fest. Die Größe befindet sich auf Datenbankseiten. Eine Größe von 0 (null) gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll. Es ist häufig wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren. Wenn Sie diesen Parameter auf <a href="dn351211(v=exchg.10).md">PageTempDBSmallest festlegen,</a> wird die kleinste temporäre Datenbank erreicht, die möglich ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Ruft die bevorzugte Anzahl von Versionsspeicherseiten ab, die für diese Instanz reserviert sind, oder legt diese fest. Wenn die Größe des Versionsspeichers diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. B. das Wiederverlangen von gelöschtem Speicherplatz in der Datenbank, stattdessen verfemt, um Platz für Transaktionsinformationen zu erhalten.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Ruft die maximale Anzahl von E/A-Vorgängen ab, die für einen bestimmten Zweck versendet werden, oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Wiederherstellung</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Absturzwiederherstellung eingeht, oder legt einen Wert fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Prüfpunktdatei für die Instanz enthalten soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die temporäre Datenbank für die Instanz enthalten soll, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Ruft die Anzahl der Arbeitselemente für die Hintergrundbereinigung ab, die jederzeit im Datenbank-Engine-Threadpool in die Warteschlange gestellt werden können, oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Ruft die Anzahl von Protokollen ab, für die Datenbank geleert wird, oder legt diese fest. Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler dazu führen, dass Protokolldateien verloren gehen. Wird ab Windows 7 unterstützt. Wird auf Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 ignoriert.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[InstanceParameters-Klasse](./instanceparameters-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
