---
description: 'Weitere Informationen finden Sie hier: JET_RETRIEVECOLUMN Struktur'
title: JET_RETRIEVECOLUMN-Struktur
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348216"
---
# <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN-Struktur

Die **JET_RETRIEVECOLUMN** Struktur enthält Eingabe-und Ausgabeparameter für [jetretrievecolumschlag](./jetretrievecolumns-function.md). Felder in der Struktur beschreiben, welche Spaltenwerte abgerufen werden sollen, wie Sie abgerufen werden und wo die Ergebnisse gespeichert werden sollen.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Member

**ColumnID**

Der Spalten Bezeichner für die abzurufende Spalte.

**pvData**

Ein Zeiger zum beginnen der Speicherung von Daten, die aus dem Spaltenwert abgerufen werden.

**cbData**

Die Größe der Zuordnung, beginnend bei **pvData**, in Bytes. Der Vorgang zum Abrufen von Spalten speichert keine weiteren Daten in **pvData** als **cbData**.

**cbactual**

Die Größe der Daten in Bytes, die durch einen Vorgang zum Abrufen einer Spalte abgerufen werden.

**grbit**

Eine Gruppe von Bits, die die Optionen für den Spalten Abruf enthalten, die NULL oder mehr der folgenden Werte enthalten.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Ruft den geänderten Wert anstelle des ursprünglichen Werts ab. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, abgerufen werden, wenn ein Datensatz eingefügt oder aktualisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Ruft nach Möglichkeit Spaltenwerte aus dem Index ab, ohne auf den Datensatz zuzugreifen. Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind. In Fällen, in denen der ursprüngliche Spaltenwert nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden als normal abgerufen, weil Sie nicht rückgängig gemacht werden. Dies ist eine Leistungs Option und sollte nur angegeben werden, wenn es wahrscheinlich ist, dass der Spaltenwert aus dem Index abgerufen werden kann. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten Index bzw. den primären Index die Datensätze selbst sind. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark ebenfalls festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Ruft Spaltenwerte aus dem Index-Lesezeichen ab und kann sich vom Indexwert unterscheiden, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex ebenfalls festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Ruft die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagsequence ab. Das Feld "itagsequence" wird häufig als Eingabe zum Abrufen von mehrwertigen Spaltenwerten aus einem Datensatz verwendet. Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Index Eintrag einer bestimmten Sequenznummer zuzuordnen und auch diese Sequenznummer abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ bitretrievenull</p></td>
<td><p>Ruft NULL-Werte für mehrwertige Spalten ab. Wenn diese Option nicht angegeben ist, werden NULL-Werte für mehrwertige Spalten automatisch übersprungen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind. Diese Option wirkt sich nur auf mehrwertige Spalten aus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</p></td>
</tr>
</tbody>
</table>


**iblongvalue**

Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md) oder [JET_coltypLongText](./jet-coltyp.md)abgerufen werden soll.

**itagsequence**

Die Sequenznummer der Werte, die in einer mehrwertigen Spalte enthalten sind. die **itagsequence** hier in der **JET_RETRIEVECOLUMN** kann 0 sein. Wenn **itagsequence** den Wert 0 hat, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben. Ein **itagsequence** -Wert von 0 kann in Aufrufen von [jetretrievecolumschlag](./jetretrievecolumn-function.md)nicht verwendet werden.

**columnidnexttaging**

Das **ColumnID** der markierten Spalte, der mehrwertigen Spalte oder der sparsespalte, wenn alle markierten Spalten abgerufen werden, indem 0 als **ColumnID** an [jetretrievecolbin](./jetretrievecolumn-function.md)übergeben wird.

**irre**

Fehlercodes und Warnungen, die beim Abrufen der Spalte zurückgegeben werden.

### <a name="requirements"></a>Anforderungen

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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumns-function.md)
