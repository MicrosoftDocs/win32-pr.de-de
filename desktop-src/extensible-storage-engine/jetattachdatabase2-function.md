---
description: 'Weitere Informationen zu: JetAttachDatabase2-Funktion'
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
ms.openlocfilehash: 02f896d41c5804fd85a3cb5f31b6c509c3099357
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983523"
---
# <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>JetAttachDatabase2-Funktion

Die **JetAttachDatabase2-Funktion** fügt eine Datenbankdatei für die Verwendung mit einer Datenbankinstanz an und gibt eine maximale Größe für diese Datenbank an. Um die Datenbank verwenden zu können, muss sie anschließend mit [JetOpenDatabase](./jetopendatabase-function.md)geöffnet werden.

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

Der Name der anzufügende Datenbank.

*cpgDatabaseSizeMax*

Die maximale Größe für die Datenbank auf Datenbankseiten. Die Standardgröße der Datenbankseite beträgt 4 Kilobyte, die vor dem Erstellen einer Datenbank mithilfe der [JetSetSystemParameter-Funktion](./jetsetsystemparameter-function.md) geändert werden kann.

Das Übergeben von 0 (null) bedeutet, dass von der Datenbank-Engine kein Maximum erzwungen wird.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Wenn <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht. Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Alle Indizes für Unicode-Daten werden gelöscht, unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">von JET_paramEnableIndexChecking</a>. Weitere Details finden Sie im Abschnitt „Anmerkungen“.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Verhindert Änderungen an der Datenbank.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Für die zukünftige Verwendung reserviert.</p> | 



### <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück. Die folgenden werden am häufigsten zurückgegeben. (Eine vollständige Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Das Anfügen einer Datenbank ist während einer Sicherung nicht zulässig.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Die durch <em>szFilename</em> angegebene Datenbankdatei muss schreibbar sein. Das Read-Only-Attribut darf nicht festgelegt werden, und der ausgeführte Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Die Datenbankdatei wird bereits von einem anderen Prozess geöffnet.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>In <em>szFilename</em>wurde ein ungültiger Pfad angegeben. <em>szFilename</em> muss ungleich NULL sein und auf einen gültigen Pfad verweisen.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Die Datenbankdatei wurde bereits von einer anderen Sitzung angefügt.</p> | 
| <p>JET_errFileNotFound</p> | <p>Die in <em>szFilename</em> angegebene Datei ist nicht vorhanden.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Beim primären Index tritt ein Fehler auf. Dies kann auf physische Beschädigungen (z. B. Datenträger- oder Speicherbeschädigung) hindekoren sein. Sie kann auch zurückgegeben werden, wenn eine Zuletzt geänderte Datenbank unter einem älteren Betriebssystem angefügt wird und sich der primäre Index über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Hinweisen.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Bei einem sekundären Index tritt ein Fehler auf. Dies kann auf physische Beschädigungen (z. B. Datenträger- oder Speicherbeschädigung) hindekoren sein. Sie kann auch zurückgegeben werden, wenn eine Zuletzt geänderte Datenbank unter einem älteren Betriebssystem angefügt wird und sich ein sekundärer Index über einer Spalte mit Unicode-Daten befindet. Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den Hinweisen. Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mithilfe des folgenden Befehls mit einem Offlinehilfsprogramm defragmentiert wird: <strong>esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Pro Instanz kann nur eine begrenzte Anzahl von Datenbanken angefügt werden. Der Grenzwert beträgt derzeit sieben Datenbanken pro Instanz.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Eine nichttale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p> | 



#### <a name="remarks"></a>Bemerkungen

Die Datenbankdatei wird mit [JetDetachDatabase](./jetdetachdatabase-function.md) oder [JetDetachDatabase2](./jetdetachdatabase2-function.md)getrennt.

Hinweise finden Sie unter [JetAttachDatabase.](./jetattachdatabase-function.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetAttachDatabase2W</strong> (Unicode) und <strong>JetAttachDatabase2A</strong> (ANSI) implementiert.</p> | 



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
