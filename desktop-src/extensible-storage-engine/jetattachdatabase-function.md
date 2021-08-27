---
description: Weitere Informationen finden Sie unter JetAttachDatabase-Funktion.
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
ms.openlocfilehash: 368771afb0ab0343e325dc578bb93a319b708b777730499bce74034fef32276c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115760"
---
# <a name="jetattachdatabase-function"></a>JetAttachDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>JetAttachDatabase-Funktion

Die **JetAttachDatabase-Funktion** angefügt eine Datenbankdatei zur Verwendung mit einer Datenbankinstanz. Um die Datenbank verwenden zu können, muss sie anschließend mit [JetOpenDatabase geöffnet werden.](./jetopendatabase-function.md)

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szFilename*

Der Name der zu anfügenden Datenbank.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.

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

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Die Datenbank-Engine kann die Datenbankdatei nicht öffnen. Die Datei wird möglicherweise von einem anderen Prozess verwendet, oder der Aufrufer hat möglicherweise nicht genügend Berechtigungen, um die Datei zu öffnen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>Die in <em>szFilename gegebene Datei</em> ist nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Fehler beim primären Index. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und der primäre Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Bei einem sekundären Index tritt ein Fehler auf. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und ein sekundärer Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mithilfe des folgenden Befehls defragmentiert wird: <strong>esentutl -d</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Pro Instanz kann nur eine begrenzte Anzahl von Datenbanken angefügt werden. Der Grenzwert liegt derzeit bei sieben Datenbanken pro Instanz.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Eine nichtfatale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Das **Aufrufen von JetAttachDatabase** entspricht dem Aufrufen von [JetAttachDatabase2](./jetattachdatabase2-function.md) und dem Übergeben eines Werts von 0 (null), d. h. es gibt keine Beschränkung für den *parameter cpgDatabaseSizeMax.*

Durch anfügen einer beschreibbaren Datenbank (d. h. wenn JET_bitDbReadOnly im *grbit-Parameter* nicht angegeben wurde) wird die Datei ausschließlich auf Betriebssystemebene geöffnet. Die Datei kann von keinem anderen Prozess geöffnet werden. Es ist möglich, dass mehrere Prozesse eine einzelne Datenbank anfügen, indem sie im schreibgeschützten Modus geöffnet werden.

Die Datenbankdatei wird mit [JetDetachDatabase oder](./jetdetachdatabase-function.md) [JetDetachDatabase2 getrennt.](./jetdetachdatabase2-function.md)

Parameter für die Indexüberprüfung

Verschiedene Versionen von Windows Unicode-Text auf unterschiedliche Weise normalisieren. Das bedeutet, dass Indizes, die unter einer Windows erstellt wurden, möglicherweise nicht in anderen Versionen funktionieren.

Vor Windows Server 2003, als die Betriebssystemversion geändert wurde (einschließlich der Installation eines Service Packs), war jeder Index über Unicode-Daten in einem potenziell beschädigten Zustand.

Indizes, die in Windows Server 2003 und höher erstellt wurden, werden mit der Version der Unicode-Normalisierung gekennzeichnet, mit der sie erstellt wurden. Ältere Indizes enthalten keine Versionsinformationen. Die meisten Unicode-Normalisierungsänderungen bestehen aus dem Hinzufügen neuer Zeichen. Codepunkte, die zuvor nicht definiert waren, werden jetzt definiert und normalisieren sich anders. Wenn Binärdaten also in einer Unicode-Spalte gespeichert werden, normalisieren sie sich anders, wenn neue Codepunkte definiert werden.

Seit Windows Server 2003 verfolgt die ESE-Datenbank-Engine Unicode-Indexeinträge nach, die nicht definierte Codepunkte enthalten. Diese können verwendet werden, um einen Index zu korrigieren, wenn sich der Satz definierter Unicode-Zeichen ändert.

Diese Parameter steuern, was geschieht, wenn die ESE-Datenbank-Engine an eine Datenbank angefügt wird, die zuletzt unter einem anderen Build des Betriebssystems verwendet wurde. Die Betriebssystemversion wird im Datenbankheader gestempelt.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **TRUE** festgelegt ist und die Datenbank potenziell beschädigte Indizes enthält:

  - **JetAttachDatabase löscht** die potenziell beschädigten Indizes, *wenn grbit* JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase gibt** einen Fehler zurück, wenn *grbit* keine JET_bitDbDeleteCorruptIndexes enthält und Indizes gelöscht werden müssen.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf FALSE festgelegt **ist:**

  - **JetAttachDatabase** ignoriert potenziell beschädigte Indizes und gibt JET_errSuccess zurück (vorausgesetzt, es sind keine anderen Fehler aufgetreten).

Windows Server 2003 und höher: Wenn [JET_paramEnableIndexChecking](./database-parameters.md) nicht zurückgesetzt wurde, wird die interne Fixuptabelle verwendet, um Indexeinträge zu korrigieren. Dadurch werden möglicherweise nicht alle Indexbeschädigungen behoben, dies ist jedoch für die Anwendung transparent.

Wenn die Datenbank als schreibgeschützt angefügt wurde, kann der Index nicht fixiert oder gelöscht werden. In diesem Fall gibt die API stattdessen einen Fehler zurück, z. B. JET_errSecondaryIndexCorrupted oder JET_errPrimaryIndexCorrupted.

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
<td><p>Implementiert als <strong>JetAddColumnW</strong> (Unicode) und <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
