---
description: Weitere Informationen finden Sie in der jetabessionparameter-Funktion
title: Jetabessionparameter-Funktion
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
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958793"
---
# <a name="jetsetsessionparameter-function"></a>Jetabessionparameter-Funktion


_**Gilt für:** Windows | Windows Server_

Die **Jet** -Sitzungs Parameter-Funktion konfiguriert die Datenbank-Engine.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parameter

*-sid*

Gibt die Sitzung an, die für diesen-Befehl verwendet werden soll.

Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.

*sesparamid*

Die ID des festzulegenden Sitzungs Parameters.

*pvParam*

Die in diesem Sitzungs Parameter festzulegenden Daten.

*cbparam*

Die Größe der bereitgestellten Daten.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).

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
<td><p>Die Instanz wurde mithilfe eines Aufrufens der <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion initialisiert, und dieser Vorgang kann nicht als Ergebnis ausgeführt werden. Dies kann vorkommen, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Parameter Werts nicht mehr den Status der Datenbank-Engine beeinflussen kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Die angegebenen tupelindexparameter waren unzulässig. Dieser Fehler wird nur zurückgegeben, wenn der <em>JET_paramIndexTuplesLengthMin</em>-, <em>JET_paramIndexTuplesLengthMax</em>-oder <em>JET_paramIndexTuplesToIndexMax</em> -Parameter auf einen unzulässigen Wert festgelegt ist. Weitere Informationen zu diesen Parametern finden Sie unter <a href="gg294119(v=exchg.10).md">index Parameter</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann vorkommen, wenn Folgendes geschieht:</p>
<ul>
<li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einer Zeichenfolge festzulegen, deren Länge außerhalb des gültigen Bereichs für den Parameter lag.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einem Dateipfad festzulegen, bei dem die Länge der absoluten Pfad Darstellung außerhalb des gültigen Bereichs für diesen Parameter liegt.</p></li>
<li><p>Es wurde versucht, einen ganzzahligen Wert mit einem ganzzahligen Wert festzulegen, der außerhalb des gültigen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, JET_paramUnicodeIndexDefault mit einem NULL- <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Zeiger, einer ungültigen LCID oder einem nicht unterstützten Satz von <strong>LCMapString</strong> -Flags festzulegen.</p></li>
<li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li>
<li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem die <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion aufgerufen wurde, die Datenbank-Engine sich im Einzel Instanz-Modus befindet und keine Sitzung angegeben wurde.</p></li>
<li><p>Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p></li>
<li><p>Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler wird möglicherweise nur von <strong>jetdeptessionparameter</strong> zurückgegeben, wenn Systemparameter festgelegt werden, die Dateisystem Pfade darstellen. Beispielsweise kann der <em>JET_paramSystemPath</em> -Parameter diesen Fehler zurückgeben. Weitere Informationen zu diesem Parameter finden Sie unter <a href="gg269235(v=exchg.10).md">Transaktionsprotokoll Parameter</a>.</p></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p>Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</p>
<p>Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Systemparameter auf den bereitgestellten Wert festgelegt.

Bei einem Fehler bleibt der Wert des System Parameters unverändert.

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


#### <a name="see-also"></a>Siehe auch

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[Jetgetsystemparameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
