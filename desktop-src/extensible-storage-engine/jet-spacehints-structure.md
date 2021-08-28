---
description: 'Weitere Informationen finden Sie unter: JET_SPACEHINTS Struktur'
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
ms.openlocfilehash: 812fc683e24e6b2401ce72d99e3537549e3d30d0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985143"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS Struktur

Die **JET_SPACEHINTS** enthält Informationen zu Speicherbelegungsmustern, wenn eine B-Struktur durch Anfüge- oder Hotpointaufteilungen wächst. Anfügeteilungen werden ausgeführt, wenn Datensätze am Ende einer B-Struktur hinzugefügt werden und Hotpointteilungen ausgeführt werden, wenn der gleichen virtuellen Einfügemarke mehrere Datensätze hinzugefügt werden (z. B. hinzufügen von "Sollen", "Mark", "Martin", "Mary" zur Mitte einer alphabetisch sortierten B-Struktur).

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

Die Dichte am Layout (Anfügen).

**cbInitial**

Die Anfangsgröße (in Bytes) des objekts, das erstellt wird. Dies muss ein Vielfaches der Datenbankseitengröße sein.

**grbit**

Eine Gruppe von Bits, die die Optionen enthalten, die für diese Struktur verwendet werden sollen, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>Ändert die interne Zuordnungsrichtlinie, um platzsymlogisch vom unmittelbar übergeordneten Element einer B-Struktur zu erhalten.</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>Ermöglicht das Anfügeteilungsverhalten entsprechend der Wachstums dynamics der Tabelle (festgelegt durch cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>Ermöglicht, dass das Hotpoint-Teilungsverhalten entsprechend der Wachstums dynamics der Tabelle (festgelegt durch cbMinExtent, ulGrowth, cbMaxExtent) wächst.</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>Wenn festgelegt, gibt der Client an, dass die sequenzielle Vorwärtsprüfung das vorherrschende Verwendungsmuster dieser Tabelle ist.</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>Wenn festgelegt, gibt der Client an, dass die sequenzielle Abwärtsprüfung das vorherrschende Verwendungsmuster dieser Tabelle ist.</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>Wenn festgelegt, erwartet die Anwendung, dass diese Tabelle in sequenzieller Reihenfolge bereinigt wird , vom niedrigsten Schlüssel zum höchsten Schlüssel.</p> | 



**ulMaintDensity**

Density to mulMaintDensity

Dichte, bei der verwaltet werden soll. Wenn die Leerzeichen JET_bitRetrieveHintTableScanForward oder JET_bitRetrieveHintTableScanBackward angeben, wird die Tabellendefragmentierung ausgelöst, wenn der verwendete Speicherplatz in der Tabelle unter diesen Schwellenwert fällt. Die Tabellendefragmentierung kann deaktiviert werden, indem dieser Member auf 0 (null) gesetzt wird. Wenn Sie diesen Member auf 100 festlegen, wird die Tabellendefragmentierung ausgeführt, sobald eine Seite frei wird.

**ulGrowth**

Das Prozentwachstum vom letzten Wachstum oder der anfänglichen Größe, gerundet auf die nächste native JET-Zuordnungsgröße.

**cbMinExtent zu klein**

Dadurch wird ulGrowth überschrieben, wenn es zu klein ist.

**cbMaxExtent**

Der maximale Wert für das Wachstum in Bytes. Dies ist die Obergrenze von ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Wenn eine B-Struktur durch Anfüge- oder Hotpointteilungen wächst (im Gegensatz zu zufälligen Datensatzeinfügungen), wird der Speicherplatz, um den die Tabelle wächst, wie folgt berechnet:

1.  Bei der Erstellung geben wir die b-Struktur cbInitial immer an.

2.  Bei der ersten Zuordnung eines bestimmten Bereichs weisen wir zu: cbInitial ulGrowth / 100 (gerundet auf die Seitengröße der Datenbank) oder \* cbMinExtent, falls größer.

3.  Bei der nächsten Zuordnung cbLastAlloc ulGrowth /100 (gerundet auf die Seitengröße der Datenbank) oder \* cbMinExtent, falls größer.

4.  Bei einigen Zuordnungen (dies kann die erste Zuordnung sein) überschreitet die berechnete Größe cbMaxExtent, und dies ist die größe danach.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
