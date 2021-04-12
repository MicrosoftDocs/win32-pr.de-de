---
description: 'Weitere Informationen finden Sie unter: jetreadfile-Funktion'
title: Jetreadfile-Funktion
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217051"
---
# <a name="jetreadfile-function"></a>Jetreadfile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>Jetreadfile-Funktion

Die **jetreadfile** -Funktion Ruft den Inhalt einer Datei ab, die mit [jetopenfile](./jetopenfile-function.md)geöffnet wurde.

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*hffile*

Das Handle der zu lesenden Datei.

*teuren*

Ausgabepuffer, von dem die Datei Daten empfangen werden.

*betrieben*

Die maximale Größe des Ausgabepuffers in Bytes.

*pcbactual*

Empfängt die tatsächliche Menge an Datei Daten, die abgerufen wurden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Der Vorgang konnte nicht ausgeführt werden, da die aktuelle externe Sicherung durch einen <a href="gg269240(v=exchg.10).md">jetstopservice</a>-Befehl abgebrochen wurde. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetreadfile</strong> vorkommen, wenn Folgendes geschieht:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig. Windows XP und spätere Versionen.</p></li>
<li><p>Bei der Ausgabepuffergröße handelt es sich nicht um ein Vielfaches der Seitengröße der Datenbank (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP und spätere Versionen.</p></li>
<li><p>Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Dies ist der erste <strong>jetreadfile</strong> -Rückruf für das angegebene Handle. Windows XP und spätere Versionen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil beim Lesen einer Datenbankseite aus einer Datenbankdatei oder einer Datenbank-Patchdatei eine nicht wiederherstellbare Daten Beschädigung festgestellt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil beim Lesen einer Transaktionsprotokoll Datei eine nicht wiederherstellbare Daten Beschädigung festgestellt wurde. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der nächste Datenblock aus der Datei in den Ausgabepuffer eingelesen. Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben. Der Dateioffset, bei dem der nächste Lesevorgang stattfindet, wird um diesen Betrag erweitert.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird. Unter Windows XP und höheren Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist. Die Sicherung der Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.

#### <a name="remarks"></a>Bemerkungen

Jeder **jetreadfile** -Befehl, der ein Handle verwendet, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. b. ein vorheriger-Rückruf, der weniger Bytes zurückgegeben hat als die Größe des Ausgabepuffers), ist immer erfolgreich, aber gibt NULL Bytes an Daten zurück.

Ein großer Ausgabepuffer sollte verwendet werden, um die Sicherungsleistung zu maximieren. Einige Experimente sind möglicherweise erforderlich, um den richtigen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu ermitteln. Der Ausgabepuffer sollte in jedem Fall nicht kleiner als 64 KB sein.

Mehrere gleichzeitige Aufrufe von **jetreadfile** mit demselben Datei Handle werden nicht unterstützt. Dies bedeutet, dass es nicht möglich ist, mehrere Puffer für einen gleichzeitigen Lesevorgang in eine Warteschlange zu stellen, um einen hohen sequenziellen Durchsatz zu erzielen. Stattdessen sollte ein einzelner großer Puffer verwendet werden.

Wenn die-Instanz so konfiguriert ist, dass das Bereinigen der Datenbankseite aktiviert ist (siehe JET_paramZeroDatabaseDuringBackup in System Parametern), werden gelöschte Daten aus der Datenbank als Nebeneffekt eines **jetreadfile** -Aufrufes in der Datenbankdatei entfernt.

Es ist sehr wichtig zu verstehen, wie Sicherungen und Daten Beschädigungen interagieren. Wenn die Datenbank-Engine Daten Beschädigungen während einer Sicherung erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl. Dies ist eine bewusste Entwurfs Entscheidung, die vor Datenverlusten geschützt werden soll. Wenn die Datenbank-Engine die erfolgreiche Ausführung einer Sicherung bei einer Daten Beschädigung gestattet hat, kann es vorkommen, dass eine ältere, nicht beschädigte Sicherung als Ergebnis verworfen wird. Dies wäre leider nicht möglich, da es möglich wäre, die Daten Beschädigung auf der Live Instanz zu beheben, indem diese Sicherung wieder hergestellt und alle Transaktionsprotokoll Dateien für diese Datenbank wiedergegeben werden. Bei diesem Szenario mit Null Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md)).

Es ist auch wichtig zu wissen, dass die streamingingsicherung am wahrscheinlichsten ist, wenn Daten beschädigt werden. Dies ist der Fall, da die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei scannt. Außerdem ist es wahrscheinlich, dass die Streamingsicherung der erste Prozess zum Erkennen der frühen Anzeichen eines Hardwarefehlers ist, wie es bei zeitweiligen Daten Beschädigungen der Fall ist. Der Grund hierfür ist die Menge der von der Sicherung abgerufenen Daten sowie die Geschwindigkeit, mit der Sie abgerufen wird.

Daten Beschädigungen werden von der Datenbank-Engine durch die Verwendung von Block Prüfsummen erkannt. Diese Prüfsummen werden direkt vor dem Schreiben einer Datenbankseite festgelegt und auf dem Lesevorgang einer Datenbankseite überprüft. Mit diesem Schema kann die Datenbank-Engine feststellen, dass die Daten zu einem bestimmten Zeitpunkt beschädigt wurden, aber die Datenbank-Engine kann die Quelle dieser Beschädigung nicht ermitteln. In der Vergangenheit wurde die vorherrschende Ursache für derartige Beschädigungen aus anderen Quellen als der Datenbank-Engine selbst herausgefunden.

#### <a name="requirements"></a>Anforderungen

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
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
