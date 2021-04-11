---
description: 'Weitere Informationen zu: jetsetsystemparameter-Funktion'
title: Jetsetsystemparameter-Funktion
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
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214754"
---
# <a name="jetsetsystemparameter-function"></a>Jetsetsystemparameter-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>Jetsetsystemparameter-Funktion

Die **jetsetsystemparameter** -Funktion wird verwendet, um die zahlreichen Konfigurationseinstellungen der Datenbank-Engine festzulegen.

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

*pinstance*

Gibt die-Instanz an, die für diesen Befehl verwendet werden soll.

**Windows 2000:**  Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **null** sein.

**Windows XP:**  Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen. Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird. In beiden Fällen werden alle Systemparameter Einstellungen aus dieser eine Instanz gelesen. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, kann dieser Parameter **null** sein, oder es handelt sich um einen Zeiger auf eine Instanz, die mit [jetinit](./jetinit-function.md) oder [jetkreateindex](./jetcreateindex-function.md)erstellt wurde. Wenn dieser Parameter **null** ist, wird die Parametereinstellung des globalen Systems (oder der Standardwert) gelesen. Wenn dieser Parameter eine Instanz ist, wird die Systemparameter Einstellung für diese Instanz gelesen.

Obwohl es sich technisch gesehen um einen out-Parameter handelt, ändert diese API niemals den Inhalt des bereitgestellten Puffers.

*-sid*

Gibt die Sitzung an, die für diesen-Befehl verwendet werden soll.

Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.

*paramid*

Die ID des System Parameters, der festgelegt wird. Eine komplette Liste der Systemparameter und deren Eigenschaften finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md) .

*lParam*

Gibt den Wert an, der für den ausgewählten Systemparameter festgelegt werden soll, wenn der Systemparameter einen ganzzahligen Typ hat.

*szparam*

Gibt den Wert für den ausgewählten Systemparameter an, wenn dieser Systemparameter vom Typ String ist.

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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p>
<p><strong>Windows Vista:</strong>  Unter Windows Vista und höheren Versionen kann Erfolg zurückgegeben werden, ohne dass der Wert des System Parameters geändert werden muss. Weitere Informationen finden Sie im Abschnitt "JET_paramEnableAdvanced System" im Thema " <a href="gg269346(v=exchg.10).md">Meta para</a> meters".</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Die Instanz wurde mithilfe eines <a href="gg294068(v=exchg.10).md">jetinit-Aufrufes</a> initialisiert, und dieser Vorgang kann nicht als Ergebnis ausgeführt werden. Dies kann bei einem <strong>jetsetsystemparameter</strong> vorkommen, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Werts den Status der Datenbank-Engine nicht beeinträchtigt hat.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Die angegebenen tupelindexparameter waren unzulässig. Dieser Fehler kann von <strong>jetsetsystemparameter</strong> nur zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> auf einen ungültigen Wert festgelegt wird.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetsetsystemparameter</strong> vorkommen, wenn:</p>
<ul>
<li><p>Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einer Zeichenfolge festzulegen, deren Länge außerhalb des gültigen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einem Dateipfad festzulegen, bei dem die Länge der absoluten Pfad Darstellung außerhalb des gültigen Bereichs für diesen Parameter liegt.</p>
<p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und höheren Versionen vorkommen.</p></li>
<li><p>Es wurde versucht, einen ganzzahligen Wert mit einem ganzzahligen Wert festzulegen, der außerhalb des gültigen Bereichs für den Parameter liegt.</p></li>
<li><p>Es wurde versucht, JET_paramUnicodeIndexDefault mit einem NULL- <strong></strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Zeiger, einer ungültigen LCID oder einem nicht unterstützten Satz von LCMapString-Flags festzulegen.</p>
<p><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und höheren Versionen vorkommen.</p></li>
<li><p>Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</p></li>
<li><p>Es wurde versucht, einen Systemparameter festzulegen, nachdem <a href="gg294068(v=exchg.10).md">jetinit</a> aufgerufen wurde, die Datenbank-Engine befindet sich im Einzel Instanz-Modus, und es wurde keine Sitzung angegeben.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</p></li>
<li><p>Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</p></li>
<li><p>Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</p>
<p><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann von <strong>jetsetsystemparameter</strong> nur zurückgegeben werden, wenn Systemparameter festgelegt werden, die Dateisystem Pfade darstellen. Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> diesen Fehler zurückgeben.</p></td>
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
<p>Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p>
<p><strong>Windows Vista:</strong>  Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die Einstellung für den Systemparameter auf den angegebenen Wert festgelegt.

Bei einem Fehler bleibt die Einstellung für den Systemparameter unverändert.

#### <a name="remarks"></a>Bemerkungen

**Jetsetsystemparameter** ist ein schlechter Auftrag der Überprüfung der ausgewählten Einstellung für jeden Systemparameter. Es muss darauf geachtet werden, dass Sie sich nicht auf diese Validierung verlassen, um gute Einstellungen zu erzwingen. Achten Sie auf die Beschreibung der einzelnen Systemparameter, und befolgen Sie diese Richtlinien für eine gute Systemparameter Einstellung.

Es gibt eine Reihe von Systemparametern, die immer festgelegt werden sollten, um sicherzustellen, dass die Datenbank-Engine ordnungsgemäß funktioniert. Insbesondere sollten alle Systemparameter, die das physische Layout der von der Datenbank-Engine verwendeten Dateien beeinflussen, immer festgelegt werden. Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).

Jeder Systemparameter verfügt über einen Standardwert. Diese Standardwerte wurden im Laufe der Zeit weiterentwickelt und sind beliebig. Es wird dringend empfohlen, dass eine Anwendung alle Standardwerte auswertet, um sicherzustellen, dass Sie geeignet sind. Wenn Sie nicht geeignet sind, sollten Sie von der Anwendung konfiguriert werden. Dies ist wichtig, da viele dieser Parameter die Zuverlässigkeit, Leistung und Ressourcennutzung der Datenbank-Engine erheblich beeinträchtigen können.

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
<td><p>Implementiert als <strong>jetsetsystemparameterw</strong> (Unicode) und <strong>jetsetsystemparametera</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[Jetgetsystemparameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
