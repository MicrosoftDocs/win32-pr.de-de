---
description: Weitere Informationen finden Sie unter JetSetSystemParameter-Funktion.
title: JetSetSystemParameter-Funktion
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da3dc4c0d211039378b5cc1301a84e35f67ab24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475796"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter-Funktion

Mit **der JetSetSystemParameter-Funktion** werden die zahlreichen Konfigurationseinstellungen der Datenbank-Engine festgelegt.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parameter

*Pinstance*

Gibt die -Instanz an, die für diesen Aufruf verwendet werden soll.

**Windows 2000:**  Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **NULL sein.**

**Windows XP:**  Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **NULL** sein oder die tatsächliche Instanz enthalten, die von [JetInit](./jetinit-function.md)zurückgegeben wird. In beiden Fällen werden alle Systemparametereinstellungen aus dieser einen Instanz gelesen. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, kann dieser Parameter **NULL** oder ein Zeiger auf eine Instanz sein, die mit [JetInit](./jetinit-function.md) oder [JetCreateIndex erstellt wurde.](./jetcreateindex-function.md) Wenn dieser Parameter **NULL ist,** wird die globale Systemparametereinstellung (oder der Standardwert) gelesen. Wenn dieser Parameter eine -Instanz ist, wird die Systemparametereinstellung für diese Instanz gelesen.

Obwohl dies technisch gesehen ein out-Parameter ist, ändert diese API nie den Inhalt des bereitgestellten Puffers.

*sesid*

Gibt die Sitzung an, die für diesen Aufruf verwendet werden soll.

Wenn angegeben, wird die angegebene -Instanz ignoriert, und die der Sitzung zugeordnete -Instanz wird verwendet.

*paramid*

Die ID des Systemparameters, der festgelegt wird. Eine [vollständige Liste der](./extensible-storage-engine-system-parameters.md) Systemparameter und deren Eigenschaften finden Sie unter Systemparameter.

*lParam*

Gibt den Wert an, der für den ausgewählten Systemparameter festgelegt werden soll, wenn dieser Systemparameter einen ganzzahligen Typ auf hat.

*szParam*

Gibt den Wert für den ausgewählten Systemparameter an, wenn dieser Systemparameter einen Zeichenfolgentyp auf hat.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p><p><strong>Windows Vista:</strong>  Bei Windows Vista und späteren Versionen kann der Erfolg ohne Änderung des Werts des Systemparameters zurückgegeben werden. Weitere Informationen finden JET_paramEnableAdvanced im Thema <a href="gg269346(v=exchg.10).md">Metaparameter</a> im Thema "Systemparameter".</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Die -Instanz wurde mithilfe eines Aufrufs von <a href="gg294068(v=exchg.10).md">JetInit</a> initialisiert, und dieser Vorgang kann daher nicht ausgeführt werden. Dies kann bei <strong>JetSetSystemParameter</strong> der Fall sein, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem sich eine Änderung des Werts nicht auf den Zustand der Datenbank-Engine auswirken kann.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Die angegebenen Tupelindexparameter waren ungültig. Dieser Fehler kann nur von <strong>JetSetSystemParameter</strong> zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a> <a href="gg294119(v=exchg.10).md"></a> , <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder JET_paramIndexTuplesToIndexMax auf einen ungültigen Wert festgelegt wird.</p><p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p> | 
| <p>JET_errInitInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz initialisiert wird.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetSetSystemParameter der Fall</strong> sein, wenn:</p><ul><li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li><li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einer Zeichenfolge zu setzen, deren Länge außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li><li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einem Dateipfad zu setzen, bei dem die Länge seiner absoluten Pfaddarstellung außerhalb des rechtlichen Bereichs für diesen Parameter lag.</p><p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li><li><p>Es wurde versucht, einen Ganzzahlwert-Systemparameter mit einer ganzen Zahl zu setzen, die außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li><li><p>Es wurde versucht, JET_paramUnicodeIndexDefault NULL-JET_UNICODEINDEX, eine ungültige LCID oder einen nicht unterstützten Satz von LCMapString-Flags zu setzen. <strong></strong><a href="gg294097(v=exchg.10).md"></a></p><p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li><li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li><li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem <a href="gg294068(v=exchg.10).md">JetInit</a> aufgerufen wurde, sich die Datenbank-Engine im Einzelinstanzmodus befindet und keine Sitzung angegeben wurde.</p><p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li><li><p>Der angegebene Systemparameter ist nur global, und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p><p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li><li><p>Der angegebene Systemparameter gilt nur pro Instanz, und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p><p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann nur von <strong>JetSetSystemParameter zurückgegeben werden,</strong> wenn Systemparameter festgelegt werden, die Dateisystempfade darstellen. Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> Fehler zurückgeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p><p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errInvalidInstance</p> | <p>Das Instanzhand handle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</p><p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p><p><strong>Windows Vista:</strong>  Dieser Fehler wird nur von Windows Vista und späteren Versionen zurückgegeben.</p> | 



Bei Erfolg wird die Einstellung für den Systemparameter auf den angegebenen Wert festgelegt.

Bei einem Fehler bleibt die Einstellung für den Systemparameter unverändert.

#### <a name="remarks"></a>Hinweise

**JetSetSystemParameter** führt eine schlechte Validierung der ausgewählten Einstellung für jeden Systemparameter durch. Es muss darauf achten, dass sie sich nicht auf diese Überprüfung verlassen, um gute Einstellungen zu erzwingen. Achten Sie besonders auf die Beschreibung der einzelnen Systemparameter, und befolgen Sie diese Richtlinien, um eine gute Systemparametereinstellung zu erhalten.

Es gibt eine Reihe von Systemparametern, die immer festgelegt werden sollten, um zu gewährleisten, dass die Datenbank-Engine wie vorgesehen funktioniert. Insbesondere sollten alle Systemparameter, die sich auf das physische Layout der von der Datenbank-Engine verwendeten Dateien auswirken, immer festgelegt werden. Weitere Informationen finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md).

Jeder Systemparameter hat einen Standardwert. Diese Standardwerte haben sich im Laufe der Zeit weiterentwickelt und sind recht willkürlich. Es wird dringend empfohlen, dass eine Anwendung alle Standardwerte auswertet, um sicherzustellen, dass sie geeignet sind. Wenn sie nicht geeignet sind, sollten sie von der Anwendung konfiguriert werden. Dies ist wichtig, da viele dieser Parameter die Zuverlässigkeit, Leistung und Ressourcenauslastung der Datenbank-Engine stark beeinträchtigen können.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetSetSystemParameterW</strong> (Unicode) und <strong>JetSetSystemParameterA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
