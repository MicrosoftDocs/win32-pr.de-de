---
description: 'Weitere Informationen finden Sie unter: JetGetSystemParameter-Funktion'
title: JetGetSystemParameter-Funktion
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 608a9c464ca645668483934a28a3f79945cd443d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984743"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter-Funktion

Die **JetGetSystemParameter-Funktion** liest die zahlreichen Konfigurationseinstellungen der Datenbank-Engine.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **NULL sein.**

Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **NULL** sein oder die tatsächliche Instanz enthalten, die von [JetInit](./jetinit-function.md)zurückgegeben wird. In beiden Fällen werden alle Systemparametereinstellungen aus dieser einen Instanz gelesen. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, kann dieser Parameter **NULL** oder ein Zeiger auf eine Instanz sein, die mit [JetInit](./jetinit-function.md) oder [JetCreateInstance erstellt wurde.](./jetcreateinstance-function.md) Wenn dieser Parameter **NULL ist,** wird die globale Systemparametereinstellung (oder der Standardwert) gelesen. Wenn dieser Parameter eine -Instanz ist, wird die Systemparametereinstellung für diese Instanz gelesen.

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

Wenn angegeben, wird die angegebene -Instanz ignoriert, und die der Sitzung zugeordnete -Instanz wird verwendet.

*paramid*

Die ID des Systemparameters, der gelesen wird.

Eine [vollständige Liste der](./extensible-storage-engine-system-parameters.md) Systemparameter und deren Eigenschaften finden Sie unter Systemparameter.

*plParam*

Der Ausgabepuffer, der den Wert des ausgewählten Systemparameters empfängt, wenn dieser Systemparameter einen ganzzahligen Typ auf hat.

*szParam*

Der Ausgabepuffer, der den Wert des ausgewählten Systemparameters empfängt, wenn dieser Systemparameter einen Zeichenfolgentyp auf hat.

*cbMax*

Die maximale Größe des Zeichenfolgenausgabepuffers in Bytes.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInitInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz initialisiert wird.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p><p>Dies kann für <strong>JetGetSystemParameter passieren, wenn:</strong></p><ul><li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li><li><p>Für den angegebenen Systemparameter muss der ganzzahlige Ausgabepuffer bereitgestellt werden, und der Ausgabepufferzeiger war <strong>NULL.</strong></p></li><li><p>Für den angegebenen Systemparameter muss ein Zeichenfolgenausgabepuffer bereitgestellt werden, und der Ausgabepufferzeiger war <strong>NULL.</strong></p><p><strong>Windows Vista:</strong> Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li><li><p>Für den angegebenen Systemparameter muss ein Zeichenfolgenausgabepuffer bereitgestellt werden, und die Größe dieses Ausgabepuffers ist zu klein, um eine mit NULL beendete Zeichenfolge zu akzeptieren.</p><p><strong>Windows Vista:</strong> Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li><li><p>Der angegebene Systemparameter kann nicht gelesen werden, da er schreibgeschützt ist.</p></li><li><p>Der angegebene Systemparameter ist nur global, und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter zu lesen. Dies kann nur bei Windows XP und späteren Versionen passieren.</p></li><li><p>Der angegebene Systemparameter gilt nur pro Instanz, und es wurde versucht, den globalen Wert für diesen Systemparameter zu lesen. Dies kann nur bei Windows XP und späteren Versionen passieren.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung. Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errInvalidInstance</p> | <p>Das Instanzhand handle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde. Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p><p><strong>Windows Vista:</strong> Dieser Fehler wird nur von Windows Vista und späteren Versionen zurückgegeben.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um die gesamte Systemparametereinstellung zu empfangen.</p><p>Der Ausgabepuffer wurde mit einem so großen Teil der Systemparametereinstellung gefüllt, wie es passen würde. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer auf NULL beendet.</p><p><strong>Hinweis:  </strong> Dieser Fehler wird nicht von allen Releases zurückgegeben. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Fehler beim Vorgang, weil der Ausgabepuffer zu klein war, um die gesamte Systemparametereinstellung zu empfangen.</p><p><strong>Hinweis:  </strong> Dieser Fehler wird in einigen Fällen nicht zurückgegeben, um die Anwendungskompatibilität zu gewährleisten. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p><p><strong>Windows Vista:</strong> Dieser Fehler wird nur von Windows Vista und späteren Versionen zurückgegeben.</p> | 



Bei Erfolg wird der für den angeforderten Systemparameter geeignete Ausgabepuffer auf den Wert dieses Systemparameters festgelegt.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.

#### <a name="remarks"></a>Bemerkungen

Es gibt ein wichtiges Problem in dieser API, das in allen Releases vorhanden ist. Wenn ein Systemparameter mit einem Zeichenfolgenwert angefordert wird und der Ausgabepuffer zu klein ist, um die gesamte Systemparametereinstellung zu empfangen, JET_wrnBufferTruncated NICHT zurückgegeben. JET_errSuccess wird stattdessen zurückgegeben. Wenn die Länge der zurückgegebenen Zeichenfolge gleich der  Größe des Ausgabepuffers kleiner als das NULL-Abschlusszeichen ist, sollte der Aufrufer so reagieren, als JET_wrnBufferTruncated zurückgegeben würden. Wenn ein Zeichenfolgenausgabepuffer der Größe 0 (null) angegeben wird, sollte der Aufrufer so reagieren, als JET_errInvalidParameter zurückgegeben.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetSystemParameterW</strong> (Unicode) und <strong>JetGetSystemParameterA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
