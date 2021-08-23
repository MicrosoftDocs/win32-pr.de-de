---
description: 'Weitere Informationen finden Sie unter: JetSetSystemParameter-Funktion'
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
ms.openlocfilehash: 8a30e1d8d18d5abe4d4c429cc27333cf8884e46979f1a0e1058bd0a33f54f5a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780340"
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

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p>
<p><strong>Windows Vista:</strong>  Bei Windows Vista und späteren Versionen kann der Erfolg ohne Änderung des Werts des Systemparameters zurückgegeben werden. Weitere Informationen finden JET_paramEnableAdvanced im Thema <a href="gg269346(v=exchg.10).md">Metaparameter</a> im Thema "Systemparameter".</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Die -Instanz wurde mithilfe eines Aufrufs von <a href="gg294068(v=exchg.10).md">JetInit</a> initialisiert, und dieser Vorgang kann daher nicht ausgeführt werden. Dies kann bei <strong>JetSetSystemParameter</strong> der Fall sein, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem sich eine Änderung des Werts nicht auf den Zustand der Datenbank-Engine auswirken kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Die angegebenen Tupelindexparameter waren ungültig. Dieser Fehler kann nur von <strong>JetSetSystemParameter</strong> zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a> <a href="gg294119(v=exchg.10).md"></a> , <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder JET_paramIndexTuplesToIndexMax auf einen ungültigen Wert festgelegt wird.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetSetSystemParameter der Fall</strong> sein, wenn:</p>
<ul>
<li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einer Zeichenfolge zu setzen, deren Länge außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichenfolgenwert mit einem Dateipfad zu setzen, bei dem die Länge seiner absoluten Pfaddarstellung außerhalb des rechtlichen Bereichs für diesen Parameter lag.</p>
<p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li>
<li><p>Es wurde versucht, einen Ganzzahlwert-Systemparameter mit einer ganzen Zahl zu setzen, die außerhalb des rechtlichen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, JET_paramUnicodeIndexDefault NULL-JET_UNICODEINDEX, eine ungültige LCID oder einen nicht unterstützten Satz von LCMapString-Flags zu setzen. <strong></strong> <a href="gg294097(v=exchg.10).md"></a></p>
<p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und späteren Versionen geschehen.</p></li>
<li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li>
<li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem <a href="gg294068(v=exchg.10).md">JetInit</a> aufgerufen wurde, sich die Datenbank-Engine im Einzelinstanzmodus befindet und keine Sitzung angegeben wurde.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li>
<li><p>Der angegebene Systemparameter ist nur global, und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li>
<li><p>Der angegebene Systemparameter gilt nur pro Instanz, und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur auf Windows XP und Windows Server 2003 geschehen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann nur von <strong>JetSetSystemParameter zurückgegeben werden,</strong> wenn Systemparameter festgelegt werden, die Dateisystempfade darstellen. Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> Fehler zurückgeben.</p></td>
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
<td><p>Das Instanzhandy ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</p>
<p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p>
<p><strong>Windows Vista:</strong>  Dieser Fehler wird nur von Windows Vista und späteren Versionen zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die Einstellung für den Systemparameter auf den angegebenen Wert festgelegt.

Bei einem Fehler bleibt die Einstellung für den Systemparameter unverändert.

#### <a name="remarks"></a>Hinweise

**JetSetSystemParameter** führt eine schlechte Validierung der ausgewählten Einstellung für jeden Systemparameter durch. Es muss darauf achten, dass sie sich nicht auf diese Überprüfung verlassen, um gute Einstellungen zu erzwingen. Achten Sie besonders auf die Beschreibung der einzelnen Systemparameter, und befolgen Sie diese Richtlinien, um eine gute Systemparametereinstellung zu erhalten.

Es gibt eine Reihe von Systemparametern, die immer festgelegt werden sollten, um zu gewährleisten, dass die Datenbank-Engine wie vorgesehen funktioniert. Insbesondere sollten alle Systemparameter, die sich auf das physische Layout der von der Datenbank-Engine verwendeten Dateien auswirken, immer festgelegt werden. Weitere Informationen finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md).

Jeder Systemparameter hat einen Standardwert. Diese Standardwerte haben sich im Laufe der Zeit weiterentwickelt und sind recht willkürlich. Es wird dringend empfohlen, dass eine Anwendung alle Standardwerte auswertet, um sicherzustellen, dass sie geeignet sind. Wenn sie nicht geeignet sind, sollten sie von der Anwendung konfiguriert werden. Dies ist wichtig, da viele dieser Parameter die Zuverlässigkeit, Leistung und Ressourcenauslastung der Datenbank-Engine stark beeinträchtigen können.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetSetSystemParameterW</strong> (Unicode) und <strong>JetSetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
