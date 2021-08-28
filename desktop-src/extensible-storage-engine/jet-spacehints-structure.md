---
description: 'Weitere Informationen zu: JET_SPACEHINTS-Struktur'
title: JET_SPACEHINTS-Struktur
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
ms.openlocfilehash: 77c452fb78916fdcdf935ec6ad890db055e63b9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479316"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS-Struktur

Die **JET_SPACEHINTS-Struktur** enthält Informationen zu Raumzuordnungsmustern, wenn eine B-Struktur durch Anfüge- oder Hotpointteilungen wächst. Anfügeteilungen treten auf, wenn Datensätze am Ende einer B-Struktur hinzugefügt werden und Hotpointteilungen auftreten, wenn mehrere Datensätze derselben virtuellen Einfügemarke hinzugefügt werden (z. B. hinzufügen von 'Soll', 'Mark', 'Martin', 'Mary' in der Mitte einer alphabetisch sortierten B-Struktur).

**Windows 7:** Die **JET_SPACEHINTS-Struktur** wird in Windows 7 eingeführt.

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

Die Größe (in Bytes) dieser Struktur. Legen Sie diesen Member auf sizeof( JET_SPACEHINTS ) fest.

**ulInitialDensity**

Die Dichte am Layout (anfügen).

**cbInitial**

Die Anfangsgröße (in Bytes) des zu erstellenden Objekts. Dies muss ein Vielfaches der Datenbankseitengröße sein.

**grbit**

Eine Gruppe von Bits, die die für diese Struktur zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>Ändert die interne Zuordnungsrichtlinie, um Speicherplatz vom unmittelbar übergeordneten Element einer B-Struktur zu erhalten.</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>Aktiviert das Anfügeteilungsverhalten, um entsprechend der Wachstums dynamics der Tabelle zu wachsen (festgelegt durch cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>Ermöglicht das Aufteilen von Hotpoints entsprechend der Wachstums dynamics der Tabelle (festgelegt durch cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>Wenn diese Einstellung festgelegt ist, gibt der Client an, dass der sequenzielle Vorwärtsscan das vorherrschende Verwendungsmuster dieser Tabelle ist.</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>Wenn diese Einstellung festgelegt ist, gibt der Client an, dass der sequenzielle Rückwärtsscan das vorherrschende Verwendungsmuster dieser Tabelle ist.</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>Wenn diese Einstellung festgelegt ist, erwartet die Anwendung, dass diese Tabelle sequenziell bereinigt wird , vom niedrigsten schlüssel zum höchsten Schlüssel.</p> | 



**ulMaintDensity**

density to mulMaintDensity

Dichte, die beibehalten werden soll. Wenn die Leerzeichen JET_bitRetrieveHintTableScanForward oder JET_bitRetrieveHintTableScanBackward angeben, wird die Tabellendefragmentierung ausgelöst, wenn der verwendete Speicherplatz in der Tabelle unter diesen Schwellenwert fällt. Die Tabellendefragmentierung kann deaktiviert werden, indem dieser Member auf 0 (null) festgelegt wird. Wenn Sie diesen Member auf 100 festlegen, wird die Defragmentierung der Tabelle ausgeführt, sobald eine Seite freigegeben wird.

**ulGrowth**

Das prozentuale Wachstum von der letzten Vergrößerung oder Anfangsgröße, gerundet auf die nächste native JET-Zuordnungsgröße.

**cbMinExtent zu klein**

Dies überschreibt ulGrowth, wenn es zu klein ist.

**cbMaxExtent**

Der maximale Wert für die Vergrößerung in Bytes. Dies kapselt ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Wenn eine B-Struktur durch Anfüge- oder Hotpointteilungen wächst (im Gegensatz zu zufälligen Datensatzeinfügungen), wird der Speicherplatz, um den die Tabelle vergrößert wird, wie folgt berechnet:

1.  Bei der Erstellung wird die b-struktur cbInitial immer vergeben.

2.  Während der ersten Zuordnung eines bestimmten Bereichs weisen wir Folgendes zu: cbInitial \* ulGrowth / 100 (gerundet auf die Seitengröße der Datenbank) oder cbMinExtent, falls größer.

3.  Während der nächsten Zuordnung wird cbLastAlloc \* ulGrowth/100 (gerundet auf die Seitengröße der Datenbank) oder cbMinExtent ( falls größer) angezeigt.

4.  Bei einer Zuordnung (die die erste Zuordnung sein kann) überschreitet die berechnete Größe cbMaxExtent, und dies ist die Vergrößerungsgröße danach.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
