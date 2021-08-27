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
ms.openlocfilehash: 2b07312cbfce36b450fe39a39810813adc2d0fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987703"
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


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Wenn <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht. Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Alle Indizes über Unicode-Daten werden gelöscht, unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking.</a> Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Veraltet. Darf nicht verwendet werden.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Verhindert Änderungen an der Datenbank.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Das Anfügen einer Datenbank ist während einer Sicherung nicht zulässig.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Die durch <em>szFilename</em> angegebene Datenbankdatei muss beschreibbar sein. Das Read-Only-Attribut darf nicht festgelegt werden, und der ausgeführte Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Die Datenbankdatei wurde bereits von einem anderen Prozess geöffnet.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>In szFilename wurde ein <em>ungültiger Pfad angegeben.</em> <em>szFilename muss</em> nicht NULL sein und auf einen gültigen Pfad verweisen.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Die Datenbankdatei wurde bereits von einer anderen Sitzung angefügt.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>Die Datenbank-Engine kann die Datenbankdatei nicht öffnen. Die Datei wird möglicherweise von einem anderen Prozess verwendet, oder der Aufrufer hat möglicherweise nicht genügend Berechtigungen, um die Datei zu öffnen.</p> | 
| <p>JET_errFileNotFound</p> | <p>Die in <em>szFilename gegebene Datei</em> ist nicht vorhanden.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Fehler beim primären Index. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und der primäre Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Bei einem sekundären Index tritt ein Fehler auf. Dies kann auf eine physische Beschädigung (z. B. Datenträger- oder Speicherbeschädigung) führen. Sie kann auch zurückgegeben werden, wenn eine Datenbank angefügt wird, die zuletzt unter einem älteren Betriebssystem geändert wurde, und ein sekundärer Index sich über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Anmerkungen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mithilfe des folgenden Befehls defragmentiert wird: <strong>esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Pro Instanz kann nur eine begrenzte Anzahl von Datenbanken angefügt werden. Der Grenzwert liegt derzeit bei sieben Datenbanken pro Instanz.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Eine nichtfatale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p> | 



#### <a name="remarks"></a>Bemerkungen

Das **Aufrufen von JetAttachDatabase** entspricht dem Aufrufen von [JetAttachDatabase2](./jetattachdatabase2-function.md) und dem Übergeben eines Werts von 0 (null), d. h. es gibt keine Beschränkung für den *parameter cpgDatabaseSizeMax.*

Durch anfügen einer beschreibbaren Datenbank (d. h., wenn JET_bitDbReadOnly im *grbit-Parameter* nicht angegeben wurde) wird die Datei ausschließlich auf Betriebssystemebene geöffnet. Die Datei kann von keinem anderen Prozess geöffnet werden. Es ist möglich, dass mehrere Prozesse eine einzelne Datenbank anfügen, indem sie im schreibgeschützten Modus geöffnet werden.

Die Datenbankdatei wird mit [JetDetachDatabase oder](./jetdetachdatabase-function.md) [JetDetachDatabase2 getrennt.](./jetdetachdatabase2-function.md)

Parameter für die Indexüberprüfung

Verschiedene Versionen von Windows Unicode-Text auf unterschiedliche Weise normalisieren. Das bedeutet, dass Indizes, die unter einer Windows erstellt wurden, möglicherweise nicht in anderen Versionen funktionieren.

Vor Windows Server 2003, als die Betriebssystemversion geändert wurde (einschließlich der Installation eines Service Packs), war jeder Index über Unicode-Daten in einem potenziell beschädigten Zustand.

Indizes, die in Windows Server 2003 und höher erstellt wurden, werden mit der Unicode-Normalisierungsversion gekennzeichnet, mit der sie erstellt wurden. Ältere Indizes enthalten keine Versionsinformationen. Die meisten Unicode-Normalisierungsänderungen bestehen aus dem Hinzufügen neuer Zeichen. Codepunkte, die zuvor nicht definiert waren, werden jetzt definiert und normalisieren sich anders. Wenn Binärdaten also in einer Unicode-Spalte gespeichert werden, normalisieren sie sich anders, wenn neue Codepunkte definiert werden.

Ab Windows Server 2003 verfolgt die ESE-Datenbank-Engine Unicode-Indexeinträge nach, die nicht definierte Codepunkte enthalten. Diese können verwendet werden, um einen Index zu korrigieren, wenn sich der Satz definierter Unicode-Zeichen ändert.

Diese Parameter steuern, was geschieht, wenn die ESE-Datenbank-Engine an eine Datenbank angefügt wird, die zuletzt unter einem anderen Build des Betriebssystems verwendet wurde. Die Betriebssystemversion wird im Datenbankheader gestempelt.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **TRUE** festgelegt ist und die Datenbank potenziell beschädigte Indizes enthält:

  - **JetAttachDatabase löscht** die potenziell beschädigten Indizes, wenn *grbit* JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase gibt** einen Fehler zurück, wenn *grbit* JET_bitDbDeleteCorruptIndexes enthält und Indizes gelöscht werden müssen.

Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf FALSE festgelegt **ist:**

  - **JetAttachDatabase** ignoriert potenziell beschädigte Indizes und gibt JET_errSuccess zurück (vorausgesetzt, es sind keine anderen Fehler aufgetreten).

Windows Server 2003 und höher: [Wenn](./database-parameters.md) JET_paramEnableIndexChecking nicht zurückgesetzt wurde, wird die interne Fixuptabelle verwendet, um Indexeinträge zu korrigieren. Dadurch werden möglicherweise nicht alle Indexbeschädigungen behoben, dies ist jedoch für die Anwendung transparent.

Wenn die Datenbank als schreibgeschützt angefügt wurde, kann der Index nicht fixiert oder gelöscht werden. In diesem Fall gibt die API stattdessen einen Fehler zurück, z. B. JET_errSecondaryIndexCorrupted oder JET_errPrimaryIndexCorrupted.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetAddColumnW</strong> (Unicode) und <strong>JetAddColumnA</strong> (ANSI) implementiert.</p> | 



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
