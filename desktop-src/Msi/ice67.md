---
description: ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zur gleichen Komponente wie die Verknüpfung selbst gehört, oder ob die Attribute der Zielkomponente sicherstellen, dass die Installations Speicherorte nicht geändert werden.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960484"
---
# <a name="ice67"></a>ICE67

ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zur gleichen Komponente wie die Verknüpfung selbst gehört, oder ob die Attribute der Zielkomponente sicherstellen, dass die Installations Speicherorte nicht geändert werden.

Wenn eine Warnung oder ein Fehler, der von ICE67 gemeldet wird, nicht behoben werden kann, kann die Verknüpfung ungültig werden, wenn die Zielkomponente den Zustand ändert und die Quell Komponente dies nicht bewirkt. Wenn z. b. die Komponente der Zieldatei auf "aus Quelle ausführen" festgelegt ist, führt eine Neuinstallation, bei der die Komponente in "lokal" geändert wird, dazu, dass die Komponente mit der Verknüpfung nicht neu installiert wird. Daher verweist die Verknüpfung auf einen ungültigen Speicherort.

Beachten Sie, dass die Verwendung einer anderen Komponente für die Verknüpfung in einigen Fällen unvermeidlich ist. Wenn die Verknüpfung z. b. im Benutzerprofil erstellt wird und die Datei in einem Verzeichnis ohne Profil installiert wird, können Sie möglicherweise nicht die gleiche Komponente für beide Datenelemente verwenden. (Dies führt zu Fehlern in Szenarios mit mehreren Benutzern – z. b. in [ICE57](ice57.md)). In diesem Fall können Sie möglicherweise angekündigte Verknüpfungen verwenden, um das gewünschte Verhalten zu erreichen, oder Sie können einfach sicherstellen, dass die Zielkomponente nicht von der Quelle in den lokalen Typ geändert werden kann.

## <a name="result"></a>Ergebnis

ICE67 gibt einen Fehler oder eine Warnung aus, wenn das Ziel einer nicht angekündigten Verknüpfung nicht zur gleichen Komponente wie die Verknüpfung selbst gehört, oder wenn die Attribute der Zielkomponente nicht sicherstellen, dass die Installations Speicherorte nicht geändert werden.

## <a name="example"></a>Beispiel

ICE67 meldet die folgenden Warnungen und Fehler für das gezeigte Beispiel.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 wird von Component2 installiert, aber die Zieldatei file1 wird von Component1 installiert. Die Zielkomponente ist als optional gekennzeichnet (was bedeutet, dass Sie lokal oder von der Quelle aus ausgeführt werden kann). Eine mögliche Situation, die zu einem Problem führt, besteht darin, dass Component1 von der Quelle in den lokalen Zustand wechselt. Dies würde dazu führen, dass Shortcut1 auf einen ungültigen Speicherort verweist.

Um diese Warnung zu beheben, installieren Sie die Verknüpfung als Teil von Component1, oder markieren Sie Component1 als LocalOnly oder sourceOnly.

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ |
|-------|-------------|
| Datei1 | Component1  |



 

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Komponente\_ | Ziel      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#File1\] |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Attribute |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



