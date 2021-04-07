---
description: 'Weitere Informationen zu: jetopendatabase-Funktion'
title: JetOpenDatabase-Funktion
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760537"
---
# <a name="jetopendatabase-function"></a>JetOpenDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopendatabase-function"></a>JetOpenDatabase-Funktion

Die **jetopendatabase** -Funktion öffnet eine zuvor angefügte Datenbank mithilfe der [jetattachdatabase](./jetattachdatabase-function.md) -Funktion oder der [JetAttachDatabase2](./jetattachdatabase2-function.md) -Funktion für die Verwendung mit einer Daten banksitzung. Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*szFilename*

Der Name der Datenbank, die geöffnet werden soll.

*szconnect*

Reserviert. Auf NULL festgelegt.

*pdbid*

Ein Zeiger auf einen Puffer, der bei einem erfolgreichen-Aufrufwert den Bezeichner der Datenbank enthält. Wenn der-Befehl fehlschlägt, ist der Wert nicht definiert.

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
<td><p>JET_bitDbExclusive</p></td>
<td><p>Ermöglicht nur einer einzelnen Sitzung das Anfügen einer Datenbank. In der Regel können mehrere Sitzungen eine Datenbank öffnen.</p></td>
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
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Exklusiver Zugriff wurde angefordert, konnte aber nicht erteilt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben. " <em>szFilename</em> " darf nicht NULL sein und muss auf eine gültige Datei verweisen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Eine andere Sitzung hat die Datenbank bereits exklusiv (mit JET_bitDbExclusive) geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Es wurde versucht, mehr als eine Datenbank zu öffnen, und <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> wurde festgelegt. Weitere Informationen finden Sie unter <a href="gg294139(v=exchg.10).md">System Parameter</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>Die Datei wurde als schreibgeschützt angefügt, aber <strong>jetopsdatabase</strong> hat JET_bitDbReadOnly nicht bestanden. Die Datenbank wird immer noch mit Schreib geschütztem Zugriff geöffnet.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementiert als <strong>jetopendatabasew</strong> (Unicode) und <strong>jetopendatabasea</strong> (ANSI).</p></td>
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
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
