---
description: 'Weitere Informationen zu: Sicherungs- und Wiederherstellungsparameter'
title: Sicherungs- und Wiederherstellungsparameter
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: d6b82d3ffa1f55d79ac516ede469d422e7aced99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982963"
---
# <a name="backup-and-restore-parameters"></a>Sicherungs- und Wiederherstellungsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Sicherungs- und Wiederherstellungsparameter

Dieses Thema enthält Parameter, die für die Sicherung und Wiederherstellung verwendet werden.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktionsprotokollen beibehalten. Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktionswiedergabe ordnungsgemäß funktioniert. Dieser Parameter kann verwendet werden, um die Wiederherstellung nach einem Absturz oder einen Wiederherstellungsvorgang zu erzwingen, um nach den Datenbanken zu suchen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>""</p> | 
| <p>Typ:</p> | <p>Ordnerpfad (Zeichenfolge)</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 246 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Dieser Parameter steuert das Ergebnis von [JetInit,](./jetinit-function.md) wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokolldateien auf einem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte aufweisen. Normalerweise stellt [JetInit](./jetinit-function.md) die Datenbanken erfolgreich wieder her, schlägt jedoch mit JET_errLogFileSizeMismatchDatabasesConsistent fehl, um anzugeben, dass die Größe der Protokolldatei falsch konfiguriert ist. Wenn dieser Parameter jedoch auf TRUE festgelegt ist, löscht die Datenbank-Engine im Hintergrund alle alten Protokolldateien, startet einen neuen Satz von Transaktionsprotokolldateien mit der konfigurierten Protokolldateigröße und gibt JET_errSuccess zurück.

Dieser Parameter ist nützlich, wenn die Anwendung die Größe der Transaktionsprotokolldatei transparent ändern möchte, in Upgrade- und Wiederherstellungsszenarien aber trotzdem transparent funktioniert.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Wenn dieser Parameter true ist, werden alle Transaktionsprotokolldateien, die auf dem Datenträger gefunden werden und nicht Teil der aktuellen Sequenz von Protokolldateien sind, von [JetInit](./jetinit-function.md)gelöscht. Dies kann verwendet werden, um überflüssige Protokolldateien nach einem Wiederherstellungsvorgang automatisch zu bereinigen.

**Windows XP:**  Eingeführt in Windows XP.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Dieser Parameter konfiguriert die Zeitspanne zwischen einem Aufruf von [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) und [JetOSSnapshotThaw,](./jetossnapshotthaw-function.md) bevor ein Timeout auftritt. Weitere Informationen finden Sie unter [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) und [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) Das Timeout ist in Millisekunden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>20000 (Windows XP und Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Wenn dieser Parameter true ist, wird jede Seite in einer Datenbank, die einer Streamingsicherung unterzogen wird, mit gelöschten Daten bereinigungen. Es ist wichtig zu beachten, dass sich die bereinigungsrelevanten Datenbankseiten auf dem Datenträger befinden. Das vollständige DataSet wird vor dem Bereinigungsprozess gesichert.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
