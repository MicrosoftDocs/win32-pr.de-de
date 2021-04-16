---
description: Weitere Informationen zu Sicherungs-und Wiederherstellungs Parametern
title: Sicherungs-und Wiederherstellungs Parameter
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530116"
---
# <a name="backup-and-restore-parameters"></a>Sicherungs-und Wiederherstellungs Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Sicherungs-und Wiederherstellungs Parameter

Dieses Thema enthält Parameter, die für die Sicherung und Wiederherstellung verwendet werden.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktions Protokollen beibehalten. Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktions Wiedergabe ordnungsgemäß funktioniert. Dieser Parameter kann verwendet werden, um die Wiederherstellung von abstürzen oder einen Wiederherstellungs Vorgang zum Suchen nach den Datenbanken zu erzwingen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Ordner Pfad (Zeichenfolge)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 246 Zeichen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramCleanupMismatchedLogFiles*  
77  

Dieser Parameter steuert das Ergebnis von [jetinit](./jetinit-function.md) , wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte haben. Normalerweise stellt [jetinit](./jetinit-function.md) die Datenbanken erfolgreich wieder her, schlägt jedoch mit JET_errLogFileSizeMismatchDatabasesConsistent fehl, um anzugeben, dass die Größe der Protokolldatei falsch konfiguriert ist. Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien, startet einen neuen Satz von Transaktionsprotokoll Dateien mit der konfigurierten Protokolldatei Größe und gibt JET_errSuccess zurück.

Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOutOfRangeLogs*  
52  

Wenn dieser Parameter true ist, werden alle auf dem Datenträger gefundenen Transaktionsprotokoll Dateien, die nicht Teil der aktuellen Sequenz von Protokolldateien sind, von [jetinit](./jetinit-function.md)gelöscht. Dies kann verwendet werden, um überflüssige Protokolldateien nach einem Wiederherstellungs Vorgang automatisch zu bereinigen.

**Windows XP:**  Eingeführt in Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramOSSnapshotTimeout*  
82  

Dieser Parameter konfiguriert den Zeitraum, der zwischen einem Aufruf von [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) und [jedessnapshotthaw](./jetossnapshotthaw-function.md) zulässig ist, bevor ein Timeout auftritt. Weitere Informationen finden Sie unter [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) und [jedessnapshotthaw](./jetossnapshotthaw-function.md) . Das Timeout ist in Millisekunden angegeben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>20000 (Windows XP und Windows Server 2003);</p>
<p>70000 (Windows Server 2003 SP1)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramZeroDatabaseDuringBackup*  
71  

Wenn dieser Parameter true ist, wird für jede Seite in einer Datenbank, die eine Streamingsicherung durchläuft, die gelöschte Daten bereinigt. Es ist wichtig zu beachten, dass sich die Datenbankseiten, die bereinigt werden, auf der Festplatte befinden. Das vollständige DataSet wird vor dem Bereinigungs Prozess gesichert.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
