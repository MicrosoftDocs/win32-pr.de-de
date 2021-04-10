---
description: 'Weitere Informationen zu: jetattachdatabase-Funktion'
title: JetAttachDatabase-Funktion
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214385"
---
# <a name="jetattachdatabase-function"></a>JetAttachDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>JetAttachDatabase-Funktion

Die **jetattachdatabase** -Funktion fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an. Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopend Database](./jetopendatabase-function.md)geöffnet werden.

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*szFilename*

Der Name der anzufügenden Datenbank.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.

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
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Veraltet. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Verhindert Änderungen an der Datenbank.</p></td>
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
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Die Datenbank-Engine kann die Datenbankdatei nicht öffnen. Die Datei wird möglicherweise von einem anderen Prozess verwendet, oder der Aufrufer verfügt möglicherweise nicht über ausreichende Berechtigungen zum Öffnen der Datei.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>Die in <em>szFilename</em> angegebene Datei ist nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Fehler beim primären Index. Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden. Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert wird und der primäre Index eine Spalte mit Unicode-Daten ist. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Es ist ein Fehler mit einem sekundären Index aufgetreten. Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden. Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert und ein sekundärer Index über eine Spalte mit Unicode-Daten verfügt. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mit folgendem Befehl ( <strong>Esentutl-d</strong>) zerlegt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden. Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Der Aufruf von **jetattachdatabase** entspricht dem Aufrufen von [JetAttachDatabase2](./jetattachdatabase2-function.md) und dem übergeben des Werts 0 (null), d. h. es gibt keine Begrenzung für den *cpgdatabasesizemax* -Parameter.

Wenn Sie eine beschreibbare Datenbank anfügen (d. h., wenn JET_bitDbReadOnly nicht im *grbit* -Parameter angegeben wurde), wird die Datei exklusiv auf Betriebssystemebene geöffnet. Ein anderer Prozess kann die Datei nicht öffnen. Es ist möglich, dass mehrere Prozesse eine einzelne Datenbank anfügen, indem Sie Sie im schreibgeschützten Modus öffnen.

Die Datenbankdatei wird mithilfe von [jetdetachdatabase](./jetdetachdatabase-function.md) oder [JetDetachDatabase2](./jetdetachdatabase2-function.md)getrennt.

Parameter für die Index Überprüfung

Verschiedene Versionen von Windows normalisieren Unicode-Text auf unterschiedliche Weise. Dies bedeutet, dass Indizes, die unter einer Windows-Version erstellt wurden, in anderen Versionen möglicherweise nicht funktionieren.

Vor Windows Server 2003, bei Änderung der Betriebssystemversion (einschließlich der Installation eines Service Packs), war jeder Index über Unicode-Daten möglicherweise beschädigt.

Indizes, die in Windows Server 2003 und höher erstellt wurden, werden mit der Version der Unicode-Normalisierung gekennzeichnet, mit der Sie erstellt wurden. Ältere Indizes enthalten keine Versionsinformationen. Die meisten Unicode-normalisierungs Änderungen umfassen das Hinzufügen neuer Zeichen, Code Punkte, die zuvor nicht definiert waren, werden nun definiert und unterschiedlich normalisiert. Wenn Binärdaten in einer Unicode-Spalte gespeichert werden, normalisiert Sie daher anders, wenn neue Code Punkte definiert werden.

Ab Windows Server 2003 verfolgt die ESE-Datenbank-Engine Unicode-Indexeinträge, die nicht definierte Code Punkte enthalten. Diese können verwendet werden, um einen Index zu korrigieren, wenn sich der Satz definierter Unicode-Zeichen ändert.

Diese Parameter steuern, was geschieht, wenn die ESE-Datenbank-Engine an eine Datenbank angefügt wird, die zuletzt unter einem anderen Build des Betriebssystems verwendet wurde. Die Betriebssystemversion wird in den Daten Bank Header gestempelt.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **true** festgelegt ist und die Datenbank potenziell beschädigte Indizes enthält:

  - **Jetattachdatabase** löscht die potenziell beschädigten Indizes, wenn *grbit* JET_bitDbDeleteCorruptIndexes

  - **Jetattachdatabase** gibt einen Fehler zurück, wenn *grbit* keine JET_bitDbDeleteCorruptIndexes enthält und Indizes vorhanden sind, die gelöscht werden müssen.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **false** festgelegt ist:

  - **Jetattachdatabase** ignoriert potenziell beschädigte Indizes und gibt JET_errSuccess zurück (unter der Voraussetzung, dass keine anderen Fehler aufgetreten sind).

Windows Server 2003 und höher: Wenn [JET_paramEnableIndexChecking](./database-parameters.md) nicht zurückgesetzt wurde, wird die interne fixuptabelle verwendet, um Indexeinträge zu fixieren. Dadurch werden möglicherweise nicht alle Index Beschädigungen behoben, Sie sind jedoch für die Anwendung transparent.

Wenn die Datenbank als schreibgeschützt angefügt wurde, kann der Index nicht korrigiert oder gelöscht werden. In diesem Fall gibt die API stattdessen einen Fehler zurück, z. b. JET_errSecondaryIndexCorrupted oder JET_errPrimaryIndexCorrupted.

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
<td><p>Implementiert als <strong>jetaddcolumnw</strong> (Unicode) und <strong>jetaddcolumna</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[Jetkreatedatabase](./jetcreatedatabase-function.md)  
[Jetdetachdatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[Jetopumdatabase](./jetopendatabase-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
