---
description: 'Weitere Informationen finden Sie unter: jetprereadindexranges-Funktion'
title: Jetprereadindexranges-Funktion
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128164"
---
# <a name="jetprereadindexranges-function"></a>Jetprereadindexranges-Funktion


_**Gilt für:** Windows | Windows Server_

Die **jetprereadindexranges** -Funktion erhöht Indizes, um die Leistung zu verbessern.

Die **jetprereadindexranges** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, für die die prereads ausgestellt werden sollen.

*rgindexranges*

Die Schlüsselbereiche für die Voraussetzungen.

*cindexbereiche*

Die Anzahl der Schlüsselbereiche, die durch die Anzahl der Elemente in *rgindexranges* festgelegt werden sollen.

*pcrangespreread*

Die Anzahl der Schlüsselbereiche, die tatsächlich vorab registriert wurden.

*rgcolumnidpreread*

Liste der Spalten-IDs für lange Wert Spalten, die vorab registriert werden sollen. Standardmäßig ist nur der On-Page-Datensatz Preread. Wenn die Spalten außerhalb der Seiten langen Werte vorausgesetzt werden müssen, müssen ihre Spalten-IDs über diesen Parameter übergeben werden.

*ccolumnidpreread*

Die Anzahl der Spalten-IDs für die Voraussetzungen für lange Wert Spalten, die durch die Anzahl der Elemente in *rgcolumnidpreread* bestimmt werden.

*grbit*

Eine Gruppe von Bits, die 0 (null) oder mehr der in der folgenden Tabelle aufgeführten Werte der Preread-Richtung angibt.

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
<td><p>Weiter</p></td>
<td><p>Preread Forward.</p></td>
</tr>
<tr class="even">
<td><p>Rückwärts</p></td>
<td><p>Vorab lesen.</p></td>
</tr>
<tr class="odd">
<td><p>Firstpageonly</p></td>
<td><p>Nur die erste Seite einer langen Spalte wird vorab registriert.</p></td>
</tr>
<tr class="even">
<td><p>Normalizedkey</p></td>
<td><p>Normalisierter Schlüssel/Lesezeichen anstelle von Spaltenwert angegeben.</p></td>
</tr>
</tbody>
</table>


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
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffer Cache befinden, sollten Sie asynchrone Lesevorgänge starten, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.

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

[JET_ERR](./jet-err.md)
