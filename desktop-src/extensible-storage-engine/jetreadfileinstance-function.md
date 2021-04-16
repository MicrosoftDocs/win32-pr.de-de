---
description: 'Weitere Informationen finden Sie unter: jetreadfilinput Stance-Funktion'
title: JetReadFileInstance-Funktion
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524959"
---
# <a name="jetreadfileinstance-function"></a>JetReadFileInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>JetReadFileInstance-Funktion

Die **jetreadfileinstance** -Funktion Ruft den Inhalt einer Datei ab, die mit der [jetopenfileinstance](./jetopenfileinstance-function.md) -Funktion geöffnet wurde.

**Windows XP**:   **jetreadfileinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für einen bestimmten API-Befehl verwendet werden soll.

Beachten Sie, dass die API-Variante für Windows 2000 nicht verfügbar ist, da nur eine Instanz unterstützt wird. In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.

Für Windows XP und spätere Versionen können Sie die API-Variante aufrufen, die diesen Parameter nicht akzeptiert, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in Fällen, in denen nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang fehl, und es wird der JET_errRunningInMultiInstanceMode Fehler zurückgegeben.

*hffile*

Das Handle der zu lesenden Datei.

*teuren*

Der Ausgabepuffer, der die Datei Daten empfängt.

*betrieben*

Die maximale Größe des Ausgabepuffers in Bytes.

*PCB*

Die tatsächliche Menge an Datei Daten, die abgerufen wurden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion vereinfacht die Rückgabe von [JET_ERR](./jet-err.md) Datentypen, die in der ESE-API (Extensible Storage Engine) definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen-Befehl der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion abgebrochen wurde. Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt entweder einen unerwarteten Wert oder einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann für die <strong>jetreadfilinput Stance</strong> -Funktion auftreten, wenn eine der folgenden Aktionen auftritt:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig. Windows XP und neuere Windows-Versionen.</p></li>
<li><p>Bei der Ausgabepuffergröße handelt es sich nicht um ein Vielfaches der Seitengröße der Datenbank (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP und neuere Windows-Versionen.</p></li>
<li><p>Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Dies ist der erste Rückruf der <strong>jetreadfileinstance</strong> -Funktion für das angegebene Handle. Windows XP und neuere Windows-Versionen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil nicht BEHEB bare Daten beim Lesen einer Transaktionsprotokoll Datei erkannt wurden. Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die dieser Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht BEHEB bare Daten beim Lesen einer Datenbankseite aus einer Datenbankdatei oder einer Datenbank-Patchdatei erkannt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die dieser Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in einem Fall, in dem nur eine Instanz unterstützt wird, aber mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die dieser Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der nächste Datenblock aus der Datei in den Ausgabepuffer eingelesen. Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben. Der Dateioffset, bei dem der nächste Lesevorgang stattfindet, wird um diesen Betrag erweitert.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die aktuelle Instanz abgebrochen wird. In Windows XP und neueren Windows-Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist. Die Sicherung der Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.

#### <a name="remarks"></a>Bemerkungen

Jeder Aufrufe der **jetreadfileinstance** -Funktion, die mithilfe eines Handles vorgenommen wurde, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. b., wenn ein vorheriger-Rückruf weniger Bytes zurückgegeben hat als die Größe des Ausgabepuffers), wird immer erfolgreich ausgeführt, gibt aber NULL Bytes an Daten zurück.

Sie sollten einen großen Ausgabepuffer verwenden, um die Sicherungsleistung zu maximieren. Möglicherweise müssen Sie experimentieren, um den optimalen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu ermitteln. In jedem Fall sollte der Ausgabepuffer nicht kleiner als 64 KB sein. Der Zeiger, den Sie an **jetreadfilinput Stance** übergeben, muss an einer Seitenbegrenzung für den Arbeitsspeicher (4 KB oder 8 KB) ausgerichtet sein. Dies können Sie erreichen, indem Sie die **virtualzuweisung** -Funktion aufrufen.

Mehrere gleichzeitige Aufrufe von **jetreadfileinstance** , die mithilfe desselben Datei Handles durchgeführt werden, werden nicht unterstützt. Dies bedeutet, dass es nicht möglich ist, mehrere Puffer in die Warteschlange zu stellen, um gleichzeitige Lesevorgänge für dieselbe Datei durchzuführen Verwenden Sie stattdessen einen einzelnen großen Puffer.

Wenn Sie eine bestimmte Instanz so konfiguriert haben, dass die Datenbankseiten Bereinigung aktiviert ist (siehe den [JET_paramCircularLog](./transaction-log-parameters.md) Parameter in [System Parametern](./extensible-storage-engine-system-parameters.md)), werden gelöschte Daten aus der Datenbank als Nebeneffekt eines Aufrufes **jetreadfileinstance** für die Datenbankdatei entfernt.

Es ist sehr wichtig zu verstehen, wie Sicherungen und Daten Beschädigungen interagieren. Wenn die Datenbank-Engine während einer Sicherung Daten Beschädigungen erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl. Dies ist eine bewusste Entwurfs Entscheidung, die vor Datenverlusten geschützt werden soll. Wenn die Datenbank-Engine die erfolgreiche Ausführung einer Sicherung bei einer Daten Beschädigung gestattet hat, kann es vorkommen, dass eine ältere, nicht beschädigte Sicherung als Ergebnis verworfen wird. Dies wäre leider nicht möglich, da es dann möglich wäre, die Daten Beschädigung auf der Live Instanz zu beheben, indem diese Sicherung wieder hergestellt und alle Transaktionsprotokoll Dateien für diese Datenbank wiedergegeben werden. Bei diesem Szenario mit Null Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md)).

Es ist auch wichtig zu verstehen, dass die Fälle von Daten Beschädigungen bei der Streamingsicherung zuerst erkannt werden. Dies liegt daran, dass die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei scannt. Außerdem ist es wahrscheinlich, dass die Streamingsicherung der erste Prozess zum Erkennen der frühen Anzeichen eines Hardwarefehlers ist, wie es bei zeitweiligen Daten Beschädigungen der Fall ist, weil die von der Sicherung abgerufenen Datenmenge und die Geschwindigkeit, mit der die Daten abgerufen werden, auftreten.

Daten Beschädigungen werden von der Datenbank-Engine durch die Verwendung von Block Prüfsummen erkannt. Diese Prüfsummen werden direkt vor dem Schreiben einer Datenbankseite festgelegt und auf dem Lesevorgang einer Datenbankseite überprüft. Mit diesem Schema kann die Datenbank-Engine ermitteln, dass die Daten zu einem bestimmten Zeitpunkt beschädigt wurden, aber die Datenbank-Engine kann die Quelle dieser Beschädigung nicht ermitteln. In der Vergangenheit stammen Instanzen solcher Daten Beschädigungen aus anderen Quellen als der Datenbank-Engine selbst.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td><p>Wird in "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothek</p></td>
<td><p>Verwendet ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetopeinfileinstance](./jetopenfileinstance-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
