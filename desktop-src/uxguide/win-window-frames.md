---
title: Fensterrahmen
description: Die meisten Programme sollten Standardfensterrahmen verwenden. Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen ausblendet. Erwägen Sie die strategische Verwendung von Glass für ein einfacheres, leichteres, zusammenhängenderes Aussehen.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dee701f7aad12e348a89034010de1f44134e9d3e
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812257"
---
# <a name="window-frames"></a>Fensterrahmen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Die meisten Programme sollten Standardfensterrahmen verwenden. Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen ausblendet. Erwägen Sie die strategische Verwendung von Glass für ein einfacheres, leichteres, zusammenhängenderes Aussehen.

Mit einem Fensterrahmen können Benutzer ein Fenster bearbeiten und den Titel und das Symbol anzeigen, um dessen Inhalt zu identifizieren.

![Screenshot des Fensterrahmens um das Editorfenster ](images/win-window-frames-image1.png)

Ein typischer Fensterrahmen.

**Hinweis:** Richtlinien zur [Fensterverwaltung](win-window-mgt.md) und zum [Branding](exper-branding.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="glass-window-frames"></a>Glass window frames (Fensterrahmen für Die Brille)

Die Fensterrahmen sind ein beeindruckender neuer Aspekt der Microsoft-Windows, die sowohl ansprechend als auch einfach sein möchten. Diese durchscheinenden Frames bieten Fenstern eine offene, weniger indringliche Darstellung, die es Benutzern ermöglicht, sich auf Inhalte und Funktionen zu konzentrieren, anstatt auf die Schnittstelle, die sie umgibt.

![Screenshot des Glassframes um den Rechner ](images/win-window-frames-image2.png)

Fensterrahmen für Die Brille.

Sie können Glass in kleinen Regionen innerhalb eines Fensters, das den Fensterrahmen berührt, strategisch verwenden. Solche Bereiche scheinen Teil des Fensterrahmens zu sein, obwohl sie technisch gesehen Teil des Clientbereichs des Fensters sind.

![Screenshot des Fensters mit durchscheinender Kante ](images/win-window-frames-image3.png)

In diesem Beispiel wird glass im Clientbereich verwendet, damit es wie ein Teil des Rahmens aussieht.

### <a name="hidden-frames"></a>Ausgeblendete Frames

Manchmal ist der beste Fensterrahmen überhaupt kein Frame. Dies ist häufig der Fall für das [primäre Fenster](glossary.md) von immersiven [Vollbildanwendungen,](glossary.md) die nicht in Verbindung mit anderen Programmen wie Medienplayern, Spielen und Kioskanwendungen verwendet werden.

Inhalts-Viewer profitieren häufig von der Option zum Anzeigen von Inhalten im Vollbildmodus. Beispiele hierfür sind Windows Internet Explorer, Windows Live Fotogalerie, Windows Movie Maker HD, Microsoft PowerPoint und Microsoft Word.

![Screenshot des Medienplayers in der Vollbildansicht ](images/win-window-frames-image4.png)

In diesem Beispiel können Windows Media Player ihren Inhalt im Vollbildmodus anzeigen.

### <a name="custom-frames"></a>Benutzerdefinierte Frames

Die meisten Windows Anwendungen sollten die Standardfensterrahmen verwenden. Für immersive, vollbildige, eigenständige Anwendungen wie Spiele und Kioskanwendungen kann es jedoch sinnvoll sein, benutzerdefinierte Frames für alle Fenster zu verwenden, die nicht im Vollbildmodus angezeigt werden. Der Beweggrund für die Verwendung benutzerdefinierter Frames sollte darin sein, der Gesamterfahrung ein einzigartiges Gefühl zu geben, nicht nur für [das Branding.](exper-branding.md)

![Abbildung von Verrenkungsbild und Rahmen ](images/win-window-frames-image5.png)

Benutzerdefinierte Frames eignen sich für immersive, eigenständige Vollbildanwendungen wie Spiele.

## <a name="guidelines"></a>Richtlinien

### <a name="window-frames"></a>Fensterrahmen

-   Verwenden Sie Standardfensterrahmen.
    -   **Ausnahme:** Um immersiven Vollbild-, eigenständigen Anwendungen ein einzigartiges Gefühl zu geben:
        -   Erwägen Sie, den Fensterrahmen des [primären Fensters](glossary.md)zu verbergen.
        -   Erwägen Sie die Verwendung von benutzerdefinierten Frames für [das sekundäre Fenster.](glossary.md)
        -   Wenn ein benutzerdefinierter Rahmen geeignet ist, wählen Sie ein Design aus, das einfach ist und nicht zu viel Aufmerksamkeit auf sich selbst richtet.

            **Falsch:**

            ![Screenshot des ablenkenden Frames ](images/win-window-frames-image6.png)

            In diesem Beispiel geht der benutzerdefinierte Frame zu sehr auf sich selbst ein.
-   Fügen Sie keinem Fensterrahmen keine Steuerelemente hinzu. Legen Sie stattdessen die Steuerelemente in das Fenster ein.

    **Falsch:**

    ![Screenshot des Steuerelements im Fensterrahmen ](images/win-window-frames-image7.png)

    **Richtig:**

    ![Screenshot des Steuerelements im Clientbereich ](images/win-window-frames-image8.png)

    Im richtigen Beispiel befindet sich das Steuerelement im Clientbereich anstelle des Fensterrahmens.

### <a name="full-screen-mode"></a>Vollbildmodus

-   Für Programme, die über einen optionalen Vollbildmodus verfügen, um den Vollbildmodus zu aktivieren:
    -   Verwenden Sie einen modalen Vollbildbefehl in der Menüleiste oder Symbolleiste. Wenn der Benutzer auf den Befehl klickt, zeigen Sie den Befehl im ausgewählten Zustand an.

        ![Screenshot des Fensters mit Vollbildmenüelement ](images/win-window-frames-image9.png)

        In diesem Beispiel wird der Vollbildbefehl zusammen mit der standardverknüpfungstaste gezeigt.

-   Verwenden Sie F11 für die Vollbildtaste.
-   Wenn eine Symbolleiste vorhanden ist und der Vollbildmodus häufig verwendet wird, verfügen Sie auch über eine grafische Symbolleistenschaltfläche mit einer QuickInfo für den Vollbildmodus.

    ![Screenshot des Vollbilds und Zurücksetzen von Schaltflächen ](images/win-window-frames-image10.png)

    Beispiele für Vollbild-Symbolleistenschaltflächen.

-   So kehren Sie aus dem Vollbildmodus zurück:
    -   Verwenden Sie einen modalen Vollbildbefehl in der Menüleiste oder Symbolleiste. Wenn der Benutzer auf den Befehl klickt, wird der Befehl im gelöschten Zustand angezeigt.
    -   Verwenden Sie F11 für die Vollbildtaste. Wenn es nicht bereits zugewiesen ist, kann esc auch für diesen Zweck verwendet werden.

### <a name="glass"></a>Glas

Standardfensterrahmen verwenden glass automatisch in Windows, aber Sie können auch Glass in Regionen verwenden, die den Fensterrahmen berühren.

-   **Erwägen Sie die strategische Verwendung von Glass in kleinen Regionen, die den Fensterrahmen ohne Text berühren.** Auf diese Weise kann ein Programm ein einfacheres, leichteres und zusammenhängenderes Aussehen erhalten, indem der Bereich als Teil des Frames angezeigt wird.
-   ![Screenshot des Fensters mit durchscheinender Kante ](images/win-window-frames-image3.png)
-   In diesem Beispiel konzentriert glass die Aufmerksamkeit des Benutzers auf den Inhalt und nicht auf die Steuerelemente.
-   **Verwenden Sie keine Brille in Situationen, in denen ein Einfacher Fensterhintergrund ansprechender oder einfacher zu verwenden wäre.**

**Richtig:**

![Screenshot des Fensters mit vier Grafiken und Bezeichnungen ](images/win-window-frames-image11.png)

In diesem Beispiel wird glass verwendet, um dem Alt+TAB-Fenster ein einfaches Aussehen zu verleihen. Glass funktioniert für dieses Fenster, da es aus Grafiken und einer einzelnen, starken Textbezeichnung besteht.

**Falsch:**

![Screenshot des Fensters mit zwölf Grafiken ](images/win-window-frames-image12.png)

In diesem falschen Beispiel ist die Verwendung von Glass ablenkend. Ein Einfacher Fensterhintergrund wäre eine bessere Wahl.

 

 
