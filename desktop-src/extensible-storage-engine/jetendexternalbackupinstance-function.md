---
description: 'Weitere Informationen zu: jetendexternalbackupinstance-Funktion'
title: Jetendexternalbackupinstance-Funktion
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042654"
---
# <a name="jetendexternalbackupinstance-function"></a>Jetendexternalbackupinstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance-function"></a>Jetendexternalbackupinstance-Funktion

Die **jetendexternalbackupinstance** -Funktion beendet eine externe Sicherungs Sitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.

**Windows XP: jetendexternalbackupinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

**Windows 2000:** Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.

**Windows XP:** Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

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
<td><p>JET_errBackupAbortByCaller</p></td>
<td><p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p>
<p>Der Aufrufer hat eine Sicherung in der Mitte der Sicherungs Sequenz beendet, ohne die Absicht mit <a href="gg294067(v=exchg.10).md">jetstopbackup</a>zu signalisieren. Dieser Fehler ist das Ergebnis eines Fehlers im Sicherungs Client in Windows Server 2003 und höher. Unter Windows XP wird dieser Fehler für eine absichtliche Beendigung der externen Sicherungs Sequenz zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003:  </strong> Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</p>
<p>Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p>
<p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn in der Tat mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn die Funktion erfolgreich ausgeführt wird, war die externe Sicherung erfolgreich. Erfolg gibt an, dass alle Dateien (z. b. Datenbanken und Protokolle), die für den Sicherungstyp (in [jetbeginexternalbackup](./jetbeginexternalbackup-function.md)angegeben) geeignet sind, von der Sicherungs-Engine abgerufen wurden. Die gesicherten Dateien können mit Hard Recovery ([jetexternalrestore](./jetexternalrestore-function.md)) wieder hergestellt werden.

Wenn diese Funktion fehlschlägt, wird die externe Sicherung normalerweise beendet. "Fehler" bedeutet, dass die Sicherung aufgrund eines Fehlers bei der Client-oder Anwendungs Verwendung ungültig ist. Es ist wichtig, den Rückgabecode für diese API zu überprüfen, um zu überprüfen, ob die Sicherungs Sequenz erfolgreich war.

#### <a name="remarks"></a>Bemerkungen

Wenn die Engine zum Protokollieren von Ereignissen konfiguriert ist, wird ein Ereignis protokolliert, um die Auflösung der externen Sicherung anzugeben.

Wenn die Sicherungs Sequenz nicht in der richtigen Reihenfolge und mit einem erfolgreichen Rückruf von [jetendexternalbackup](./jetendexternalbackup-function.md)abgeschlossen ist, können nachfolgende inkrementelle Sicherungen mehr Daten enthalten, als die Anwendung erwartet hat.

Weitere Informationen zur API-Sequenz für die externe Sicherung finden Sie unter [jetbeginexternalbackup](./jetbeginexternalbackup-function.md).

Vor Windows Vista hat die Engine, wenn die Protokoll Verkürzung nicht durchgeführt wurde, die Sicherung als Kopier Sicherung angesehen. Allerdings kann es sich bei der Sicherung um eine normale Sicherung handeln, bei der die abkürzen nicht durchgeführt wurde (z. b. Wenn separate Datenbanken vorhanden sind). Mithilfe der Option JET_bitBackupTruncateDone können Sie die Engine über diese Informationen informieren und ordnungsgemäße Änderungen am Daten Bank Header zulassen.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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

[Fehler Behandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetbeginexternalbackupinstance](./jetbeginexternalbackupinstance-function.md)  
[Jetclosefile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[Jetexternalrestore](./jetexternalrestore-function.md)  
[Jetgetattachinfo](./jetgetattachinfo-function.md)  
[Jetgetloginfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetreadfile](./jetreadfile-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jettruneurelog](./jettruncatelog-function.md)
