---
description: Weitere Informationen finden Sie unter Datenbankparameter.
title: Datenbankparameter
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: cdccfca7e7a68ea997c9b564939f89799634e344
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471836"
---
# <a name="database-parameters"></a>Datenbankparameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-parameters"></a>Datenbankparameter

Dieses Thema enthält Parameter, die für die Datenbank verwendet werden.

*JET_paramCheckFormatWhenOpenFail*  
44  

Wenn dieser Parameter festgelegt ist, gibt [JetInit](./jetinit-function.md) einen speziellen Fehler zurück, wenn eine Datenbank oder ein Transaktionsprotokoll aus einer früheren Version der Datenbank-Engine geöffnet wird. Diese Fehler sind:


| <p>Fehler</p> | <p>BESCHREIBUNG</p> | 
|--------------|--------------------|
| <p>JET_errDatabase200Format</p> | <p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in Windows NT 3.51 erstellt.</p> | 
| <p>JET_errDatabase400Format</p> | <p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in einer Testversion vor Windows NT Server 4.0 erstellt.</p> | 
| <p>JET_errDatabase500Format</p> | <p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in Windows NT Server 4.0 erstellt.</p> | 



**Windows Vista:**  Für Windows Vista und höher ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| | | <p>Standardwert:</p> | <p>True</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramDatabasePageSize*  
64  

Dieser Parameter konfiguriert die Seitengröße für die Datenbank. Die Seitengröße ist die kleinste Einheit der Speicherplatzzuweisung, die für eine Datenbankdatei möglich ist. Die Seitengröße der Datenbank ist ebenfalls sehr wichtig, da sie die Obergrenze für die Größe eines einzelnen Datensatzes in der Datenbank fest legt.

**Hinweis:** Derzeit wird pro Prozess nur eine Datenbankseitengröße unterstützt. Wenn Sie sich also in einem einzigen Prozess befinden, der verschiedene Anwendungen enthält, die die Datenbank-Engine verwenden, müssen sich alle auf eine Datenbankseitengröße einigen.


| | | <p>Standardwert:</p> | <p>4096</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>2048, 4096, 8192</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramDbExtensionSize*  
18  

Dieser Parameter steuert den Speicherplatz, der einer Datenbankdatei jedes Mal hinzugefügt wird, wenn sie wachsen muss, um mehr Daten aufnehmen zu können. Die Größe befindet sich auf Datenbankseiten.


| | | <p>Standardwert:</p> | <p>256</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>1 – 2147483647</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p><p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramEnableIndexChecking*  
45  

Wenn dieser Parameter true ist, wird jede Datenbank zur [JetAttachDatabase-Zeit](./jetattachdatabase-function.md) auf Indizes über Unicode-Schlüsselspalten überprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden. Dies muss geschehen, da die Datenbank-Engine die von [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) generierten Sortierschlüssel beibehält und sich der Wert dieser Sortierschlüssel von Release zu Release ändert.

Wenn ein primärer Index erkannt wird, der sich in diesem Zustand befindet, schlägt [JetAttachDatabase](./jetattachdatabase-function.md) immer mit JET_errPrimaryIndexCorrupted fehl.

Wenn sekundäre Indizes erkannt werden, die sich in diesem Zustand befinden, gibt es zwei mögliche Ergebnisse. Wenn JET_bitDbDeleteCorruptIndexes an [JetAttachDatabase](./jetattachdatabase-function.md) übergeben wurde, werden diese Indizes gelöscht, und JET_wrnCorruptIndexDeleted werden von [JetAttachDatabase](./jetattachdatabase-function.md)zurückgegeben. Diese Indizes müssen von Ihrer Anwendung neu erstellt werden. Wenn JET_bitDbDeleteCorruptIndexes nicht an [JetAttachDatabase](./jetattachdatabase-function.md) übergeben wurde, schlägt der Aufruf mit JET_errSecondaryIndexCorrupted fehl.

**Hinweis** Es wird dringend empfohlen, diesen Parameter von Ihrer Anwendung auf True festzulegen.

**Hinweis** Es wird dringend empfohlen, dass Anwendungen die Verwendung von Unicode-Schlüsselspalten in ihren Primärschlüsselindizes (gruppiert) vermeiden.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Global</p><p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Nein</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramEnableIndexCleanup*  
54  

Wenn dieser Parameter auf TRUE festgelegt ist, bereinigt die Datenbank-Engine indizes über Unicode-Schlüsselspalten bei Bedarf automatisch zur [JetInit-Zeit,](./jetinit-function.md) um Änderungen des Datenbankformats zu vermeiden, die durch Änderungen an der NLS-Bibliothek in Windows verursacht werden. Solche Änderungen werden routinemäßig an der NLS-Bibliothek vorgenommen, um Unterstützung für neue Sprachen hinzuzufügen, einer Sprache fehlende Zeichen hinzuzufügen, einer Sprache eine Sortierungsreihenfolge hinzuzufügen oder Fehler in der Sortierungsreihenfolge einer Sprache zu beheben. Diese Änderungen wirken sich auf die von [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) erzeugten Sortierschlüssel aus, die von der Datenbank-Engine als Komponenten von Indexschlüsseln beibehalten werden.

Es ist wichtig zu beachten, dass die Änderungen am Index so groß sein können, dass eine inkrementelle Bereinigung nicht möglich ist. In diesem Fall wird der Index wie von **JET_paramEnableIndexChecking** vorgeschrieben behandelt.

**Hinweis** Es wird dringend empfohlen, dass dieser Parameter und **JET_paramEnableIndexChecking** von Ihrer Anwendung auf **True** festgelegt werden.


| | | <p>Standardwert:</p> | <p>True</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p><p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows Releases von Server 2003 und höher</p> | 



*JET_paramOneDatabasePerSession*  
102  

Wenn dieser Parameter true ist, darf nur eine Datenbank mit [JetOpenDatabase](./jetopendatabase-function.md) von einer bestimmten Sitzung gleichzeitig geöffnet werden. Die temporäre Datenbank wird von dieser Einschränkung ausgeschlossen.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird nur auf Windows XP und Windows Server 2003 geschrieben.

**Windows Vista:**  Dieser Parameter verhält sich normal ab Windows Vista.

**Hinweis**  Dieser Parameter wird nur geschrieben.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Nein</p><p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramEnableOnlineDefrag*  
35  

Dieser Parameter steuert das Verhalten der Onlinedefragmentierung, wenn es mit [JetDefragment](./jetdefragment-function.md)initiiert wird. Weitere Informationen finden Sie unter [JetDefragment.](./jetdefragment-function.md)

Windows 2000: Am Windows 2000 war dieser Parameter ein einfacher boolescher Wert, der die Onlinedefragmentierung eingrenzte, wenn er von [JetDefragment](./jetdefragment-function.md)initiiert wurde. Bei Festlegung auf **TRUE** wird die Onlinedefragmentierung für die Datensätze jeder Tabelle in der Datenbank ausgeführt.

**Windows XP:**  Bei Windows XP und späteren Versionen kann dieser Parameter auf eine oder mehrere der folgenden Optionen festgelegt werden:


| <p>Option</p> | <p>BESCHREIBUNG</p> | 
|---------------|--------------------|
| <p>JET_OnlineDefragDisable</p> | <p>Führen Sie keine Onlinedefragmentierung durch. Dies ist die Binärdatei, die der Windows 2000-Einstellung false für diesen Parameter entspricht.</p> | 
| <p>JET_OnlineDefragAllOBSOLETE</p> | <p>Führen Sie die vollständige Onlinedefragmentierung durch. Dies ist die Binärdatei, die der einstellung Windows 2000 von True für diesen Parameter entspricht.</p> | 
| <p>JET_OnlineDefragDatabases</p> | <p>Führen Sie die Onlinedefragmentierung der Datensätze der einzelnen Tabellen in der Datenbank durch.</p> | 
| <p>JET_OnlineDefragSpaceTrees</p> | <p>Führen Sie die Onlinedefragmentierung der Platzstrukturen der einzelnen Tabellen in der Datenbank durch.</p> | 
| <p>JET_OnlineDefragStreamingFiles</p> | <p>Dieser Parameter wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 
| <p>JET_OnlineDefragAll</p> | <p>Führen Sie die vollständige Onlinedefragmentierung durch. Dies ist das konzeptionelle Äquivalent zur einstellung Windows 2000 von True für diesen Parameter.</p> | 




| | | <p>Standardwert:</p> | <p><strong>Windows 2000:</strong>  STIMMT</p><p><strong>Windows XP: Für Windows XP und höher:</strong> JET_OnlineDefragAll</p> | | <p>Typ:</p> | <p><strong>Windows 2000:</strong>  Boolean</p><p><strong>Windows XP und höher:</strong>  JET_GRBIT (integer)</p> | | <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong>  False, True</p><p><strong>Windows XP und höher:</strong> 0 – JET_OnlineDefragAll</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Ja</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramPageFragment*  
20  

Dieser Parameter ist der Schwellenwert, den die Datenbank-Engine verwendet, um die Fragmentierung des freien Speicherplatzes zu steuern. Die Größe befindet sich auf Datenbankseiten.


| | | <p>Standardwert:</p> | <p>8</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramRecordUpgradeDirtyLevel*  
78

Dieser Parameter steuert, wie aggressiv der Cache-Manager für Datenbankseiten eine Datenbankseite schreibt, die einer konvertierungsseitigen Formatkonvertierung unterzogen wurde. Diese Formatkonvertierungen erfolgen während des Ladens von Seiten aus einer Datenbank, die mit der Windows 2000-Datenbank-Engine erstellt, aber von einer Windows XP- oder einer späteren Version der Datenbank-Engine verwendet wurde.


| | | <p>Standardwert:</p> | <p>1</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-3</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramWaypointLatency*  
153  

Die Latenz (in Protokollen) hinter dem Trinkgeld/protokoll mit dem höchsten Commit zum Zurücklassen von Datenbankseiten geleert. Wenn Sie diese Latenz aktivieren, kann die Datenbankwiederherstellung im Falle eines schwerwiegenden Verlusts der letzten Protokolldatei möglich sein. Siehe JET_bitReplayIgnoreLostLogs.


| | | <p>Standardwert:</p> | <p>0</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-1023</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Ja</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTrees*  
160  

Aktivieren/deaktivieren Sie die automatische sequenzielle B-Strukturdefragmentierung.


| | | <p>Standardwert:</p> | <p>1</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>0-1</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Bestimmt, wie häufig die B-Strukturdichte überprüft wird.


| | | <p>Standardwert:</p> | <p>10</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-Max Integer</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramIOThrottlingTimeQuanta*  
162  

Die maximale Zeit in Millisekunden, die der E/A-Drosselungsmechanismus einer Auszuführenden Aufgabe zur Vergibt, damit sie als "abgeschlossen" betrachtet wird.


| | | <p>Standardwert:</p> | <p>125</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-10000</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
