---
description: 'Weitere Informationen zu: jetcompact-Funktion'
title: Jetcompact-Funktion
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358946"
---
# <a name="jetcompact-function"></a>Jetcompact-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcompact-function"></a>Jetcompact-Funktion

Die **jetcompact** -Funktion erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird zu einem für die Verwendung optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures verpackt, die bei der Indexerstellung für die Indizes ausgewählt wurden. Auf diese Weise können komprimierte Daten so dicht wie möglich gespeichert werden. Alternativ können durch komprimierte Datenspeicher Platz für nachfolgende Daten Satz Vergrößerung oder Index Einfügungen reserviert werden.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*szdatabasesrc*

Die Quelldatenbank, die komprimiert wird.

*szdatabasedest*

Der Name, der für die komprimierte Datenbank verwendet werden soll.

*pfnstatus*

Eine Rückruffunktion, die regelmäßig über den Daten Bank Compact-Vorgang aufgerufen werden kann, um den Status zu melden.

*pconvert*

Ein Zeiger, der verwendet wird, um eine Alternative ESE-DLL festzulegen, die zum Lesen der Quelldatenbank verwendet werden kann, und um optionale Parameter für einen **jetcompact** -Vorgang bereitzustellen, der eine Datenbank von einem früheren in ein späteres Versions Format umwandelt. Diese Funktion wurde in Windows Server 2003 nicht mehr unterstützt.

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
<td><p>JET_bitCompactRepair</p></td>
<td><p>Wird verwendet, wenn die Quelldatenbank bekanntermaßen beschädigt ist. Sie ermöglicht eine ganze Reihe neuer Verhalten, die so viele Daten wie möglich aus der Quelldatenbank retten sollen. <strong>Jetcompact</strong> mit diesem Options Satz kann JET_errSuccess zurückgeben, aber nicht alle in der Quelldatenbank erstellten Daten kopieren. Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCompactStats</p></td>
<td><p>Bewirkt, dass <strong>jetcompact</strong> Statistiken für die Quelldatenbank in einer Datei namens DFRGINFO.TXT abgibt. Die Statistik enthält den Namen der einzelnen Tabellen in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> , die groß genug sind, um getrennt vom Datensatz, die Anzahl der Blattseiten des gruppierten Indexes und die Anzahl der Blattseiten für lange Werte gespeichert zu werden. Außerdem werden zusammenfassende Statistiken einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Daten Bank Komprimierung benötigten Zeit und des temporären Daten Bank Speicherplatzes ebenfalls ebenfalls gekippt.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Ein <em>pconvert</em> -Zeiger ungleich NULL wurde angegeben, aber die verwendete Version von ESE unterstützt die Convert-Funktion nicht. Diese Funktion wurde in der Windows Server 2003-Version von ESE entfernt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Die Aufruf Sitzung befindet sich innerhalb einer Transaktion. <strong>Jetcompact</strong> muss von einer Sitzung außerhalb einer Transaktion aufgerufen werden.</p></td>
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
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die Quelldatenbank in die Zieldatenbank kopiert. Die Zieldatenbank befindet sich in einem optimalen Zustand, z. b. befinden sich alle Tabellenindizes im angrenzenden logischen Speicherplatz. Jede Indexseite wird mit dem Betrag aufgefüllt, der beim ursprünglichen Erstellen der Indizes in der Quelldatenbank konfiguriert wurde. Alle Daten-und metadateneinstellungen werden mit voller Treue kopiert, es sei denn, die REPAIR-Option wurde angegeben. Wenn die REPAIR-Option angegeben wurde, wurden möglicherweise einige Daten aus der Quelldatenbank nicht kopiert.

Bei einem Fehler kann die Zieldatenbank vorhanden sein, ist aber keine vollständige Kopie der Quelldatenbank.

#### <a name="remarks"></a>Bemerkungen

Das Komprimieren einer Datenbank wird auch verwendet, um eine Datenbank von einem früheren Versions Format auf eine modernere Version zu aktualisieren. Ein optionaler Parameter ist *pconvert*, der eine-Struktur enthält, die eine Beschreibung für eine frühere Version der dll enthalten kann, die zum Lesen des Quelldaten Bank Formats verwendet werden kann. Diese Funktion wurde in Windows Server 2003 nicht mehr unterstützt. Im Anschluss an Windows Server 2003 können neue Versionen von ESE immer ältere Versionen des Daten Bank Formats lesen, sodass diese Funktion nicht benötigt wird.

Die gewünschte Datendichte nach einem Compact-Vorgang wird beim Erstellen von Tabellen und Indizes angegeben. Die Dichte muss zwischen 20% und 100% liegen. Wenn eine Datenbank in erster Linie gelesen und nicht aktualisiert wird, wird die Dichte von Anwendungen auf 100% festgelegt, um die Anzahl der e/a-Vorgänge während der Abfrage Verarbeitung zu verringern. Wenn die Daten jedoch häufig mit Vorgängen aktualisiert werden, die die Größe der mit dem Datensatz gespeicherten Daten erhöhen, oder wenn häufig neue Daten eingefügt werden, wählt die Anwendung eine niedrigere Dichte aus, sodass Updates häufig benötigte Ressourcen finden. Der Vorgang der Komprimierung der Datenbank bewirkt, dass die Datenbank idealerweise entsprechend der von der Anwendung ausgewählten Füllung angelegt wird.

Die Daten Bank Komprimierung ist ein Offline Vorgang. Sie kann nicht ausgeführt werden, während die Datenbank verwendet wird. Demzufolge erfolgt dies in der Regel im Rahmen eines Buildprozesses der Entwicklung einer Anwendung, die ein DataSet als Teil von sich selbst bereitstellt.

Die Offline Daten Bank Komprimierung berührt jedes Bit von Daten in einer Datenbank und kann als Mittel zum Überprüfen der Konsistenz einer Datenbank verwendet werden. Wenn eine Datenbank Fehler verdächtig ist, kann Sie komprimiert werden. Wenn in der Komprimierung kein Fehler gefunden wird, ist bekannt, dass sich die Datenbank in einem gültigen Zustand für ESE befindet.

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
<td><p>Implementiert als <strong>jetcompactw</strong> (Unicode) und <strong>jetcompacta</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[Jetdebug](./jetdefragment-function.md)  
[Jetstopservice](./jetstopservice-function.md)
