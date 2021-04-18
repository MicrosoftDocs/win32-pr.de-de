---
description: Weitere Informationen finden Sie in der jetabessioncontext-Funktion
title: Jetabessioncontext-Funktion
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345762"
---
# <a name="jetsetsessioncontext-function"></a>Jetabessioncontext-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>Jetabessioncontext-Funktion

Die **jetsetsessioncontext** -Funktion verknüpft eine Sitzung mit dem aktuellen Thread unter Verwendung des angegebenen Kontext Handles. Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im gleichen Thread ausgeführt werden muss.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*ulcontext*

Ein eindeutiger Bezeichner, dem diese Sitzung zugeordnet wird.

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben. Dieser Fehler wird von <strong>jetin</strong> den folgenden Bedingungen zurückgegeben:</p>
<ul>
<li><p><em>ulcontext</em> ist NULL.</p></li>
<li><p><em>ulcontext</em> ist-1</p></li>
</ul></td>
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
<td><p>JET_errSessionContextAlreadySet</p></td>
<td><p>Die Sitzung konnte dem aktuellen Thread nicht zugeordnet werden, da Sie bereits einem Thread zugeordnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird die Sitzung dem aktuellen Thread zugeordnet. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, bleibt der Sitzungszustand unverändert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Eine Sitzung wird in der Regel an einen bestimmten Thread für die Dauer einer Transaktion gebunden. Dieses Verhalten soll Anwendungen dabei helfen, die konzeptionell beschädigte Freigabe einer einzelnen Sitzung unter mehreren Threads zu erkennen und zu verhindern. Manchmal funktioniert diese einfache Überprüfung nicht mit der Architektur der Anwendung. Wenn die Anwendung z. b. serverseitige Objekte mithilfe eines Thread Pools hostet und Transaktionen mehrere Server Aufrufe an ein bestimmtes Objekt überspannen, kann dieser Schutz dazu führen, dass einige dieser Aufrufe mit JET_errSessionSharingViolation fehlschlagen, obwohl das Verwendungs Muster korrekt ist. Diese Situation tritt häufig bei COM-Objekt Servern auf.

**Jetabsitzungskontext** und [jetressitzungskontext](./jetresetsessioncontext-function.md) lösen dieses Problem, indem Sie die Überprüfung dieser Sitzung ein wenig flexibler gestalten. Wenn die Anwendung mit einer bestimmten Sitzung eine Reihe von ESE-API-aufrufen durchführen soll, wird der Sitzungs Kontext zuerst auf einen bestimmten Wert festgelegt. Durch diese Aktion wird die Sitzung dem aufrufenden Thread zugeordnet. Im vorliegenden Beispiel könnte dieser Kontext die Adresse des Objekts sein, das das Jet-Sitzungs Handle enthält. Nachdem die ESE-API-Aufrufe durchgeführt wurden, setzt die Anwendung den Sitzungs Kontext zurück. Durch diese Aktion wird die Zuordnung der Sitzung zum aufrufenden Thread aufgehoben. Das-Objekt und seine Sitzung können dann von einem anderen Thread verwendet werden, auch wenn die Sitzung über eine aktive Transaktion verfügt.

Es ist wichtig zu beachten, dass **jetctessioncontext** aufgerufen werden muss, bevor eine Transaktion in dieser Sitzung geöffnet wird, oder die Zuordnung funktioniert nicht.

**Jetsezessioncontext** ist Thread sicher. Mehrere Threads können gleichzeitig versuchen, einen Thread Kontext in derselben Sitzung festzulegen, und nur ein Thread wird gewonnen. Diese Tatsache kann von der Anwendung verwendet werden, um eine Sitzung aus einem Pool zuzuordnen, ohne dass der externe Zustand über die Zuordnung gespeichert wird.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[Jetstopservice](./jetstopservice-function.md)
