---
description: ICE59 überprüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die vom Zielfeature der Verknüpfung installiert werden.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1a8d6318a9b4525941edd3873c9fc35bd11f488e42c8a82da71c4b2c0b9b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044020"
---
# <a name="ice59"></a>ICE59

ICE59 überprüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die vom Zielfeature der Verknüpfung installiert werden.

Von ICE59 gemeldete Fehler führen im Allgemeinen zu folgendem Verhalten:

1.  Die angekündigte Verknüpfung startet den Windows Installer, um das in der Spalte Ziel aufgeführte Feature zu installieren.
2.  Da die [FeatureComponents-Tabelle](featurecomponents-table.md) das Zielfeature jedoch nicht der Komponente zuteilt, die die Verknüpfung enthält, wird die Keyfile der Komponente (die durch die Verknüpfung aktiviert wird) nicht installiert.
3.  Daher ist die Verknüpfung unterbrochen und macht nichts.

## <a name="result"></a>Ergebnis

ICE59 gibt einen Fehler aus, wenn eine angekündigte Verknüpfung nicht zu den Komponenten gehört, die von der Zielfunktion der Verknüpfung installiert werden.

## <a name="example"></a>Beispiel

ICE59 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

In diesem Fall gibt ShortcutB FeatureA an und startet bei Aktivierung die Schlüsseldatei von ComponentB. ComponentB wird jedoch nie von FeatureA installiert, sodass das Ziel der Verknüpfung auch nach Abschluss der Bedarfsinstallationsphase nicht vorhanden ist.

Um diesen Fehler zu beheben, fügen Sie der [Tabelle FeatureComponents](featurecomponents-table.md) eine Zeile hinzu, die FeatureA und ComponentB zuteilt.

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Ziel   | Komponente\_ |
|-----------|----------|-------------|
| ShortcutB | FeatureA | ComponentB  |



 

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Komponente\_ | Komponente\_ |
|-----------|-------------|
| FeatureA  | ComponentA  |



 

[Featuretabelle](feature-table.md) (partiell)



| Komponente  | Ebene |
|----------|-------|
| FeatureA | 10    |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente  | KeyPath |
|------------|---------|
| ComponentA | Filea   |
| ComponentB | Fileb   |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ | Sequenz |
|-------|-------------|----------|
| Filea | ComponentA  | 1        |
| Fileb | ComponentB  | 2        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



