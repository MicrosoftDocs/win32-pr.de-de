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
ms.openlocfilehash: 9451844edc9f55bda75e5ec80e4958b3c474c919
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476356"
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

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Die -Instanz wurde mithilfe eines Aufrufs der <a href="gg294068(v=exchg.10).md">JetInit-Funktion</a> initialisiert, und dieser Vorgang kann daher nicht ausgeführt werden. Dies kann passieren, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Parameterwerts den Zustand der Datenbank-Engine nicht mehr beeinflussen kann.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion beendet</a> wurden.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Die angegebenen Tupelindexparameter waren ungültig. Dieser Fehler wird nur zurückgegeben, wenn <em>der</em>JET_paramIndexTuplesLengthMin , <em></em> <em>JET_paramIndexTuplesLengthMax</em>oder JET_paramIndexTuplesToIndexMax parameter auf einen ungültigen Wert festgelegt ist. Informationen zu diesen Parametern finden Sie unter <a href="gg294119(v=exchg.10).md">Indexparameter</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz initialisiert wird.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann passieren, wenn Folgendes auftritt:</p><ul><li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li><li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einer Zeichenfolge zu setzen, deren Länge außerhalb des rechtlichen Bereichs für den Parameter lag.</p></li><li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einem Dateipfad zu setzen, bei dem die Länge seiner absoluten Pfaddarstellung außerhalb des rechtlichen Bereichs für diesen Parameter lag.</p></li><li><p>Es wurde versucht, einen Ganzzahlwert-Systemparameter mit einer ganzen Zahl zu setzen, die außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li><li><p>Es wurde versucht, eine -JET_paramUnicodeIndexDefault mit <a href="gg294097(v=exchg.10).md"></a> einem NULL JET_UNICODEINDEX zeiger, einer ungültigen LCID oder einem nicht unterstützten Satz <strong>von LCMapString-Flags</strong> zu setzen.</p></li><li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li><li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem die <a href="gg294068(v=exchg.10).md">JetInit-Funktion</a> aufgerufen wurde, sich die Datenbank-Engine im Einzelinstanzmodus befindet und keine Sitzung angegeben wurde.</p></li><li><p>Der angegebene Systemparameter ist nur global, und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p></li><li><p>Der angegebene Systemparameter gilt nur pro Instanz, und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann nur von <strong>JetSetSessionParameter zurückgegeben werden,</strong> wenn Systemparameter festgelegt werden, die Dateisystempfade darstellen. Beispielsweise kann der <em>JET_paramSystemPath-Parameter</em> diesen Fehler zurückgeben. Informationen zu diesem Parameter finden Sie unter <a href="gg269235(v=exchg.10).md">Transaktionsprotokollparameter.</a></p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p><p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errInvalidInstance</p> | <p>Das Instanzhandy ist ungültig oder verweist auf eine heruntergefahrene Instanz.</p><p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 



Bei Erfolg wird der Systemparameter auf den angegebenen Wert festgelegt.

Bei einem Fehler bleibt der Wert des Systemparameters unverändert.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
