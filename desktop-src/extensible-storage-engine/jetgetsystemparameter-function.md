---
description: 'Weitere Informationen: jetgetsystemparameter-Funktion'
title: Jetgetsystemparameter-Funktion
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
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217852"
---
# <a name="jetgetsystemparameter-function"></a>Jetgetsystemparameter-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetsystemparameter-function"></a>Jetgetsystemparameter-Funktion

Die **jetgetsystemparameter** -Funktion liest die zahlreichen Konfigurationseinstellungen der Datenbank-Engine.

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

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **null** sein.

Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen. Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird. In beiden Fällen werden alle Systemparameter Einstellungen aus dieser eine Instanz gelesen. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, kann dieser Parameter **null** sein, oder es handelt sich um einen Zeiger auf eine Instanz, die mit [jetinit](./jetinit-function.md) oder [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde. Wenn dieser Parameter **null** ist, wird die Parametereinstellung des globalen Systems (oder der Standardwert) gelesen. Wenn dieser Parameter eine Instanz ist, wird die Systemparameter Einstellung für diese Instanz gelesen.

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.

*paramid*

Die ID des System Parameters, der gelesen wird.

Eine komplette Liste der Systemparameter und deren Eigenschaften finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md) .

*plparam*

Der Ausgabepuffer, der den Wert des ausgewählten System Parameters empfängt, wenn dieser Systemparameter einen ganzzahligen Typ hat.

*szparam*

Der Ausgabepuffer, der den Wert des ausgewählten System Parameters empfängt, wenn dieser Systemparameter vom Typ String ist.

*cbmax*

Die maximale Größe des Zeichen folgen-Ausgabepuffers in Bytes.

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
<td><p>JET_errInitInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</p>
<p>Dies kann für <strong>jetgetsystemparameter</strong> auftreten, wenn:</p>
<ul>
<li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li>
<li><p>Der angegebene Systemparameter erfordert, dass der ganzzahlige Ausgabepuffer bereitgestellt wird und dass der Ausgabepuffer Zeiger <strong>null</strong>war.</p></li>
<li><p>Der angegebene Systemparameter erfordert, dass ein Zeichen folgen-Ausgabepuffer angegeben wird und dass der Ausgabepuffer Zeiger <strong>null</strong>war.</p>
<p><strong>Windows Vista:  </strong> Dies kann nur in Windows Vista und höheren Versionen vorkommen.</p></li>
<li><p>Der angegebene Systemparameter erfordert, dass ein Zeichen folgen-Ausgabepuffer angegeben wird, und die Größe dieses Ausgabepuffers ist zu klein, um eine NULL-terminierte Zeichenfolge zu akzeptieren.</p>
<p><strong>Windows Vista:  </strong> Dies kann nur in Windows Vista und höheren Versionen vorkommen.</p></li>
<li><p>Der angegebene Systemparameter kann nicht gelesen werden, da er schreibgeschützt ist.</p></li>
<li><p>Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter zu lesen. Dies kann nur unter Windows XP und höheren Versionen vorkommen.</p></li>
<li><p>Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter zu lesen. Dies kann nur unter Windows XP und höheren Versionen vorkommen.</p></li>
</ul></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung. Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance</p></td>
<td><p>Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde. Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p>
<p><strong>Windows Vista:  </strong> Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um die gesamte Systemparameter Einstellung zu erhalten.</p>
<p>Der Ausgabepuffer wurde mit dem Umfang der Systemparameter Einstellung aufgefüllt, wie er passt. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer Null beendet.</p>
<p><strong>Hinweis  </strong> Dieser Fehler wird nicht von allen Releases zurückgegeben. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil der Ausgabepuffer zu klein war, um die gesamte Systemparameter Einstellung zu erhalten.</p>
<p><strong>Hinweis  </strong> Dieser Fehler wird in einigen Fällen nicht zurückgegeben, um die Anwendungs Kompatibilität zu erhalten. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p>
<p><strong>Windows Vista:  </strong> Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der für den angeforderten Systemparameter geeignete Ausgabepuffer auf den Wert dieses System Parameters festgelegt.

Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.

#### <a name="remarks"></a>Bemerkungen

In dieser API gibt es ein wichtiges Problem, das in allen Releases vorhanden ist. Wenn ein Systemparameter mit einem Zeichen folgen Wert angefordert wird und der Ausgabepuffer zu klein ist, um die gesamte Systemparameter Einstellung zu erhalten, werden keine JET_wrnBufferTruncated zurückgegeben. Stattdessen wird JET_errSuccess zurückgegeben. Wenn die Länge der zurückgegebenen Zeichenfolge der Größe des Ausgabepuffers abzüglich des **null** -Terminator entspricht, sollte der Aufrufer so reagieren, als ob JET_wrnBufferTruncated zurückgegeben würden. Wenn ein Ausgabepuffer der Größe 0 (null) angegeben wird, sollte der Aufrufer so reagieren, als ob JET_errInvalidParameter zurückgegeben werden.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetgetsystemparameterw</strong> (Unicode) und <strong>jetgetsystemparametera</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
