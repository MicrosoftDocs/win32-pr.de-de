---
description: 'Weitere Informationen zu: jetregistercallback-Funktion'
title: JetRegisterCallback-Funktion
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348172"
---
# <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion

Die **jetregistercallback** -Funktion ermöglicht es der Anwendung, die Datenbank-Engine so zu konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung ausgegeben werden. Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von [jetterm](./jetterm-function.md)heruntergefahren wird.

**Windows XP: jetregistercallback** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*cbyp*

Eine Bitmaske, die aus den Rückruf Gründen besteht, für die die Anwendung Benachrichtigungen empfangen möchte.

Um diese Bitmaske zu erstellen, führen Sie einfach oder zusammengültige Rückruf Gründe aus der [JET_CBTYP](./jet-cbtyp.md) Enumeration aus.

*pCallback*

Der Funktionszeiger auf die Rückruffunktion für die Anwendung.

*pvcontext*

Gibt einen Kontext Zeiger an, der der Rückruffunktion für die Anwendung zugewiesen wird.

*phcallbackid*

Gibt ein Handle zurück, das später verwendet werden kann, um die Registrierung der angegebenen Rückruffunktion mit [jetunregistercallback](./jetunregistercallback-function.md)abzubrechen.

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dieser Fehler wird von <strong>jetregistercallback</strong> zurückgegeben, wenn Folgendes gilt:</p>
<ul>
<li><p><em>cbyp</em> ist 0 (null),</p></li>
<li><p><em>pCallback</em> ist NULL.</p></li>
<li><p><em>phcallbackid</em> ist NULL.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der angegebene Rückruf für die angegebenen Rückruf Gründe mit der Tabelle, die dem angegebenen Cursor zugeordnet ist, registriert. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler wird der Rückruf nicht registriert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Diese Methode stellt eine Möglichkeit bereit, mit der die Anwendung flüchtige Rückrufe einer Tabelle in einer Datenbank zuordnen können. Wenn die Anwendung persistente Rückrufe einer Tabelle in der Datenbank zuordnen möchte, sollte Sie den Rückruf an [JET_TABLECREATE](./jet-tablecreate-structure.md) mithilfe von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)übergeben.

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

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[Jetterm](./jetterm-function.md)  
[Jetunregistercallback](./jetunregistercallback-function.md)
