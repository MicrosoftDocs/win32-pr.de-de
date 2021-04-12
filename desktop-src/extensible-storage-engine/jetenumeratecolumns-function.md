---
description: 'Weitere Informationen zu: jetenreeratecolumschlag-Funktion'
title: JetEnumerateColumns-Funktion
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217053"
---
# <a name="jetenumeratecolumns-function"></a>JetEnumerateColumns-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetenumeratecolumns-function"></a>JetEnumerateColumns-Funktion

Die **jetenenumeratecolumschlag** -Funktion ruft effizient eine Gruppe von Spalten und deren Werten aus dem aktuellen Datensatz eines Cursors oder dem Kopier Puffer dieses Cursors ab. Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, *itagsequence* -Nummern und anderen Merkmalen eingeschränkt werden. Diese Spalten Abruf-API ist eindeutig, da Sie Informationen in dynamisch zugewiesener Speicher zurückgibt, die mit einem vom Benutzer bereitgestellten [rezuordnungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf abgerufen werden. Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. b. Größe und Multiplizität), die dem Aufrufer unbekannt sind. Dadurch ist es nicht mehr erforderlich, die Ermittlungs Modi [jetretrievecolumgen](./jetretrievecolumn-function.md) zu verwenden, um die Eigenschaften zu bestimmen, um einen letzten Rückruf für [jetretrievecolumschlag](./jetretrievecolumn-function.md) einzurichten, mit dem die gewünschten Daten erfolgreich abgerufen werden.

**Windows XP: jetenreeratecolumschlag** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*cenum ColumnID*

Ein Array von Spalten-IDs, von denen jedes ein optionales Array von *itagsequence* -Zahlen auflistet.

Wenn *cenumcolumnid* gleich 0 (null) ist, wird *rgenumcolumnid* ignoriert, und alle Spaltenwerte werden aufgezählt und an den Aufrufer zurückgegeben. Wenn ein Element des Spalten-ID-Arrays auf eine Spalten-ID von 0 (null) verweist, wird die Enumeration dieser Spalte übersprungen, und ein entsprechender Slot in der Ausgabe wird mit dem Spalten Status JET_wrnColumnSkipped generiert.

Wenn *ctagsequence* für ein angegebenes Element des Spalten-ID-Arrays 0 (null) ist, wird *rgtagsequence* ignoriert, und alle Spaltenwerte für diese Spalten-ID werden aufgezählt und an den Aufrufer zurückgegeben. Wenn ein Element eines *itagsequence* -Zahlen Arrays auf eine *itagsequence* -Nummer von 0 (null) verweist, wird die Enumeration dieser *itagsequence* -Nummer ausgelassen, und ein entsprechender Slot in der Ausgabe wird mit dem Spaltenwert Status JET_wrnColumnSkipped generiert.

*rgenum ColumnID*

Siehe *cenum ColumnID*.

*pcenumcolumn*

Gibt das aufgelistete Array von Spalten und deren Werten im Arbeitsspeicher zurück, die über den bereitgestellten *itagsequence* -kompatiblen Rückruf zugeordnet wurden.

Wenn bei der Eingabe ein Array von Spalten-IDs angefordert wird, entsprechen die Reihenfolge und Größe des Ausgabe Arrays der Reihenfolge und Größe des Eingabe Arrays. Wenn ein Array von *itagsequence* -Nummern für eine bestimmte Spalten-ID bei der Eingabe angefordert wird, entsprechen die Reihenfolge und Größe des Ausgabe Arrays der Spaltenwerte für diese Spalte der Reihenfolge und Größe des Eingabe Arrays.

Die Ausgabeparameter werden bei jedem Fehler auf 0 (null) und **null** festgelegt, ausgenommen JET_errBadColumnId und JET_errColumnNotFound. Wenn diese Fehler zurückgegeben werden, sind die Ausgabedaten gültig und für alle außer den betroffenen Spalten-IDs vollständig. Der Statuscode für jede der betroffenen Spalten-IDs wird auf einen der folgenden Fehler festgelegt, damit der Aufrufer ermitteln kann, welche Spalten-IDs schlecht waren, und möglicherweise Korrekturmaßnahmen ergreifen.

*prgenencolumn*

Siehe *pcenumcolumn*.

*pfnrezuweisung*

Identifiziert einen [erneut zuordnenden](/cpp/c-runtime-library/reference/realloc?view=vs-2019) kompatiblen Rückruf und einen optionalen Kontext Zeiger, der zum Zuordnen von Arbeitsspeicher für das Ausgabe Array von Spalten und deren Werten verwendet wird.

*pvrezuccontext*

Weitere Informationen finden Sie unter *pfnrezuweisung*.

*cbdatamost*

Legt eine Obergrenze für die Menge der Daten fest, die von einer Long-Text-oder Long Binary-Spalte zurückgegeben wird.

Dieser Parameter kann verwendet werden, um die Enumeration eines extrem großen Spaltenwerts zu verhindern. Normalerweise kann eine solche Enumeration beim API-Befehl mit JET_errOutOfMemory fehlschlagen. Wenn ein großer Spaltenwert auf diese Weise abgeschnitten wird, wird der Status des Spaltenwerts JET_wrnColumnTruncated.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitEnumerateCompressOutput</p></td>
<td><p>Beim Aufzählen von Spaltenwerten können alle Spalten, für die wir alle Werte abrufen und nur einen nicht-NULL-Spaltenwert aufweisen, in einem komprimierten Format zurückgegeben werden. Der Status dieser Spalten wird auf JET_wrnColumnSingleValue festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur zurückgegeben. Es ist nicht sichergestellt, dass alle berechtigten Spalten auf diese Weise komprimiert werden. Weitere Informationen finden Sie unter <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateCopy</p></td>
<td><p>Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes anstelle der ursprünglichen Spaltenwerte aufgezählt werden sollen. Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufgelistet. Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufgezählt werden.</p>
<p>Diese Option ist mit JET_bitRetrieveCopy identisch, wenn Sie mit <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a> oder <a href="gg294135(v=exchg.10).md">jetretrievecolumschlag</a>verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateIgnoreDefault</p></td>
<td><p>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben. Normalerweise würde der Standardwert für die Spalte, sofern vorhanden, in diesem Fall zurückgegeben werden. Wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, wird ein anderer Wert zurückgegeben (d. h., wenn eine Spalte mit einem Standardwert explizit auf <strong>null</strong> festgelegt ist, wird ein <strong>null</strong> -Wert als Wert für diese Spalte zurückgegeben). Beachten Sie, dass auch dann, wenn diese Option angefordert wird, immer noch ein Spaltenwert angezeigt wird, der dem Standardwert entspricht. Es wird nicht versucht, Spaltenwerte zu entfernen, die ihren Standardwerten entsprechen.</p>
<p>Beachten Sie, dass sich diese Option auf die Ausgabe von <strong>jetenreeratecolumschlag</strong> auswirkt, wenn Sie mit JET_bitEnumeratePresenceOnly oder JET_bitEnumerateTaggedOnly verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateIgnoreUserDefinedDefault</p></td>
<td><p>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben. Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</p>
<p><strong>Windows Server 2003 und früher:  </strong> Für Windows Server 2003 und frühere Versionen schlägt der Vorgang mit JET_errCallbackFailed fehl.</p>
<p><strong>Windows Server 2003 SP1:  </strong> Dieser mögliche Wert ist nur für Windows Server 2003 SP1 und spätere Betriebssysteme verfügbar. Wenn dieser mögliche Wert angegeben wird und die Tabelle eine Spalte mit einem benutzerdefinierten Standardwert enthält, schlägt der Vorgang mit JET_errCallbackFailed fehl.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumeratePresenceOnly</p></td>
<td><p>Wenn ein nicht-NULL-Wert für den angeforderten Spalten-oder Spaltenwert vorhanden ist, werden die zugehörigen Daten nicht zurückgegeben. Stattdessen wird der zugehörige Status für diesen Spalten-oder Spaltenwert auf JET_wrnColumnPresent festgelegt. Wenn der Spalten-oder Spaltenwert <strong>null</strong> ist, werden JET_wrnColumnNull wie gewohnt zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateTaggedOnly</p></td>
<td><p>Wenn Sie alle Spaltenwerte im Datensatz auflisten (z. b. Wenn <em>cenumcolumnid</em> NULL ist), werden nur markierte Spaltenwerte zurückgegeben. Diese Option ist beim Auflisten eines bestimmten Arrays von Spalten-IDs nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateInRecordOnly</p></td>
<td><p><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBadColumnId</p></td>
<td><p>Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID. Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn bestimmte Spalten-IDs angefordert wurden, eine dieser Spalten-IDs ungültig war und die erste ungültige Spalten-ID mit diesem Fehler für den zugehörigen Spalten Statuscode fehlgeschlagen ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die von der angegebenen Spalten-ID beschriebene Spalte ist in der Tabelle nicht vorhanden. Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn bestimmte Spalten-IDs angefordert wurden, eine dieser Spalten-IDs ungültig war und die erste ungültige Spalten-ID mit diesem Fehler für den zugehörigen Spalten Statuscode fehlgeschlagen ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:  </strong> Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn Folgendes gilt:</p>
<ul>
<li><p>JET_bitEnumerateLocal wird angegeben.</p></li>
<li><p>Es wurde ein ungültiges <em>grbit</em> angegeben.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dieser Fehler wird von <strong>jetenreeratecolumschlag</strong> zurückgegeben, wenn Folgendes gilt:</p>
<ul>
<li><p><em>pcenumcolumn</em> ist <strong>null</strong>.</p></li>
<li><p><em>prgenencolumn</em> ist <strong>null</strong>.</p></li>
<li><p><em>pfnrezuweisung</em> ist <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor ist nicht in einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Der Cursor wird auf einem Datensatz positioniert, der gelöscht wurde. Dafür sind viele verschiedene Gründe möglich. Der häufigste Grund ist, dass sich die Sitzung nicht in einer Transaktion befindet, der Cursor auf einem Datensatz positioniert wurde, dass der Datensatz gelöscht wurde und der Cursor dann versucht hat, auf diesen Datensatz zu verweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:  </strong> Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden die angeforderten Daten in den Ausgabe Puffern zurückgegeben. Es ist Aufgabe des Aufrufers, den von diesem Rückruf zugeordneten Arbeitsspeicher freizugeben und in den Ausgabe Puffern zurückzugeben. Dieser Speicher sollte durch den bereitgestellten [rezuordnungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf freigegeben werden. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler wird keine der angeforderten Daten zurückgegeben. Arbeitsspeicher, der während des Aufrufs zugewiesen wurde, wird automatisch mit dem bereitgestellten [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf freigegeben. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Wenn Sie alle Spaltenwerte im Datensatz auflisten und JET_bitEnumerateIgnoreDefaults nicht angegeben haben, können Sie nicht davon ausgehen, dass Ihnen nie ein Spalten-oder Spaltenwert mit dem Statuscode JET_wrnColumnNull angezeigt wird. Dieser Statuscode kann angezeigt werden, wenn eine Spalte einen Standardwert hat und explizit auf **null** festgelegt wurde oder wenn die Spalte eine nicht-sparsespalte ist (z. b. eine Spalte mit fester oder variabler Größe).

Der *cbdatamost* -Parameter gilt nicht für alle Spaltenwerte. Mit diesem Parameter werden nur lange Text-und lange binäre Spaltenwerte gekürzt, die so groß sind, dass Sie separat vom Datensatz gespeichert wurden.

Wenn **jetentoeratecolumschlag** Daten in den Ausgabeparametern zurückgibt, ist der Aufrufer für die Freigabe des Arbeitsspeichers im Array sowie für jeden Speicher verantwortlich, auf den in diesem Array eingebettete Zeiger verwiesen wird.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumns-function.md)
