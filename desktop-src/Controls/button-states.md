---
title: Schaltflächen Zustände
description: In diesem Abschnitt wird erläutert, wie die Auswahl einer Schaltfläche den Zustand und die Reaktion der Anwendung ändert.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474445"
---
# <a name="button-states"></a>Schaltflächen Zustände

In diesem Abschnitt wird erläutert, wie die Auswahl einer Schaltfläche den Zustand und die Reaktion der Anwendung ändert.

Der Abschnitt besteht aus den folgenden Themen:

-   [Schaltflächen Auswahl](#button-selection)
-   [Elemente eines Schaltflächen Zustands](#elements-of-a-button-state)
    -   [Fokus Zustand](#focus-state)
    -   [Pushzustand](#push-state)
    -   [Status überprüfen](#check-state)
-   [Änderungen an einem Schaltflächen Zustand](#changes-to-a-button-state)

## <a name="button-selection"></a>Schaltflächen Auswahl

Der Benutzer kann eine Schaltfläche auf drei Arten auswählen: durch Klicken mit der Maus, durch Tabstopps und drücken der Eingabetaste bzw. (wenn die Schaltfläche Teil einer Gruppe ist, die durch das Format der [**WS- \_ Gruppe**](/windows/desktop/winmsg/window-styles) definiert ist), indem Sie in der Gruppe auf die ausgewählte Schaltfläche klicken und die Pfeiltasten zum Verschieben innerhalb dieser Gruppe verwenden. Die zwei Tabstopps-Methoden sind Teil der vordefinierten Tastaturschnittstelle, die vom System bereitgestellt wird. Eine umfassende Beschreibung dieser Schnittstelle finden Sie unter [Dialog Felder](/windows/desktop/dlgbox/dialog-boxes).

Die Auswahl einer Schaltfläche verursacht in der Regel die folgenden Ereignisse:

-   Das System gibt die Schaltfläche mit dem Tastaturfokus.
-   Die Schaltfläche sendet über das übergeordnete Fenster eine Meldung, um Sie über die Auswahl zu benachrichtigen.
-   Das übergeordnete Fenster (oder das System) sendet der Schaltfläche eine Meldung, um deren Zustand zu ändern.
-   Das übergeordnete Fenster (oder das System) zeichnet die Schaltfläche neu, um den neuen Zustand widerzuspiegeln.

## <a name="elements-of-a-button-state"></a>Elemente eines Schaltflächen Zustands

Der Zustand einer Schaltfläche kann durch den Fokus Zustand, den pushzustand und den Prüf Zustand gekennzeichnet werden.

-   [Fokus Zustand](#focus-state)
-   [Pushzustand](#push-state)
-   [Status überprüfen](#check-state)

### <a name="focus-state"></a>Fokus Zustand

Der Fokus Zustand gilt für ein Kontrollkästchen, ein Optionsfeld, eine Schaltfläche oder eine vom Besitzer gezeichnete Schaltfläche. Eine Schaltfläche empfängt den Tastaturfokus, wenn der Benutzer Sie auswählt, und verliert den Fokus, wenn der Benutzer ein anderes Steuerelement auswählt. Nur ein Steuerelement kann den Tastaturfokus gleichzeitig aufweisen.

Wenn eine Schaltfläche den Tastaturfokus besitzt, markiert das System in der Regel den Text, das Symbol oder die Bitmap einer Schaltfläche, indem Sie Sie mit einer gepunkteten Linie umgibt. Außerdem verfügt eine Schaltfläche mit einem schweren dunklen Rand, wenn Sie den Fokus besitzt. Das System ändert automatisch die Hervorhebung für eine automatische Schaltfläche, aber die Anwendung muss die Hervorhebung für eine nicht automatische Schaltfläche ändern, indem Nachrichten gesendet werden.

### <a name="push-state"></a>Pushzustand

Der pushzustand gilt für eine Schaltfläche, ein Kontrollkästchen, ein Optionsfeld oder ein Kontrollkästchen mit drei Zuständen, gilt aber nicht für andere Schaltflächen. Der pushzustand einer Schaltfläche kann entweder per Push oder nicht per Push übermittelt werden. Wenn eine Schaltfläche für die pushübertragung (oder eine beliebige Schaltfläche mit dem b-Format [**b \_**](button-styles.md) ) per Push abgelegt wird, wird die Schaltfläche als abgesenkter Schaltfläche Wenn Sie nicht per Pushvorgang übermittelt wird, wird Sie als aufgelöster Schaltfläche gezeichnet. Wenn Sie auf ein Kontrollkästchen, ein Optionsfeld oder ein Kontrollkästchen mit drei Zuständen klicken, ist der Hintergrund der Schaltfläche abgeblendet. Wenn Sie nicht per Pushvorgang übertragen wird, ist der Hintergrund der Schaltfläche nicht ausgegraut.

### <a name="check-state"></a>Status überprüfen

Der Zustand überprüfen gilt für ein Kontrollkästchen, ein Optionsfeld oder ein Kontrollkästchen mit drei Zuständen, gilt aber nicht für andere Schaltflächen. Der Status kann überprüft, gelöscht oder (für Kontrollkästchen mit drei Zuständen) unbestimmt werden. Ein Kontrollkästchen wird aktiviert, wenn ein Häkchen enthalten ist, und wird deaktiviert, wenn dies nicht der Fall ist. Ein Optionsfeld wird aktiviert, wenn es einen schwarzen Punkt enthält. Wenn dies nicht der Fall ist, wird Sie gelöscht. Ein Kontrollkästchen mit drei Zuständen ist aktiviert, wenn es ein Häkchen enthält, nicht gelöscht wird und unbestimmt ist, wenn es ein abgeschnischtes Feld enthält. Das System ändert automatisch den Status der Überprüfung einer automatischen Schaltfläche, aber die Anwendung muss den Integritäts Status einer nicht automatischen Schaltfläche ändern.

## <a name="changes-to-a-button-state"></a>Änderungen an einem Schaltflächen Zustand

Wenn der Benutzer eine Schaltfläche auswählt, ist es in der Regel notwendig, eine oder mehrere der Zustands Elemente der Schaltfläche zu ändern. Das System ändert automatisch den Fokus Zustand für alle Schaltflächen Typen, den pushzustand für pushschaltflächen oder Schaltflächen mit der Art " [**b- \_ pushlike**](button-styles.md) " und den Status "überprüfen" für alle automatischen Schaltflächen. Die Anwendung muss alle anderen Statusänderungen vornehmen, wobei der Typ, der Stil und der aktuelle Zustand der Schaltfläche berücksichtigt werden. In der folgenden Liste werden die Zustands Elemente angezeigt, die für die einzelnen Schaltflächen Typen geändert werden müssen:

-   Ein Kontrollkästchen muss den Status der Überprüfung ändern.
-   Ein Optionsfeld muss den Status der Überprüfung ändern. Es kann auch erforderlich sein, den Prüf Zustand anderer Options Felder in derselben Gruppe zu ändern, um die gegenseitig ausschließende Art von Options Feldern sicherzustellen.
-   Da der Zustand einer vom Besitzer gezeichneten Schaltfläche anwendungsabhängig ist, kann die Anwendung, die in der Schaltfläche geändert werden muss, variieren. Es müssen keine Elemente eines Gruppen Felds geändert werden, da Benutzer keine Gruppen Felder auswählen können.

Eine Anwendung kann den Zustand einer Schaltfläche ermitteln, indem Sie [**eine BM \_ getcheck**](bm-getcheck.md) -oder [**BM \_ GetState**](bm-getstate.md) -Nachricht sendet. die Anwendung kann den Zustand einer Schaltfläche festlegen, indem Sie eine [**BM- \_ setcheck**](bm-setcheck.md) -oder [**BM \_ SetState**](bm-setstate.md) -Nachricht sendet.

 

 