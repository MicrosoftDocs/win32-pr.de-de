---
description: 'Weitere Informationen zu: jetkreatedatabase-Funktion'
title: JetCreateDatabase-Funktion
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362271"
---
# <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion

Die **jetkreatedatabase** -Funktion erstellt eine Datenbankdatei und fügt Sie an, die für die ESE-Datenbank-Engine verwendet wird. Das Aufrufen von [JetCreateDatabase2](./jetcreatedatabase2-function.md) mit dem auf NULL festgelegten *cpgdatabasesizemax* ist mit dem Aufrufen von **jetcreatedatabase** identisch, wobei *szconnect* auf NULL festgelegt ist. Zurzeit können bis zu sieben Datenbanken pro Instanz erstellt werden.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*szFilename*

Der Name der zu erstellenden Datenbank.

*szconnect*

Für die zukünftige Verwendung reserviert. Auf NULL festgelegt.

*pdbid*

Ein Zeiger auf einen Puffer, der bei einem erfolgreichen-Aufrufwert den Bezeichner der Datenbank enthält. Bei einem Fehler ist der Wert nicht definiert.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>Wenn <strong>jetkreatedatabase</strong> aufgerufen wird und die Datenbank bereits vorhanden ist, schlägt der API-Aufruf standardmäßig fehl, und die ursprüngliche Datenbank wird nicht überschrieben. JET_bitDbOverwriteExisting ändert dieses Verhalten, und die alte Datenbank wird mit einem neuen überschrieben. Windows XP und höher.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff deaktiviert die Protokollierung. Das Festlegen dieses Bits verliert die Möglichkeit, Protokolldateien wiederzugeben und die Datenbank nach einem katastrophalen Ereignis in einem konsistenten verwendbaren Zustand wiederherzustellen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>Wenn Sie JET_bitDbShadowingOff festlegen, wird die Duplizierung einiger interner Datenbankstrukturen (shadowingup) deaktiviert. Die Duplizierung dieser Strukturen erfolgt aus Gründen der Resilienz, sodass durch das Festlegen von JET_bitDbShadowingOff diese Resilienz entfernt wird.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>Die in <em>szFilename</em> benannte Datenbank ist bereits vorhanden. Wenn dieser Fehler zurückgegeben wird, wird die Datenbank nicht angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Kann zurückgegeben werden, wenn exklusiver Zugriff angefordert wurde, jedoch nicht erteilt werden konnte oder wenn die Datenbank bereits von einer anderen Sitzung bereits geöffnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Wird zurückgegeben, wenn <em>cpgdatabasesizemax</em> größer ist als die maximale Anzahl von Seiten, die in einer Datenbank zulässig sind. Der aktuelle Höchstwert ist 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben. " <em>szFilename</em> " darf nicht NULL sein. Standardmäßig muss " <em>szFilename</em> " auf ein Verzeichnis verweisen, das vorhanden ist. Der Pfad wird erstellt, wenn <em>JET_paramCreatePathIfNotExist</em> festgelegt ist (siehe <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Gibt an, dass eine andere Sitzung die Datenbank bereits exklusiv geöffnet hat (mit JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, eine Datenbank zu erstellen, während eine Transaktion durchgeführt wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Es wurde versucht, mehr als eine Datenbank zu öffnen, und JET_paramOneDatabasePerSession wurde festgelegt. Siehe <a href="gg269337(v=exchg.10).md">Daten Bank Parameter</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden. Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly gibt an, dass die Datei schreibgeschützt angefügt wurde, aber <strong>jetkreatedatabase</strong> nicht JET_bitDbReadOnly bestanden hat. Die Datenbank wird immer noch mit Schreib geschütztem Zugriff geöffnet.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn die in *szFilename* angegebene Datenbank vorhanden ist und JET_bitDbOverwriteExisting nicht übermittelt wurde, tritt beim API-Befehl ein Fehler auf. Wenn JET_bitDbOverwriteExisting übermittelt wurde, wird die alte Datenbankdatei zuerst gelöscht.

Wenn die API eine Datenbankdatei erstellt und dann auf einen anderen Fehler stößt, wird die Datei bereinigt und gelöscht.

**Jetkreatedatabase** öffnet die Datenbank implizit. Es ist nicht zwingend notwendig, anschließend [jetopbank](./jetopendatabase-function.md)zu nennen.

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
<td><p>Implementiert als <strong>jetkreatedatabasew</strong> (Unicode) und <strong>jetkreatedatabasea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[Jetopumdatabase](./jetopendatabase-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
