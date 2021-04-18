---
description: ICE59 prüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die von der Zielfunktion der Verknüpfung installiert werden.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343847"
---
# <a name="ice59"></a>ICE59

ICE59 prüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die von der Zielfunktion der Verknüpfung installiert werden.

Von ICE59 gemeldete Fehler führen in der Regel zu folgendem Verhalten:

1.  Die angekündigte Verknüpfung startet die Windows Installer, um das in der Ziel Spalte aufgelistete Feature zu installieren.
2.  Da die [FeatureComponents-Tabelle](featurecomponents-table.md) die Zielfunktion jedoch nicht der Komponente zuordnet, die die Verknüpfung enthält, wird die keyfile der Komponente (die durch die Verknüpfung aktiviert ist) nicht installiert.
3.  Daher ist die Verknüpfung beschädigt und führt keine Aktion aus.

## <a name="result"></a>Ergebnis

ICE59 gibt einen Fehler aus, wenn eine angekündigte Verknüpfung nicht zu den Komponenten gehört, die von der Zielfunktion der Verknüpfung installiert werden.

## <a name="example"></a>Beispiel

ICE59 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

In diesem Fall gibt shortcutb "FeatureA" an und startet bei Aktivierung die Schlüsseldatei von "componentb". Obwohl componentb noch nie von FeatureA installiert wird, ist das Ziel der Verknüpfung nicht vorhanden, auch wenn die Installations-on-Demand-Phase abgeschlossen ist.

Um diesen Fehler zu beheben, fügen Sie der [FeatureComponents-Tabelle](featurecomponents-table.md) eine Zeile hinzu, in der Featurekomponenten und componentb verknüpft sind.

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Ziel   | Komponente\_ |
|-----------|----------|-------------|
| Shortcutb | FeatureA | Componentb  |



 

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Funktion\_ | Komponente\_ |
|-----------|-------------|
| FeatureA  | Componenta  |



 

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion  | Ebene |
|----------|-------|
| FeatureA | 10    |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | KEYPATH |
|------------|---------|
| Componenta | Mit der   |
| Componentb | FileB   |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ | Sequenz |
|-------|-------------|----------|
| Mit der | Componenta  | 1        |
| FileB | Componentb  | 2        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



