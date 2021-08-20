---
description: Weitere Informationen finden Sie unter JetSetSessionParameter-Funktion.
title: JetSetSessionParameter-Funktion
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5766a503fbac8a8abae51c6022fe91e9ecca0d72e28cbecbaeed597862765bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891018"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetSetSessionParameter-Funktion** konfiguriert die Datenbank-Engine.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parameter

*sesid*

Gibt die Sitzung an, die für diesen Aufruf verwendet werden soll.

Wenn angegeben, wird die angegebene -Instanz ignoriert, und die der Sitzung zugeordnete -Instanz wird verwendet.

*sespartrenn*

Die ID des sitzungsparameters, der festgelegt werden soll.

*pvParam*

Die daten, die in diesem Sitzungsparameter festgelegt werden.

*cbParam*

Die Größe der bereitgestellten Daten.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Die -Instanz wurde mithilfe eines Aufrufs der <a href="gg294068(v=exchg.10).md">JetInit-Funktion</a> initialisiert, und dieser Vorgang kann daher nicht ausgeführt werden. Dies kann passieren, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Parameterwerts den Zustand der Datenbank-Engine nicht mehr beeinflussen kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion beendet</a> wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Die angegebenen Tupelindexparameter waren ungültig. Dieser Fehler wird nur zurückgegeben, wenn <em>JET_paramIndexTuplesLengthMin</em>, <em></em> <em>JET_paramIndexTuplesLengthMax</em>oder JET_paramIndexTuplesToIndexMax parameter auf einen ungültigen Wert festgelegt ist. Informationen zu diesen Parametern finden Sie unter <a href="gg294119(v=exchg.10).md">Indexparameter</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann passieren, wenn Folgendes auftritt:</p>
<ul>
<li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einer Zeichenfolge zu setzen, deren Länge außerhalb des rechtlichen Bereichs für den Parameter lag.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einem Dateipfad zu setzen, bei dem die Länge seiner absoluten Pfaddarstellung außerhalb des rechtlichen Bereichs für diesen Parameter lag.</p></li>
<li><p>Es wurde versucht, einen Ganzzahlwert-Systemparameter mit einer ganzen Zahl zu setzen, die außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, die JET_paramUnicodeIndexDefault null <a href="gg294097(v=exchg.10).md"></a> JET_UNICODEINDEX, eine ungültige LCID oder einen nicht unterstützten Satz <strong>von LCMapString-Flags</strong> zu setzen.</p></li>
<li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li>
<li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem die <a href="gg294068(v=exchg.10).md">JetInit-Funktion</a> aufgerufen wurde, sich die Datenbank-Engine im Einzelinstanzmodus befindet und keine Sitzung angegeben wurde.</p></li>
<li><p>Der angegebene Systemparameter ist nur global, und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p></li>
<li><p>Der angegebene Systemparameter gilt nur pro Instanz, und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann nur von <strong>JetSetSessionParameter zurückgegeben werden,</strong> wenn Systemparameter festgelegt werden, die Dateisystempfade darstellen. Beispielsweise kann der <em>JET_paramSystemPath</em> Parameter diesen Fehler zurückgeben. Informationen zu diesem Parameter finden Sie unter <a href="gg269235(v=exchg.10).md">Transaktionsprotokollparameter.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>Das Instanzhandy ist ungültig oder verweist auf eine heruntergefahrene Instanz.</p>
<p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Systemparameter auf den angegebenen Wert festgelegt.

Bei einem Fehler bleibt der Wert des Systemparameters unverändert.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Siehe auch

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
