---
description: 'Weitere Informationen zu: JetCreateDatabase-Funktion'
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
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358299"
---
# <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion

Die **JetCreateDatabase-Funktion** erstellt und fügt eine Datenbankdatei an, die mit der ESE-Datenbank-Engine verwendet werden soll. Das Aufrufen von [JetCreateDatabase2](./jetcreatedatabase2-function.md) mit *cpgDatabaseSizeMax* auf 0 (null) ist identisch mit dem Aufrufen von **JetCreateDatabase,** wobei *szConnect* auf NULL festgelegt ist. Derzeit können bis zu sieben Datenbanken pro Instanz erstellt werden.

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

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szFilename*

Der Name der zu erstellenden Datenbank.

*szConnect*

Für die zukünftige Verwendung reserviert. Auf NULL festgelegt.

*pdbid*

Zeiger auf einen Puffer, der bei einem erfolgreichen Aufruf den Bezeichner der Datenbank enthält. Bei einem Fehler ist der Wert nicht definiert.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.

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
<td><p>Wenn <strong>JetCreateDatabase</strong> aufgerufen wird und die Datenbank bereits vorhanden ist, schlägt der API-Aufruf standardmäßig fehl, und die ursprüngliche Datenbank wird nicht überschrieben. JET_bitDbOverwriteExisting ändert dieses Verhalten, und die alte Datenbank wird mit einer neuen datenbank überschrieben. Windows XP und höher.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff deaktiviert die Protokollierung. Das Festlegen dieses Bits verliert die Fähigkeit, Protokolldateien wiederzugeben und die Datenbank nach einem schwerwiegenden Ereignis in einen konsistenten verwendbaren Zustand wiederherzustellen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>Durch festlegen JET_bitDbShadowingOff wird die Duplizierung einiger interner Datenbankstrukturen (Schatten) deaktiviert. Die Duplizierung dieser Strukturen erfolgt aus Gründen der Resilienz, sodass durch festlegen JET_bitDbShadowingOff diese Resilienz entfernt wird.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Die Datenbank mit dem Namen <em>szFilename</em> ist bereits vorhanden. Wenn dieser Fehler zurückgegeben wird, wird die Datenbank nicht angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Kann zurückgegeben werden, wenn exklusiver Zugriff angefordert wurde, aber nicht gewährt werden konnte, oder wenn eine andere Sitzung die Datenbank bereits exklusiv geöffnet hat.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Wird zurückgegeben, wenn <em>cpgDatabaseSizeMax</em> größer als die maximal zulässige Anzahl von Seiten in einer Datenbank ist. Der aktuelle Höchstwert ist 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>In <em>szFilename</em>wurde ein ungültiger Pfad angegeben. <em>szFilename</em> muss ungleich NULL sein. Standardmäßig muss <em>szFilename</em> auf ein verzeichnis verweisen, das vorhanden ist. Der Pfad wird erstellt, wenn <em>JET_paramCreatePathIfNotExist</em> festgelegt ist (siehe <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Gibt an, dass die Datenbank bereits in einer anderen Sitzung exklusiv geöffnet wurde (mit JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Die Datenbankdatei wurde bereits von einer anderen Sitzung angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, eine Datenbank während einer Transaktion zu erstellen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Es wurde versucht, mehrere Datenbanken zu öffnen, und JET_paramOneDatabasePerSession wurde festgelegt. Weitere Informationen finden Sie unter <a href="gg269337(v=exchg.10).md">Datenbankparameter.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, weil kein Arbeitsspeicher zugeordnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine begrenzte Anzahl von Datenbanken angefügt werden. Der Grenzwert beträgt derzeit sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nichttale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly gibt an, dass die Datei schreibgeschützt angefügt wurde, <strong>JetCreateDatabase</strong> jedoch nicht JET_bitDbReadOnly übergeben hat. Die Datenbank wird weiterhin mit schreibgeschütztem Zugriff geöffnet.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Wenn die in *szFilename* angegebene Datenbank vorhanden ist und JET_bitDbOverwriteExisting nicht übergeben wurde, schlägt der API-Aufruf fehl. Wenn JET_bitDbOverwriteExisting übergeben wurde, wird die alte Datenbankdatei zuerst gelöscht.

Wenn die API eine Datenbankdatei erstellt und dann auf einen anderen Fehler trifft, wird die Datei bereinigt und gelöscht.

**JetCreateDatabase** öffnet die Datenbank implizit. Es ist nicht notwendigerweise erforderlich, [jetOpenDatabase](./jetopendatabase-function.md)anschließend aufzurufen.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetCreateDatabaseW</strong> (Unicode) und <strong>JetCreateDatabaseA</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
