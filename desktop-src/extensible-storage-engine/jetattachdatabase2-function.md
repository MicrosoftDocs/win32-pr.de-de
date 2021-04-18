---
description: 'Weitere Informationen finden Sie hier: JetAttachDatabase2-Funktion'
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
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351533"
---
# <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion

Die **JetAttachDatabase2** -Funktion fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an und gibt eine maximale Größe für diese Datenbank an. Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopend Database](./jetopendatabase-function.md)geöffnet werden.

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.

*szFilename*

Der Name der anzufügenden Datenbank.

*cpgdatabasesizemax*

Die maximale Größe (in Datenbankseiten) für die Datenbank. Die standardmäßige Datenbankseiten Größe beträgt 4 Kilobytes, die mithilfe der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion geändert werden können, bevor eine Datenbank erstellt wird.

Das übergeben von NULL bedeutet, dass kein Maximum von der Datenbank-Engine erzwungen wird.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:

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
<td><p>Alle Indizes für Unicode-Daten werden unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>gelöscht. Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p></td>
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

Die-Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück. Im folgenden finden Sie die am häufigsten zurückgegebenen. (Eine komplette Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)

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
<td><p>Die von <em>szFilename</em> angegebene Datenbankdatei muss beschreibbar sein. Das Read-Only-Attribut darf nicht festgelegt werden, und der laufende Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Die Datenbankdatei wurde bereits von einem anderen Prozess geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben. " <em>szFilename</em> " darf nicht NULL sein und verweist auf einen gültigen Pfad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Die in <em>szFilename</em> angegebene Datei ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Fehler beim primären Index. Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden. Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert wird und der primäre Index eine Spalte mit Unicode-Daten ist. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Es ist ein Fehler mit einem sekundären Index aufgetreten. Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden. Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert und ein sekundärer Index über eine Spalte mit Unicode-Daten verfügt. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mit folgendem Befehl ( <strong>Esentutl-d</strong>) zerlegt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden. Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Die Datenbankdatei wird mithilfe von [jetdetachdatabase](./jetdetachdatabase-function.md) oder [JetDetachDatabase2](./jetdetachdatabase2-function.md)getrennt.

Weitere Hinweise finden Sie unter [jetattachdatabase](./jetattachdatabase-function.md) .

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
<td><p>Implementiert als <strong>JetAttachDatabase2W</strong> (Unicode) und <strong>JetAttachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetkreatedatabase](./jetcreatedatabase-function.md)  
[Jetopumdatabase](./jetopendatabase-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
