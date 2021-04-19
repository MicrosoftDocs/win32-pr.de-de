---
description: 'Weitere Informationen zu: jetopenfile-Funktion'
title: JetOpenFile-Funktion
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343222"
---
# <a name="jetopenfile-function"></a>JetOpenFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>JetOpenFile-Funktion

Die **jetopenfile** -Funktion öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung. Die Daten aus diesen Dateien können anschließend mithilfe von [jetreadfile](./jetreadfile-function.md)über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mithilfe von [jetclosefile](./jetclosefile-function.md)geschlossen werden. Eine externe Sicherung der-Instanz muss zuvor mithilfe von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md)initiiert werden.

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parameter

*szFilename*

Der relative oder absolute Pfad zu einer angefügten Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei, die von der-Instanz verwaltet wird und für die Sicherung gelesen wird.

*phffile*

Der Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.

*pulfilesizelow*

Der Ausgabepuffer, der die wenigsten signifikanten 32 Bits der Dateigröße empfängt.

*pulfilesizehigh*

Der Ausgabepuffer, der die signifi32 kantesten Bits der Größe der Datei empfängt.

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
<td><p>Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei aufgrund einer Freigabe Verletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde. Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetopatfile</strong> vorkommen, wenn Folgendes geschieht:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases).</p></li>
<li><p>Der angegebene filename-Parameter ist NULL oder eine Zeichenfolge der Länge 0 (null) (Windows XP und spätere Releases).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da Sie nicht gefunden wurde. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen. <strong>Jetopenfile</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die vorherige Datei, die mit <strong>jetopenfile</strong> geöffnet wurde, von <a href="gg294127(v=exchg.10).md">jetclosefile</a>geschlossen wurde. Zurzeit wird nur ein ausstehendes Datei Handle unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird. JET_errRestoreInProgress der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben. Wenn das Handle für eine Datenbankdatei vorgesehen ist, wird diese Datenbankdatei für die Streamingsicherung vorbereitet. Dies kann dazu führen, dass eine datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei erstellt wird. Die Datenbank-Patchdatei weist genau denselben Pfad und Dateinamen wie die Datenbankdatei auf, verfügt aber über eine. Pat-Erweiterung. Die Größe der Datei wird ebenfalls zurückgegeben.

Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert. Eine Datenbank-Patchdatei wird möglicherweise temporär auf dem Datenträger erstellt, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden. Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird. Unter Windows XP und höheren Versionen wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufens nicht an die Instanz angefügt wurde.

**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **jetopenfile** nicht überprüft, ob der angeforderte Dateipfad mit dem Satz von Dateien verknüpft ist, die für die Instanz gesichert werden sollen. Daher ist es möglich, diese Funktion für den Zugriff auf eine beliebige Datei zu verwenden, die durch den aktuellen Sicherheitskontext des Threads geöffnet werden kann. Es ist zwingend erforderlich, dass die Anwendung die an diese Funktion weiter gegebenen Pfade an einen bekannten Satz von guten Dateipfaden einschränkt oder eine Offenlegung von Informations Angriffen möglich wäre.

#### <a name="remarks"></a>Bemerkungen

Die Ausgabepuffer für die Handle-und Dateigröße müssen vorhanden sein. Wenn Sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepuffer Parameter nicht überprüft werden.

Zurzeit kann jeweils nur eine Datei für die Sicherung geöffnet werden.

**Jetopenfile** bestätigt die Sicherungs Berechtigung nicht vor dem Öffnen der angeforderten Datei.

Die Größe der zu lesenden Datei, wie von dieser Funktion gemeldet, stimmt möglicherweise nicht mit der Größe der Datei auf dem Datenträger ab. Unter Windows XP und höheren Versionen können zusätzliche Informationen an eine Datenbankdatei angehängt werden, die während eines Wiederherstellungs Vorgangs von der Datenbank-Engine verwendet wird. Daher sollte die Anwendung nur die von **jetopenfile** zurückgegebene Dateigröße oder die tatsächliche Anzahl von Daten bytes, die von [jetreadfile](./jetreadfile-function.md)zurückgegeben werden, verlassen.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetopenfilew</strong> (Unicode) und <strong>jetopenfilea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetclosefile](./jetclosefile-function.md)  
[Jetgetattachinfo](./jetgetattachinfo-function.md)  
[Jetgetloginfo](./jetgetloginfo-function.md)  
[Jetreadfile](./jetreadfile-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jettruneurelog](./jettruncatelog-function.md)
