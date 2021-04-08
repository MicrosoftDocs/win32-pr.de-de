---
description: 'Weitere Informationen zu: jetopentable-Funktion'
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
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749705"
---
# <a name="jetopentable-function"></a>JetOpenTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentable-function"></a>JetOpenTable-Funktion

Die **jetopentable** -Funktion öffnet einen Cursor für eine zuvor erstellte Tabelle.

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

*-sid*

Der zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Der Daten Bank Bezeichner, der zum Suchen der Tabelle verwendet werden soll.

*sztablename*

Der Name der zu öffnenden Tabelle.

*pvparameters*

Veraltet. Auf **null** festgelegt.

*cbparameters*

Veraltet. Legen Sie den Wert auf 0 (null) fest.

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
<td><p>JET_bitTableDenyRead</p></td>
<td><p>Die Tabelle kann nicht für den Lesezugriff durch eine andere Daten banksitzung geöffnet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>Die Tabelle kann nicht für den Schreibzugriff durch eine andere Daten banksitzung geöffnet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>Die Seiten für diese Tabelle werden nicht zwischengespeichert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Ermöglicht DDL-Änderungen in Tabellen, die als fixedddl gekennzeichnet sind. Diese Option muss mit der Option JET_bitTableDenyRead verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Gibt einen Hinweis an, dass sich die Tabelle wahrscheinlich nicht im Puffer Cache befindet, und dass das vorab lesen für die Leistung von Vorteil sein kann.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Fordert den schreibgeschützten Zugriff auf die Tabelle an.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>Die Tabelle sollte sehr aggressiv vom Datenträger abgerufen werden, da die Anwendung Sie sequenziell scannt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Fordert Schreibzugriff auf die Tabelle an.</p></td>
</tr>
</tbody>
</table>


*pTableID*

Bei Erfolg verweist auf den Bezeichner der Tabelle. Bei einem Fehler ist der Inhalt für *pTableID* nicht definiert.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>DBID</em> ist kein gültiger Daten Bank Bezeichner.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Es wurde eine ungültige Kombination von <em>grbit</em> übermittelt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Der in <em>sztablename</em> angegebene Name ist ungültig.</p>
<p>Weitere Informationen zu gültigen Tabellennamen finden Sie unter dem Parameter " <em>sztablename</em> " in <a href="gg269210(v=exchg.10).md">jetkreatetable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Es wurde versucht, eine Tabelle zu öffnen, die in der Datenbank nicht vorhanden ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>Die Tabelle wird von einem anderen Daten Bank Vorgang verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Eine nicht schwerwiegende Warnung, die angibt, dass die Tabelle vom System verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>Die Tabelle wird durch einen anderen Daten Bank Vorgang gesperrt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Es wurde versucht, zu viele eindeutige Tabellen gleichzeitig zu öffnen. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Tabellen, die mit **jetopentable** geöffnet werden, sollten normalerweise mit [jetclosetable](./jetclosetable-function.md)geschlossen werden. Die Ausnahme von dieser Regel tritt auf, wenn **jetopentable** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)). Beim Rollback einer Transaktion wird die Tabelle automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit [jetclosetable](./jetclosetable-function.md)zu schließen.

Es ist zulässig, Systemtabellen mit **jetopentable** (z. b. MSysObjects, msysunicodefixup) zu öffnen. Das Schema der Systemtabellen kann sich ändern, sodass der Zugriff auf Systemtabellen nicht empfehlenswert ist. Die Anzahl der eindeutigen Tabellen, die gleichzeitig geöffnet werden können, wird direkt durch *JET_paramMaxOpenTables* beeinträchtigt. Wenn die Tabelle momentan geöffnet ist, wird ein neuer Cursor für die Tabelle erstellt. Cursor Ressourcen werden mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit *JET_paramMaxCursors* konfiguriert. Siehe auch [jetdupcursor](./jetdupcursor-function.md).

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
<td><p>Implementiert als <strong>jetopentablew</strong> (Unicode) und <strong>jetopentablea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetdupcursor](./jetdupcursor-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
