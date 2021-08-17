---
description: 'Weitere Informationen zu: JetReadFileInstance-Funktion'
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
ms.openlocfilehash: ec5c83bb78528a61bbe7af9bafa59567100ee9da669915b96230bfb97b8bf390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891116"
---
# <a name="jetreadfileinstance-function"></a>JetReadFileInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>JetReadFileInstance-Funktion

Die **JetReadFileInstance-Funktion** ruft den Inhalt einer Datei ab, die mit der [JetOpenFileInstance-Funktion](./jetopenfileinstance-function.md) geöffnet wurde.

**Windows XP:** **JetReadFileInstance** wurde in Windows XP eingeführt.

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

*Instanz*

Die -Instanz, die für einen bestimmten API-Aufruf verwendet werden soll.

Beachten Sie, dass für Windows 2000 die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar ist, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und höhere Versionen können Sie die API-Variante aufrufen, die diesen Parameter nur dann nicht akzeptiert, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), wenn nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang fehl und gibt den JET_errRunningInMultiInstanceMode Fehler zurück.

*hfFile*

Das Handle der zu lesenden Datei.

*Pv*

Der Ausgabepuffer, der die Dateidaten empfängt.

*Cb*

Die maximale Größe des Ausgabepuffers in Bytes.

*Pcb*

Die tatsächliche Menge der abgerufenen Dateidaten.

### <a name="return-value"></a>Rückgabewert

Diese Funktion erleichtert die Rückgabe aller [JET_ERR](./jet-err.md) Datentypen, die in der ESE-API (Extensible Storage Engine) definiert sind. Weitere Informationen zu JET-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion</a> abgebrochen wurde. Dieser Fehler wird nur von Windows XP und höher Windows Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion</a> ausgeführt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und höher Windows Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt entweder einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für die <strong>JetReadFileInstance-Funktion</strong> auftreten, wenn eine der folgenden Vorgänge auftritt:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig. Windows XP und höher Windows Versionen.</p></li>
<li><p>Die Ausgabepuffergröße ist kein Vielfaches der Datenbankseitengröße (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP und höher Windows Versionen.</p></li>
<li><p>Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten<a href="gg269337(v=exchg.10).md">(JET_paramDatabasePageSize</a>), und dies ist der erste Aufruf der <strong>JetReadFileInstance-Funktion</strong> für das angegebene Handle. Windows XP und höher Windows Versionen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Fehler beim Vorgang, weil beim Lesen einer Transaktionsprotokolldatei eine nicht behebbare Datenbeschädigung erkannt wurde. Dieser Fehler wird nur von Windows XP und höher Windows Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die dieser Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Fehler beim Vorgang, weil beim Lesen einer Datenbankseite aus einer Datenbankdatei oder Einer Datenbankpatchdatei eine nicht behebbare Datenbeschädigung erkannt wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die dieser Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) in einem Fall zu verwenden, in dem nur eine Instanz unterstützt wird, aber bereits mehrere Instanzen vorhanden sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die dieser Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der nächste Datenabschnitt aus der Datei in den Ausgabepuffer eingelesen. Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben. Der Dateioffset, bei dem der nächste Lesefehler auftritt, wird um diesen Betrag erweitert.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die aktuelle Instanz. In Windows XP und höher Windows Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist. Die Sicherung dieser Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.

#### <a name="remarks"></a>Hinweise

Jeder Aufruf der **JetReadFileInstance-Funktion** mit einem Handle, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. B. wenn ein vorheriger Aufruf weniger Bytes als die Größe des Ausgabepuffers zurückgegeben hat), ist immer erfolgreich, gibt jedoch 0 Bytes an Daten zurück.

Sie sollten einen großen Ausgabepuffer verwenden, um die Sicherungsleistung zu maximieren. Möglicherweise müssen Sie experimentieren, um den optimalen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu finden. In jedem Fall sollte der Ausgabepuffer nicht kleiner als 64 KB sein. Der Zeiger, den Sie an **JetReadFileInstance** übergeben, muss an einer Speicherseitengrenze ausgerichtet sein (4 KB oder 8 KB). Rufen Sie hierzu die **VirtualAlloc-Funktion** auf.

Mehrere gleichzeitige Aufrufe von **JetReadFileInstance** mit demselben Dateihandle werden nicht unterstützt. Dies bedeutet, dass es nicht möglich ist, mehrere Puffer für gleichzeitiges Lesen für dieselbe Datei in die Warteschlange zu stellen, um einen hohen sequenziellen Durchsatz zu erzielen. Verwenden Sie stattdessen einen einzelnen großen Puffer.

Wenn Sie eine bestimmte Instanz so konfiguriert haben, dass die Bereinigung von Datenbankseiten aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) Parameter unter [Systemparameter),](./extensible-storage-engine-system-parameters.md)werden gelöschte Daten als Nebeneffekt eines Aufrufs von **JetReadFileInstance** für die Datenbankdatei aus der Datenbank entfernt.

Es ist sehr wichtig zu verstehen, wie Sicherungen und Datenbeschädigungen interagieren. Wenn die Datenbank-Engine während einer Sicherung eine Datenbeschädigung erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl. Dies ist eine bewusste Entwurfsentscheidung zum Schutz vor Datenverlusten. Wenn die Datenbank-Engine zulässt, dass eine Sicherung erfolgreich ausgeführt werden kann, wenn eine Datenbeschädigung vorliegt, kann eine ältere, nicht korrigierte Sicherung als Ergebnis verworfen werden. Dies wäre leider der Fall, da es dann möglich wäre, die Datenbeschädigung auf der Liveinstanz zu beheben, indem diese Sicherung wiederhergestellt und alle Transaktionsprotokolldateien für diese Datenbank wiedergegeben werden. In diesem Szenario ohne Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) unter [Systemparameter](./extensible-storage-engine-system-parameters.md)).

Es ist auch wichtig zu verstehen, dass Fälle von Datenbeschädigung in der Regel zuerst während der Streamingsicherung erkannt werden. Dies liegt daran, dass die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei überprüft. Es ist auch wahrscheinlich, dass die Streamingsicherung der erste Prozess ist, um die frühen Anzeichen von Hardwarefehlern zu erkennen, die sich durch zeitweilige Datenbeschädigungsfehler manifestieren, da sowohl die Menge der durch die Sicherung abgerufenen Daten als auch die Geschwindigkeit, mit der diese Daten abgerufen werden, auftreten.

Datenbeschädigungen werden von der Datenbank-Engine mithilfe von Blockprüfsummen erkannt. Diese Prüfsummen werden unmittelbar vor dem Schreiben einer Datenbankseite festgelegt und auf einer gelesenen Datenbankseite überprüft. Dieses Schema ermöglicht es der Datenbank-Engine, zu bestimmen, dass Daten zu einem bestimmten Zeitpunkt beschädigt wurden, ermöglicht es der Datenbank-Engine jedoch nicht, die Quelle dieser Beschädigung zu ermitteln. In der Vergangenheit stammen Instanzen solcher Datenbeschädigungen aus anderen Quellen als der Datenbank-Engine selbst.

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothek</p></td>
<td><p>Verwendet ESENT.lib.</p></td>
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
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
