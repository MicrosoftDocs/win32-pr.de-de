---
description: ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zu derselben Komponente wie die Verknüpfung selbst gehört oder dass die Attribute der Zielkomponente sicherstellen, dass sie die Installationsstandorte nicht ändert.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b25f3bba6bd6efaf20b55982524840348f39e8717dc53b7699a6f5f2886df01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787390"
---
# <a name="ice67"></a>ICE67

ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zu derselben Komponente wie die Verknüpfung selbst gehört oder dass die Attribute der Zielkomponente sicherstellen, dass sie die Installationsstandorte nicht ändert.

Wenn eine von ICE67 gemeldete Warnung oder ein Fehler nicht behoben werden kann, kann die Verknüpfung ungültig sein, wenn die Zielkomponente den Zustand ändert und die Quellkomponente dies nicht tut. Wenn z. B. die Komponente der Zieldatei so festgelegt ist, dass sie aus der Quelle ausgeführt wird, führt eine Neuinstallation, die die Komponente in eine lokale Ändert, dazu, dass die Komponente, die die Verknüpfung enthält, nicht neu installiert wird. Daher zeigt die Verknüpfung auf eine ungültige Position.

Beachten Sie, dass in einigen Fällen die Verwendung einer anderen Komponente für die Verknüpfung unvermeidbar ist. Wenn die Verknüpfung beispielsweise im Benutzerprofil erstellt und die Datei in einem Verzeichnis ohne Profil installiert wird, können Sie möglicherweise nicht dieselbe Komponente für beide Daten verwenden. (Dies führt zu Ausfällen in Szenarien mit mehreren Benutzer , z. B. in [ICE57 beschrieben).](ice57.md) In diesem Fall können Sie möglicherweise angekündigte Verknüpfungen verwenden, um das von Ihnen wünschen Verhalten zu erreichen, oder Sie können einfach sicherstellen, dass sich die Zielkomponente nicht von der Quelle zur lokalen Ausführung ändern kann.

## <a name="result"></a>Ergebnis

ICE67 gibt einen Fehler oder eine Warnung zurück, wenn das Ziel einer nicht angekündigten Verknüpfung nicht zu derselben Komponente gehört wie die Verknüpfung selbst, oder wenn die Attribute der Zielkomponente nicht sicherstellen, dass sich die Installationsstandorte nicht ändern.

## <a name="example"></a>Beispiel

ICE67 meldet die folgende Warnung und Fehler für das gezeigte Beispiel.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 wird von Component2 installiert, aber die Zieldatei File1 wird von component1 installiert. Die Zielkomponente ist als optional gekennzeichnet (d. h., sie kann lokal oder aus der Quelle ausgeführt werden). Eine mögliche Situation, die zu einem Problem führen würde, ist, wenn Component1 von "run-from-source" in "local" wechselt. Dies würde dazu führen, dass Shortcut1 auf einen ungültigen Speicherort zeigen würde.

Um diese Warnung zu beheben, installieren Sie die Verknüpfung als Teil von Component1, oder markieren Sie Component1 als LocalOnly oder SourceOnly.

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ |
|-------|-------------|
| Datei1 | Komponente1  |



 

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Komponente\_ | Ziel      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#File1\] |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente  | Attribute |
|------------|------------|
| Komponente1 | 2          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



