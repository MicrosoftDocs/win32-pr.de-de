---
description: Weitere Informationen finden Sie in der jettruneureloginstance-Funktion
title: Jettruneureloginstance-Funktion
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354516"
---
# <a name="jettruncateloginstance-function"></a>Jettruneureloginstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jettruncateloginstance-function"></a>Jettruneureloginstance-Funktion

Die **jettruneureloginstance** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um Transaktionsprotokoll Dateien zu löschen, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde.

**Windows XP:**  **jettruneureloginstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

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
<td><p><strong>Windows Server 2003:</strong>  Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</p>
<p>Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde. <a href="gg269263(v=exchg.10).md">Jettruneurelog</a> gibt diesen Fehler zurück, wenn ausstehende Datei Handles vorhanden sind, die mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben. Dies kann bei <a href="gg269263(v=exchg.10).md">jettruneurelog</a> vorkommen, wenn das angegebene Instanzhandle ungültig ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die Transaktionsprotokoll Dateien, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde, gelöscht. Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.

Wenn diese Funktion fehlschlägt, kann der Sicherungs Zustands Automat so erweitert werden, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Möglicherweise wird eine bestimmte Anzahl von Transaktionsprotokoll Dateien gelöscht, die kleiner als die gewünschte Anzahl ist, aber Sie werden immer vom ältesten zum jüngsten gelöscht.

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

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jetstopservice](./jetstopservice-function.md)
