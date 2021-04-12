---
description: 'Weitere Informationen finden Sie unter: jetcomputestats-Funktion'
title: Jetcomputestats-Funktion
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218590"
---
# <a name="jetcomputestats-function"></a>Jetcomputestats-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcomputestats-function"></a>Jetcomputestats-Funktion

Die **jetcomputestats** -Funktion durchläuft jeden Index einer Tabelle, um genau die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index zu berechnen. Diese Informationen werden in Verbindung mit der Anzahl von Datenbankseiten, die für einen Index zugeordnet sind, und dem aktuellen Zeitpunkt der Berechnung in den Index Metadaten in der Datenbank gespeichert. Diese Daten können anschließend mit Informations Vorgängen abgerufen werden.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet wird. Beschreibt die Tabelle, für die Statistiken berechnet werden sollen.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Es ist ein Fehler aufgetreten, der erfordert, dass für diesen Vorgang alle Änderungen zurückgesetzt werden, das Transaktionsrollback selbst jedoch fehlgeschlagen ist</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden aktuelle Statistiken in den Daten Bank Katalogen für die Tabelle gespeichert, die mit dem angegebenen Cursor beschrieben wird.

Bei einem Fehler werden keine Updates jeglicher Art an der Datenbank vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann Ressourcen aufwendig sein, da jeder Index in einer Tabelle vollständig durchlaufen werden muss. [Jetgetrecordposition](./jetgetrecordposition-function.md) kann verwendet werden, um eine grobe Schätzung der Anzahl von Einträgen in einem Index zu erhalten, kann jedoch nicht die Anzahl der unterschiedlichen Werte in einem Index schätzen.

Die von diesem Vorgang berechneten Daten werden veraltet, und die Tabelle wird anschließend aktualisiert.

Aktualisierungen der von **jetcomputestats** vorgenommenen Datenbank werden verzögert durchgeführt. Dies bedeutet, dass keine Protokoll Leerung von diesem Vorgang begleitet wird und ein Systemabsturz nach einer Rückgabe von JET_errSuccess von **jetcomputestats** weiterhin dazu führen kann, dass diese Updates verloren gehen.

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
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[Jetgetrecordposition](./jetgetrecordposition-function.md)  
[Jetgettableinfo](./jetgettableinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetstopservice](./jetstopservice-function.md)
