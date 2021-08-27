---
description: Weitere Informationen finden Sie unter JetCreateDatabase-Funktion.
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
ms.openlocfilehash: b7b3998d25d4f54d5150ad2a7a7d523f943d2eb7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465067"
---
# <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreatedatabase-function"></a>JetCreateDatabase-Funktion

Mit **der JetCreateDatabase-Funktion** wird eine Datenbankdatei erstellt und angefügt, die mit der ESE-Datenbank-Engine verwendet werden soll. Das [Aufrufen von JetCreateDatabase2](./jetcreatedatabase2-function.md) mit *cpgDatabaseSizeMax* auf 0 (null) ist identisch mit dem Aufrufen von **JetCreateDatabase,** bei dem *szConnect* auf NULL festgelegt ist. Derzeit können bis zu sieben Datenbanken pro Instanz erstellt werden.

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

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Wenn <strong>JetCreateDatabase</strong> aufgerufen wird und die Datenbank bereits vorhanden ist, ist der API-Aufruf standardmäßig nicht möglich, und die ursprüngliche Datenbank wird nicht überschrieben. JET_bitDbOverwriteExisting ändert dieses Verhalten, und die alte Datenbank wird durch eine neue überschrieben. Windows XP und höher.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff deaktiviert die Protokollierung. Das Festlegen dieses Bits verliert die Möglichkeit, Protokolldateien wiederzuverspielen und die Datenbank nach einem schwerwiegenden Ereignis in einem konsistenten nutzbaren Zustand wiederhergestellt zu haben.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>Durch JET_bitDbShadowingOff wird die Duplizierung einiger interner Datenbankstrukturen (Schatten) deaktiviert. Die Duplizierung dieser Strukturen erfolgt aus Resilienz- und JET_bitDbShadowingOff diese Resilienz zu beseitigen.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>Die Datenbank mit dem Namen in <em>szFilename</em> ist bereits vorhanden. Wenn dieser Fehler zurückgegeben wird, wird die Datenbank nicht angefügt.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Kann zurückgegeben werden, wenn exklusiver Zugriff angefordert wurde, aber nicht gewährt werden konnte oder wenn die Datenbank bereits von einer anderen Sitzung exklusiv geöffnet wurde.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Wird <em>zurückgegeben, wenn cpgDatabaseSizeMax</em> größer ist als die maximale Anzahl von Seiten, die in einer Datenbank zulässig sind. Der aktuelle Höchstwert ist 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>In szFilename wurde ein <em>ungültiger Pfad angegeben.</em> <em>szFilename</em> muss nicht NULL sein. Standardmäßig muss <em>szFilename</em> auf ein Verzeichnis verweisen, das vorhanden ist. Der Pfad wird erstellt, wenn <em>JET_paramCreatePathIfNotExist</em> festgelegt ist (siehe <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Gibt an, dass eine andere Sitzung die Datenbank bereits exklusiv geöffnet hat (mit JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Die Datenbankdatei wurde bereits von einer anderen Sitzung angefügt.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, während einer Transaktion eine Datenbank zu erstellen.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Es wurde versucht, mehrere Datenbanken zu öffnen, und JET_paramOneDatabasePerSession wurde festgelegt. Weitere Informationen <a href="gg269337(v=exchg.10).md">finden Sie unter Datenbankparameter.</a></p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil der Arbeitsspeicher nicht zugeordnet werden konnte.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden. Der Grenzwert liegt derzeit bei sieben Datenbanken pro Instanz.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Eine nichtfatale Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly gibt an, dass die Datei schreibgeschützt angefügt wurde, <strong>JetCreateDatabase</strong> jedoch keine JET_bitDbReadOnly. Die Datenbank wird weiterhin mit schreibgeschützten Zugriff geöffnet.</p> | 



#### <a name="remarks"></a>Hinweise

Wenn die in *szFilename* angegebene Datenbank vorhanden ist und JET_bitDbOverwriteExisting übergeben wurde, ist der API-Aufruf nicht erfolgreich. Wenn JET_bitDbOverwriteExisting übergeben wurde, wird die alte Datenbankdatei zuerst gelöscht.

Wenn die API eine Datenbankdatei erstellt und dann auf einen weiteren Fehler trifft, wird die Datei bereinigt und gelöscht.

**JetCreateDatabase** öffnet die Datenbank implizit. Es ist nicht notwendigerweise, [anschließend JetOpenDatabase auf aufruft.](./jetopendatabase-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetCreateDatabaseW</strong> (Unicode) und <strong>JetCreateDatabaseA</strong> (ANSI) implementiert.</p> | 



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
