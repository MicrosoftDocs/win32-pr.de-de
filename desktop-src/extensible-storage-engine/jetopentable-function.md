---
description: Weitere Informationen finden Sie unter JetOpenTable-Funktion.
title: JetOpenTable-Funktion
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 816bed58b4c886cc2e9984a44e1e4e10f7768f4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472520"
---
# <a name="jetopentable-function"></a>JetOpenTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentable-function"></a>JetOpenTable-Funktion

Die **JetOpenTable-Funktion** öffnet einen Cursor für eine zuvor erstellte Tabelle.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der zu verwendende Datenbanksitzungskontext.

*Dbid*

Der Datenbankbezeichner, der zum Suchen der Tabelle verwendet werden soll.

*szTableName*

Der Name der zu öffnenden Tabelle.

*pvParameters*

Veraltet. Legen Sie auf **NULL fest.**

*cbParameters*

Veraltet. Legen Sie auf 0 (null) fest.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableDenyRead</p> | <p>Die Tabelle kann nicht für den Lesezugriff durch eine andere Datenbanksitzung geöffnet werden.</p> | 
| <p>JET_bitTableDenyWrite</p> | <p>Die Tabelle kann nicht für den Schreibzugriff durch eine andere Datenbanksitzung geöffnet werden.</p> | 
| <p>JET_bitTableNoCache</p> | <p>Speichern Sie die Seiten für diese Tabelle nicht zwischen.</p> | 
| <p>JET_bitTablePermitDDL</p> | <p>Ermöglicht DDL-Änderungen für Tabellen, die als FixedDDL gekennzeichnet sind. Diese Option muss mit der Option JET_bitTableDenyRead verwendet werden.</p> | 
| <p>JET_bitTablePreread</p> | <p>Gibt einen Hinweis darauf an, dass sich die Tabelle wahrscheinlich nicht im Puffercache befindet und dass das Vorlesen für die Leistung von Vorteil sein kann.</p> | 
| <p>JET_bitTableReadOnly</p> | <p>Fordert schreibgeschützten Zugriff auf die Tabelle an.</p> | 
| <p>JET_bitTableSequential</p> | <p>Die Tabelle sollte sehr aggressiv vom Datenträger vorab abgerufen werden, da die Anwendung sie sequenziell scannt.</p> | 
| <p>JET_bitTableUpdatable</p> | <p>Fordert Schreibzugriff auf die Tabelle an.</p> | 



*Ptableid*

Bei Erfolg verweist auf den Bezeichner der Tabelle. Bei einem Fehler ist der Inhalt *für ptableid* nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p><em>dbid</em> ist kein gültiger Datenbankbezeichner.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine fehlerhafte Kombination von <em>Grbit wurde</em> übergeben.</p> | 
| <p>JET_errInvalidName</p> | <p>Der in <em>szTableName gegebene Name</em> ist ungültig.</p><p>Weitere Informationen zu gültigen Tabellennamen finden Sie unter <em>dem szTableName-Parameter</em> in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Es wurde versucht, eine Tabelle zu öffnen, die in der Datenbank nicht vorhanden ist.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p> | 
| <p>JET_errTableInUse</p> | <p>Die Tabelle wird von einem anderen Datenbankvorgang verwendet.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Eine nichtfatale Warnung, die angibt, dass die Tabelle vom System verwendet wird.</p> | 
| <p>JET_errTableLocked</p> | <p>Die Tabelle wird durch einen anderen Datenbankvorgang gesperrt.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Es wurde versucht, zu viele eindeutige Tabellen gleichzeitig zu öffnen. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p> | 



#### <a name="remarks"></a>Hinweise

Tabellen, die mit **JetOpenTable geöffnet werden,** sollten normalerweise mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md) Die Ausnahme von dieser Regel tritt auf, wenn **JetOpenTable** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [JetRollback](./jetrollback-function.md)). Beim Roll back einer Transaktion wird die Tabelle automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit [JetCloseTable zu schließen.](./jetclosetable-function.md)

Es ist gesetzlich, Systemtabellen mit **JetOpenTable** zu öffnen (z. B. MSysObjects, MSysUnicodeFixup). Das Schema der Systemtabellen kann sich ändern, daher wird davon abgeraten, auf Systemtabellen zu zugreifen. Die Anzahl eindeutiger Tabellen, die gleichzeitig geöffnet werden können, wird direkt von *JET_paramMaxOpenTables.* Wenn die Tabelle derzeit geöffnet ist, wird ein neuer Cursor für die Tabelle erstellt. Cursorressourcen werden mit [JetSetSystemParameter mit JET_paramMaxCursors.](./jetsetsystemparameter-function.md)  Siehe auch [JetDupCursor](./jetdupcursor-function.md).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetOpenTableW</strong> (Unicode) und <strong>JetOpenTableA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
