---
description: 'Weitere Informationen finden Sie hier: JET_SPACEHINTS Struktur'
title: JET_SPACEHINTS Struktur
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344398"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS Struktur

Die **JET_SPACEHINTS** Struktur enthält Informationen zu Speicherplatz Zuordnungs Mustern, wenn eine b-Struktur durch Anfüge-oder hotpointteilungen wächst. Anfüge Teilungen treten auf, wenn dem Ende einer b-Strukturdaten Sätze hinzugefügt werden und die hotpointteilungen durchgeführt werden, wenn der gleichen virtuellen Einfügemarke mehrere Datensätze hinzugefügt werden (z. b. "Marie", "Mark", "Martin", "Mary" in der Mitte einer in eine alphabetisch sortierten b-Struktur hinzufügen).

**Windows 7:** Die **JET_SPACEHINTS** Struktur wird in Windows 7 eingeführt.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) dieser Struktur. Legen Sie diesen Member auf sizeof (JET_SPACEHINTS) fest.

**ulinitialdensity**

Die Dichte beim (Anfügen) Layout.

**cbinitial**

Die Anfangs Größe (in Bytes) des Objekts, das erstellt wird. Dies muss ein Vielfaches der Seitengröße der Datenbank sein.

**grbit**

Eine Gruppe von Bits, die die für diese-Struktur zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

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
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Ändert die interne Zuordnungs Richtlinie, um Speicherplatz auf der Grundlage des unmittelbar übergeordneten Elements einer b-Struktur zu erzielen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Ermöglicht das Anfügen von Split-Verhalten entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Ermöglicht das Anwachsen des hotpointverhaltens entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Wenn dieser Wert festgelegt ist, gibt der Client an, dass der Forward-sequenzielle Scan das vorherrschende Verwendungs Muster dieser Tabelle ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Wenn festgelegt, gibt der Client an, dass die rückwärts sequenzielle Überprüfung das vorherrschende Verwendungs Muster dieser Tabelle ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Wenn festgelegt, erwartet die Anwendung, dass diese Tabelle in sequenzieller Reihenfolge vom niedrigsten zum höchsten Schlüssel bereinigt wird.</p></td>
</tr>
</tbody>
</table>


**ulmaintdensity**

Dichte für mehrmaintdensity

Die zu verwaltende Dichte. Wenn die Speicherplatz Hinweise JET_bitRetrieveHintTableScanForward oder JET_bitRetrieveHintTableScanBackward angeben, wird die Tabellen Defragmentierung ausgelöst, wenn der verwendete Speicherplatz in der Tabelle unter diesen Schwellenwert fällt. Die Tabellen Defragmentierung kann deaktiviert werden, indem dieser Member auf NULL festgelegt wird. Wenn dieser Member auf 100 festgelegt wird, wird die Tabellen Defragmentierung ausgeführt, sobald eine Seite freigegeben wird.

**ulgrowth**

Das prozentuale Wachstum von der letzten Vergrößerung oder anfangs Größe auf die nächste Native Jet-Zuordnungs Größe gerundet.

**cbminblock zu klein**

Dies überschreibt ulgrowth, wenn zu klein.

**cbmaxblock**

Der maximale Wert für das Wachstum in Bytes. Dies begrenzt ulgrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Wenn eine b-Struktur durch Anfüge-oder hotpointteilungen wächst (im Gegensatz zu zufälligen Daten Satz Einfügungen), wird der von der Tabelle generierte Speicherplatz wie folgt berechnet:

1.  Bei der Erstellung wird der b-Struktur cbinitial, immer, übergeben.

2.  Während der ersten Zuordnung eines bestimmten Bereichs belegen wir Folgendes: cbinitial \* ulgrowth/100 (gerundet auf die Seitengröße der Datenbank) oder cbminblock, wenn größer.

3.  Bei der nächsten Zuordnung wird cblastalloc \* ulgrowth/100 (auf die Seitengröße der DB gerundet) oder cbminblock, wenn größer.

4.  Bei einer Zuordnungs Zuweisung (bei der es sich um die erste Zuordnung handeln kann), überschreitet die berechnete Größe den cbmaxblock, und dies ist die Vergrößerung.

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

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
