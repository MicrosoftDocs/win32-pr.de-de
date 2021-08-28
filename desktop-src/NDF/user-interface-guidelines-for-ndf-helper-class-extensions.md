---
title: Benutzeroberflächenrichtlinien für NDF-Hilfsklassenerweiterungen
description: Beim Erstellen der Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparaturschritte nachvollziehen kann.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0094dbee5410d512cfa85f9c227d4b0217f1c507662addb4735023a2ba5833eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801720"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Benutzeroberflächenrichtlinien für NDF-Hilfsklassenerweiterungen

Beim Erstellen der Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparaturschritte nachvollziehen kann.

## <a name="root-cause-and-repair"></a>Grundursache und Reparatur

Wenn ein Vorfall auftritt, wird ein Dialogfeld angezeigt, in dem der Benutzer darüber informiert wird, was passiert ist. Der von Ihnen erstellte Text wird in zwei separaten Bereichen angezeigt.

-   **Grundursache:** Eine kurze Beschreibung der Ursache des Problems. Enthält Informationen, mit deren Hilfe ein Administrator oder ein erweiterter Benutzer das Problem beheben kann.
-   **Reparieren:** Erweitert die Grundursache, um weitere Details zu den Schritten zur Verfügung zu stellen, die ein Benutzer ausführen kann, ohne zu lang zu werden.

Jede Grundursache oder Reparatur sollte einen Titel und eine Beschreibung enthalten. Der text vor dem ersten \\ "n"-Zeichen wird für den Titel verwendet. Für die Beschreibung wird der text nach dem ersten "n"-Zeichen (einschließlich aller nachfolgenden \\ Zeilenumbrüche) verwendet.

## <a name="title-guidelines"></a>Titelrichtlinien

Der Titel einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:

-   Muss mindestens 128 Zeichen lang sein. (40 Zeichen oder weniger werden empfohlen.)
-   Sollte nicht mit einem Zeitraum enden.

## <a name="description-guidelines"></a>Beschreibungsrichtlinien

Die Beschreibung einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:

-   Muss mindestens 512 Zeichen lang sein.
-   Jeder Satz sollte mit einem Zeitraum enden.
-   Das Zeichen \\ "n" kann verwendet werden, um einen Zeilenumbruch in der Beschreibung zu erstellen.

 

 




