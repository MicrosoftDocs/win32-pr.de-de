---
description: Weitere Informationen finden Sie unter Sicherungs- und Wiederherstellungsparameter.
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
ms.openlocfilehash: e57cc3f1078d46436d56a56c48c31a3fac4956c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481406"
---
# <a name="backup-and-restore-parameters"></a>Sicherungs- und Wiederherstellungsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Sicherungs- und Wiederherstellungsparameter

Dieses Thema enthält Parameter, die für die Sicherung und Wiederherstellung verwendet werden.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktionsprotokollen beibehalten. Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktionswiedergabe ordnungsgemäß funktioniert. Dieser Parameter kann verwendet werden, um eine Absturzwiederherstellung oder einen Wiederherstellungsvorgang zu erzwingen, um nach den Datenbanken zu suchen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.


| | | <p>Standardwert:</p> | <p>""</p> | | <p>Typ:</p> | <p>Ordnerpfad (Zeichenfolge)</p> | | <p>Gültiger Bereich:</p> | <p>0 – 246 Zeichen</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Dieser Parameter steuert das Ergebnis von [JetInit,](./jetinit-function.md) wenn die Datenbank-Engine so konfiguriert ist, dass transaktionsprotokolldateien auf dem Datenträger verwendet werden, die eine andere Größe als die konfigurierte haben. Normalerweise stellt [JetInit die](./jetinit-function.md) Datenbanken erfolgreich wieder auf, aber es wird ein Fehler JET_errLogFileSizeMismatchDatabasesConsistent, um anzugeben, dass die Größe der Protokolldatei falsch konfiguriert ist. Wenn dieser Parameter jedoch auf TRUE festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien, startet einen neuen Satz von Transaktionsprotokolldateien mit der konfigurierten Protokolldateigröße und gibt JET_errSuccess.

Dieser Parameter ist nützlich, wenn die Anwendung die Größe der Transaktionsprotokolldatei transparent ändern möchte, aber in Upgrade- und Wiederherstellungsszenarien weiterhin transparent funktioniert.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Wenn dieser Parameter true ist, werden alle Transaktionsprotokolldateien auf dem Datenträger, die nicht Teil der aktuellen Sequenz von Protokolldateien sind, von [JetInit gelöscht.](./jetinit-function.md) Dies kann verwendet werden, um nach einem Wiederherstellungsvorgang automatisch nicht verwendete Protokolldateien zu bereinigen.

**Windows XP:**  Eingeführt in Windows XP.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Dieser Parameter konfiguriert die Zulässige Zeit zwischen einem Aufruf von [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) und [JetOSSnapshotThaw,](./jetossnapshotthaw-function.md) bevor ein Timeout auftritt. Weitere Informationen finden Sie unter [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) und [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) Das Timeout liegt in Millisekunden.


| | | <p>Standardwert:</p> | <p>20000 (Windows XP und Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Wenn dieser Parameter true ist, wird jede Seite in einer Datenbank, die einer Streamingsicherung unterzogen wird, mit gelöschten Daten wiederherstellen. Es ist wichtig zu beachten, dass sich die zu bereinigungsbereinigungen Datenbankseiten auf dem Datenträger befinden. Das vollständige DataSet wird vor dem Bereinigungsprozess sichern.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
