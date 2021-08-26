---
description: Weitere Informationen finden Sie unter JetAttachDatabase2-Funktion.
title: JetAttachDatabase2-Funktion
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99735582ea794288099428b0d737059dc5792d23749aa70f209d3cf7edf845ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016310"
---
# <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion

Die **JetAttachDatabase2-Funktion** angefügt eine Datenbankdatei zur Verwendung mit einer Datenbankinstanz und gibt eine maximale Größe für diese Datenbank an. Um die Datenbank verwenden zu können, muss sie anschließend mit [JetOpenDatabase geöffnet werden.](./jetopendatabase-function.md)

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*szFilename*

Der Name der zu anfügenden Datenbank.

*cpgDatabaseSizeMax*

Die maximale Größe auf Datenbankseiten für die Datenbank. Die Standardgröße der Datenbankseite beträgt 4 KB, die vor dem Erstellen einer Datenbank mithilfe der [JetSetSystemParameter-Funktion](./jetsetsystemparameter-function.md) geändert werden kann.

Wenn 0 (null) übergeben wird, bedeutet dies, dass von der Datenbank-Engine kein Maximum erzwungen wird.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Wenn <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht. Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Alle Indizes für Unicode-Daten werden gelöscht, unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking.</a> Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Verhindert Änderungen an der Datenbank.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen der [JET_ERR](./jet-err.md) zurück. Die folgenden werden am häufigsten zurückgegeben. (Eine vollständige Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Das Anfügen einer Datenbank ist während einer Sicherung nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Die durch <em>szFilename</em> angegebene Datenbankdatei muss beschreibbar sein. Das Read-Only-Attribut darf nicht festgelegt werden, und der ausgeführte Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Die Datenbankdatei wurde bereits von einem anderen Prozess geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>In szFilename wurde ein <em>ungültiger Pfad angegeben.</em> <em>szFilename muss</em> nicht NULL sein und auf einen gültigen Pfad verweisen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Die Datenbankdatei wurde bereits von einer anderen Sitzung angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Die in <em>szFilename gegebene Datei</em> ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Fehler beim primären Index. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und der primäre Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Bei einem sekundären Index tritt ein Fehler auf. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und ein sekundärer Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mithilfe des folgenden Befehls defragmentiert wird: <strong>esentutl -d</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine begrenzte Anzahl von Datenbanken angefügt werden. Der Grenzwert liegt derzeit bei sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nichtfatale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Die Datenbankdatei wird mit [JetDetachDatabase oder](./jetdetachdatabase-function.md) [JetDetachDatabase2 getrennt.](./jetdetachdatabase2-function.md)

Hinweise finden Sie unter [JetAttachDatabase.](./jetattachdatabase-function.md)

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
<td><p>Wird in Esent.h deklariert.</p></td>
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
<td><p>Implementiert als <strong>JetAttachDatabase2W</strong> (Unicode) und <strong>JetAttachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
