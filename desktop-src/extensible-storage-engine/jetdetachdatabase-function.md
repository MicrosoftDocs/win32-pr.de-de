---
description: 'Weitere Informationen zu: jetdetachdatabase-Funktion'
title: JetDetachDatabase-Funktion
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349928"
---
# <a name="jetdetachdatabase-function"></a>JetDetachDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdetachdatabase-function"></a>JetDetachDatabase-Funktion

Die **jetdetachdatabase** -Funktion gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*szFilename*

Der Name der zu trennenden Datenbank. Wenn *szFilename* **null** oder eine leere Zeichenfolge ist, werden alle an die " *gsid* " angefügten Datenbanken getrennt.

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
<td><p>Die Datenbank wird gesichert und kann nicht getrennt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Die Datenbank wurde von <a href="gg269299(v=exchg.10).md">jetopbank</a>geöffnet. Datenbanken müssen vor dem Trennen geschlossen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a> oder <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, eine Datenbank zu trennen, während eine Transaktion durchgeführt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn eine angefügte Datenbank (mit [jetattachdatabase](./jetattachdatabase-function.md)) geöffnet wurde, muss Sie vor dem trennen mit [jetclosedatabase](./jetclosedatabase-function.md) geschlossen werden.

Nur Windows 2000: Datenbanken, die vor dem Aufrufen von [jetterm](./jetterm-function.md) nicht getrennt wurden, werden automatisch erneut angefügt, wenn [jetinit das](./jetinit-function.md) nächste Mal aufgerufen wird.

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
<td><p>Implementiert als <strong>jetdetachdatabasew</strong> (Unicode) und <strong>jetdetachdatabasea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[Jetkreatedatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetterm](./jetterm-function.md)
