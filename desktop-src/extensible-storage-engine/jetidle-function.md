---
description: 'Weitere Informationen zu: jetidle-Funktion'
title: Jetidle-Funktion
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866820"
---
# <a name="jetidle-function"></a>Jetidle-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetidle-function"></a>Jetidle-Funktion

Die **jetidle** -Funktion ist veraltet und sollte nur zu Testzwecken verwendet werden. **Jetidle** kann verwendet werden, um Cleanuptasks im Leerlauf auszuführen oder den Versionsspeicher Status in ESE zu überprüfen.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet wird.

*grbit*

Eine Gruppe von Bits, die die Optionen enthalten, die für diesen-Befehl verwendet werden sollen, einschließlich 0 (null) oder mehr der folgenden Bits:

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
<td><p>JET_bitIdleCompact</p></td>
<td><p>Löst die Bereinigung des Versionsspeicher aus.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIdleFlushBuffers</p></td>
<td><p>Für die zukünftige Verwendung reserviert. Wenn dieses Flag angegeben wird, gibt die API JET_errInvalidgrbit zurück.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIdleStatus</p></td>
<td><p>Gibt JET_wrnIdleFull zurück, wenn der Versionsspeicher größer als der Halbwert ist.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein für die API bereitgestellter <em>grbit</em> -Parameter war ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der entsprechende Vorgang ausgelöst, oder es wird ein Fehlercode angezeigt, der angibt, wie voll der Versionsspeicher vom angegebenen *grbit* ist.

Wenn diese Funktion fehlschlägt, wurde der angeforderte Vorgang nicht erfolgreich abgeschlossen.

#### <a name="remarks"></a>Bemerkungen

Der Versionsspeicher verwaltet den Snapshot-Isolations Mechanismus von ESE. Wenn der Versionsspeicher größer als der Halbwert ist, kann das Programm Transaktionen mit langer Laufzeit schließen. Wenn eine Transaktion mit langer Ausführungsdauer den Versionsspeicher erschöpft, hält ESE Schreibvorgänge für die Datenbank an.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)
