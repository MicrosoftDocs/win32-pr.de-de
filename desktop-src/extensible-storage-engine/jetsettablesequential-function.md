---
description: 'Weitere Informationen zu: jetsettablesequential-Funktion'
title: Jetsettablesequential-Funktion
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348359"
---
# <a name="jetsettablesequential-function"></a>Jetsettablesequential-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>Jetsettablesequential-Funktion

Die **jetsettablesequential** -Funktion benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten aktuellen Index scannt, der einen bestimmten Cursor enthält. Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten.

**Windows XP:**  **jetsettablesequential** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>Diese Option wird verwendet, um in Vorwärtsrichtung zu indizieren.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> wurde in Windows 7 eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>Diese Option wird verwendet, um rückwärts zu indizieren.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> wurde in Windows 7 eingeführt.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der-Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>stillgelegt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der aktuelle Index des Cursors für einen sequenziellen Scan des gesamten Indexes optimiert. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung an der Konfiguration des Cursors. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Wenn die Anwendung eine bekannte Teilmenge eines Indexes effizient scannen muss, wird eine ähnliche Optimierung auch immer dann durchgeführt, wenn ein Index Bereich mithilfe von [jetsetindexrange](./jetsetindexrange-function.md)festgelegt wird. Diese Optimierung ist nur unter Windows XP und höheren Versionen verfügbar.

Wenn die Anwendung eine unbekannte Teilmenge eines Indexes effizient scannen muss, sollte keine Aktion ausgeführt werden. Die Engine kann das Scan Verhalten automatisch erkennen und Daten im Voraus abrufen. Dieses Verhalten ist jedoch nicht so aggressiv.

Durch diese Optimierung wird das Scannen des primären Indexes effizient und das Scannen nur der Index Eintrags Daten in einem sekundären Index effizient durchsucht. Es wird nicht überprüft, dass ein sekundärer Index gescannt wird, während Daten Satz Daten effizient abgerufen werden. Dies liegt daran, dass die Engine für die Daten Satz Daten keinen Lesevorgang ausführt.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)  
[Jetstopservice](./jetstopservice-function.md)
