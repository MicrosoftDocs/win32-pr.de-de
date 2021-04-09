---
description: 'Weitere Informationen finden Sie hier: Daten Bank Parameter'
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130200"
---
# <a name="database-parameters"></a>Datenbankparameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-parameters"></a>Datenbankparameter

Dieses Thema enthält Parameter, die für die-Datenbank verwendet werden.

*JET_paramCheckFormatWhenOpenFail*  
44  

Wenn dieser Parameter festgelegt wird, gibt [jetinit](./jetinit-function.md) einen besonderen Fehler zurück, wenn eine Datenbank oder ein Transaktionsprotokoll einer früheren Version der Datenbank-Engine geöffnet wird. Folgende Fehler sind aufgetreten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fehler</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden mit der Datenbank-Engine in Windows NT 3,51 erstellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden in einer Testversion vor Windows NT Server 4,0 mit der Datenbank-Engine erstellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>Die Datenbank-und/oder Transaktionsprotokoll Dateien wurden mit der Datenbank-Engine in Windows NT Server 4,0 erstellt.</p></td>
</tr>
</tbody>
</table>


**Windows Vista:**  Für Windows Vista und höher ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
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


*JET_paramDatabasePageSize*  
64  

Dieser Parameter konfiguriert die Seitengröße für die Datenbank. Die Seitengröße ist die kleinste Einheit der Speicherplatz Zuordnung, die für eine Datenbankdatei möglich ist. Die Größe der Datenbankseite ist ebenfalls sehr wichtig, da Sie die Obergrenze für die Größe eines einzelnen Datensatzes in der Datenbank festlegt.

**Hinweis** Zurzeit wird pro Prozess nur eine Datenbankseiten Größe unterstützt. Dies bedeutet, dass Sie, wenn Sie sich in einem einzelnen Prozess befinden, der verschiedene Anwendungen enthält, die die Datenbank-Engine verwenden, alle für eine Datenbankseiten Größe zustimmen müssen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>2048, 4096, 8192</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramDbExtensionSize*  
18  

Mit diesem Parameter wird die Menge des Speicherplatzes gesteuert, der einer Datenbankdatei hinzugefügt wird, wenn Sie vergrößert werden muss, um mehr Daten aufzunehmen. Die Größe befindet sich auf Datenbankseiten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
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
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexChecking*  
45  

Wenn dieser Parameter true ist, wird jede Datenbank bei der [jetattachdatabase](./jetattachdatabase-function.md) -Zeit für Indizes über Unicode-Schlüssel Spalten geprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden. Dies muss erreicht werden, da die Datenbank-Engine die von [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) generierten Sortierschlüssel beibehält und der Wert dieser Sortierschlüssel von Release zu Release geändert wird.

Wenn ein primärer Index in diesem Status erkannt wird, schlägt [jetattachdatabase](./jetattachdatabase-function.md) immer mit JET_errPrimaryIndexCorrupted fehl.

Wenn sekundäre Indizes in diesem Status erkannt werden, gibt es zwei mögliche Ergebnisse. Wenn JET_bitDbDeleteCorruptIndexes an [jetattachdatabase](./jetattachdatabase-function.md) weitergeleitet wurde, werden diese Indizes gelöscht, und JET_wrnCorruptIndexDeleted wird von [jetattachdatabase](./jetattachdatabase-function.md)zurückgegeben. Diese Indizes müssen von Ihrer Anwendung neu erstellt werden. Wenn JET_bitDbDeleteCorruptIndexes nicht an [jetattachdatabase](./jetattachdatabase-function.md) weitergegeben wurde, schlägt der-Rückruf mit JET_errSecondaryIndexCorrupted fehl.

**Hinweis** Es wird dringend empfohlen, dass dieser Parameter von Ihrer Anwendung auf true festgelegt wird.

**Hinweis** Es wird dringend empfohlen, dass Anwendungen die Verwendung von Unicode-Schlüssel Spalten in ihren Primärschlüssel Indizes (gruppierte Indizes) vermeiden.

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
<td><p>Global</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
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
<td><p>Ja</p></td>
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


*JET_paramEnableIndexCleanup*  
54  

Wenn dieser Parameter auf "true" festgelegt ist, kann die Datenbank-Engine ggf. Indizes über Unicode-Schlüssel Spalten automatisch bereinigen [, um Daten](./jetinit-function.md) Bank Formatänderungen zu vermeiden, die durch Änderungen an der NLS-Bibliothek in Windows verursacht werden. Diese Änderungen werden regelmäßig an der NLS-Bibliothek vorgenommen, um Unterstützung für neue Sprachen hinzuzufügen, einer Sprache fehlende Zeichen hinzuzufügen, einer Sprache eine Sortierreihenfolge hinzuzufügen oder Fehler in der Sortierreihenfolge einer Sprache zu beheben. Diese Änderungen wirken sich auf die von [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) erzeugten Sortierschlüssel aus, die von der Datenbank-Engine als Komponenten von Index Schlüsseln persistent gespeichert werden.

Es ist wichtig zu wissen, dass es möglich ist, dass die Änderungen am Index so groß sind, dass eine inkrementelle Bereinigung nicht möglich ist. In diesem Fall wird der Index wie von **JET_paramEnableIndexChecking** vorgeschrieben behandelt.

**Hinweis** Es wird dringend empfohlen, diesen Parameter und **JET_paramEnableIndexChecking** von Ihrer Anwendung auf **true** festzulegen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
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
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
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
<td><p>Windows Server 2003 und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

Wenn dieser Parameter true ist, kann jeweils nur eine Datenbank von einer bestimmten Sitzung aus mit [jetopddatabase](./jetopendatabase-function.md) geöffnet werden. Die temporäre Datenbank wird von dieser Einschränkung ausgeschlossen.

**Windows XP und Windows Server 2003:**  Dieser Parameter ist nur unter Windows XP und Windows Server 2003 schreibgeschützt.

**Windows Vista:**  Dieser Parameter verhält sich normal mit Windows Vista.

**Hinweis**  Dieser Parameter ist schreibgeschützt.

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
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
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


*JET_paramEnableOnlineDefrag*  
35  

Dieser Parameter steuert das Verhalten der Online Defragmentierung, wenn es mithilfe von [jetdefragment](./jetdefragment-function.md)initiiert wird. Weitere Informationen finden Sie unter [jetdefragment](./jetdefragment-function.md) .

Windows 2000: bei Windows 2000 war dieser Parameter ein einfacher boolescher Wert, der eine Online Defragmentierung durchführt, wenn er von [jetdefragment](./jetdefragment-function.md)initiiert wurde. Wenn diese Einstellung auf " **true**" festgelegt ist, wird die Online Defragmentierung für die Datensätze der einzelnen Tabellen in der Datenbank ausgeführt.

**Windows XP:**  Unter Windows XP und höheren Versionen kann dieser Parameter auf eine oder mehrere der folgenden Optionen festgelegt werden:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Option</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>Führen Sie keine Online Defragmentierung durch. Dies ist das binäre Äquivalent zur Windows 2000-Einstellung false für diesen Parameter.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>Führen Sie eine vollständige Online Defragmentierung durch. Dies ist die Binärdatei, die der Einstellung "true" von Windows 2000 für diesen Parameter entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>Führt eine Online Defragmentierung der Datensätze der einzelnen Tabellen in der Datenbank aus.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>Führt eine Online Defragmentierung der Leerräume der einzelnen Tabellen in der Datenbank aus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>Dieser Parameter wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>Führen Sie eine vollständige Online Defragmentierung durch. Dies ist das konzeptionelle Äquivalent zur Windows 2000-Einstellung true für diesen Parameter.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong>  Fall</p>
<p><strong>Windows XP: für Windows XP und höher:</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p><strong>Windows 2000:</strong>  Booleschen</p>
<p><strong>Windows XP und höher:</strong>  JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  False, true</p>
<p><strong>Windows XP und höher:</strong>  0 – JET_OnlineDefragAll</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramPageFragment*  
20  

Dieser Parameter ist der Schwellenwert, den die Datenbank-Engine zum Steuern der Fragmentierung des freien Speicherplatzes verwendet. Die Größe befindet sich auf Datenbankseiten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>8</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramRecordUpgradeDirtyLevel*  
78

Mit diesem Parameter wird gesteuert, wie aggressiv der Cache-Manager für die Datenbankseite eine Datenbankseite schreibt, bei der eine direkte Formatkonvertierung durchgeführt wurde. Diese Formatkonvertierungen erfolgen im laufenden Betrieb, wenn Seiten aus einer Datenbank geladen werden, die mit dem Windows 2000-Datenbankmodul erstellt, aber von einer Windows XP-Version oder einer neueren Version der Datenbank-Engine verwendet wurde.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-3</p></td>
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
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

Die Wartezeit (in Protokollen) hinter dem Tip/Most-Commit-Protokoll, um Datenbankseiten Leerungen abzuschieben. Wenn Sie diese Wartezeit aktivieren, kann die Daten Bank Wiederherstellung bei einem schwerwiegenden Verlust der aktuellen Protokolldatei möglich sein. Siehe JET_bitReplayIgnoreLostLogs.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-1023</p></td>
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
<td><p>Ja</p></td>
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
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

Aktivieren/Deaktivieren Sie die automatische sequenzielle B-Struktur-Defragmentierung.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-1</p></td>
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
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Bestimmt, wie oft die B-Struktur Dichte überprüft wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-maximale Ganzzahl</p></td>
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
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

Maximale Zeit in Millisekunden, die der e/a-einschränstungs Mechanismus eine auszuwertende Aufgabe angibt, damit Sie als "abgeschlossen" angesehen wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-10000</p></td>
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
<td><p>Windows 7</p></td>
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

[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[Jetdebug](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
