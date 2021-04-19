---
description: 'Weitere Informationen finden Sie hier: JetDetachDatabase2-Funktion'
title: JetDetachDatabase2-Funktion
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362839"
---
# <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2-Funktion

Die **JetDetachDatabase2** -Funktion gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.

**Windows XP:**  **JetDetachDatabase2** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*szFilename*

Der Name der zu trennenden Datenbank. Wenn *szFilename* **null** oder eine leere Zeichenfolge ist, werden alle an die " *gsid* " angefügten Datenbanken getrennt.

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
<td><p>JET_bitForceCloseAndDetach</p></td>
<td><p>Erzwingt, dass die Datenbank geschlossen und getrennt wird. Wird JET_bitForceCloseAndDetach nicht unterstützt, wird JET_errForceDetachNotAllowed zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitForceDetach</p></td>
<td><p>Erzwingt, dass die Datenbank getrennt wird. Wird JET_bitForceDetach nicht unterstützt, wird JET_errForceDetachNotAllowed zurückgegeben.</p></td>
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
<td><p>JET_errForceDetachNotAllowed</p></td>
<td><p>JET_bitForceDetach wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
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
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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
<td><p>Implementiert als <strong>JetDetachDatabase2W</strong> (Unicode) und <strong>JetDetachDatabase2A</strong> (ANSI).</p></td>
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
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetkreatedatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[Jetopumdatabase](./jetopendatabase-function.md)  
[Jetterm](./jetterm-function.md)
