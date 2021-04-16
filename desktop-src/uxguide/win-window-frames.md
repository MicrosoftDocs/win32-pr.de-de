---
title: Fensterrahmen
description: Die meisten Programme sollten Standardfenster Rahmen verwenden. Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen verbirgt. Sie sollten Glas strategisch für ein einfacheres, helleres aussehen in Erwägung gezogen werden.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552831"
---
# <a name="window-frames"></a>Fensterrahmen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Die meisten Programme sollten Standardfenster Rahmen verwenden. Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen verbirgt. Sie sollten Glas strategisch für ein einfacheres, helleres aussehen in Erwägung gezogen werden.

Mit einem Fensterrahmen können Benutzer ein Fenster bearbeiten und den Titel und das Symbol anzeigen, um dessen Inhalte zu identifizieren.

![Screenshot des Fensterrahmens um das Editor Fenster ](images/win-window-frames-image1.png)

Ein typischer Fensterrahmen.

**Hinweis:** Richtlinien für die [Fensterverwaltung](win-window-mgt.md) und das [Branding](exper-branding.md) werden in separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="glass-window-frames"></a>Glasfenster Rahmen

Die Glasfenster Rahmen sind ein neuer Aspekt der Microsoft Windows-Ästhetik, der sowohl ansprechend als auch leicht zu sein ist. Diese Durchschnitt stellen ermöglichen Windows ein offenes, weniger eindringliches Erscheinungsbild, das es Benutzern ermöglicht, sich auf Inhalte und Funktionen zu konzentrieren und nicht auf die Schnittstelle, die

![Screenshot des Glasrahmens um den Rechner ](images/win-window-frames-image2.png)

Glasfenster Rahmen.

Sie können Glas in kleinen Regionen in einem Fenster, das den Fensterrahmen berührt, strategisch strategisch verwenden. Diese Bereiche scheinen Teil des Fensterrahmens zu sein, auch wenn Sie technisch gesehen Teil des Client Bereichs des Fensters sind.

![Screenshot des Fensters mit der durchlässigen Kante ](images/win-window-frames-image3.png)

In diesem Beispiel wird Glas im Client Bereich verwendet, um einen Teil des Frames zu sehen.

### <a name="hidden-frames"></a>Verborgene Frames

Manchmal ist der beste Fensterrahmen überhaupt kein Frame. Dies ist häufig der Fall für das [primäre Fenster](glossary.md) von immersiven [Vollbild](glossary.md) -Anwendungen, die nicht zusammen mit anderen Programmen verwendet werden, wie z. b. Medien Player, Spiele und Kiosk Anwendungen.

Inhalts Betrachter profitieren häufig von der Option, Inhalte voll Bildschirm anzuzeigen. Beispiele hierfür sind Windows Internet Explorer, Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint und Microsoft Word.

![Screenshot von Media Player in der Vollbildansicht ](images/win-window-frames-image4.png)

In diesem Beispiel kann der Inhalt des Windows-Media Player voll Bildschirms angezeigt werden.

### <a name="custom-frames"></a>Benutzerdefinierte Frames

Die meisten Windows-Anwendungen sollten die Standardfenster Rahmen verwenden. Bei immersiven, eigenständigen, eigenständigen Anwendungen wie spielen und Kiosk Anwendungen kann es jedoch sinnvoll sein, benutzerdefinierte Frames für alle Fenster zu verwenden, die nicht voll Bildschirm angezeigt werden. Die Motivation für die Verwendung von benutzerdefinierten Frames sollte darin bestehen, die allgemeine Darstellung zu einem einzigartigen Verhalten zu machen, nicht nur für [Branding](exper-branding.md).

![Abbildung von Durcheinander und Frame des zusammen gewürelten Bilds ](images/win-window-frames-image5.png)

Benutzerdefinierte Frames eignen sich für immersive, voll Bild-und eigenständige Anwendungen, wie z. b. Spiele.

## <a name="guidelines"></a>Richtlinien

### <a name="window-frames"></a>Fensterrahmen

-   Standardfenster Rahmen verwenden.
    -   **Ausnahme:** Um immersive Vollbild-, eigenständige Anwendungen zu einem einzigartigen Gefühl zu machen:
        -   Sie sollten den Fensterrahmen des [primären Fensters](glossary.md)ausblenden.
        -   Verwenden Sie benutzerdefinierte Frames für ein [sekundäres Fenster](glossary.md).
        -   Wenn ein benutzerdefinierter Frame geeignet ist, wählen Sie einen Entwurf aus, der einfach ist und nicht zu viel Aufmerksamkeit auf sich selbst zeichnet.

            **Falsch:**

            ![Screenshot des abfragende Frames ](images/win-window-frames-image6.png)

            In diesem Beispiel zeichnet der benutzerdefinierte Frame eine zu große Aufmerksamkeit auf sich selbst.
-   Fügen Sie einem Fensterrahmen keine Steuerelemente hinzu. Fügen Sie die Steuerelemente stattdessen in das Fenster ein.

    **Falsch:**

    ![Screenshot des Steuer Elements im Fensterrahmen ](images/win-window-frames-image7.png)

    **Richtig:**

    ![Screenshot des Steuer Elements im Client Bereich ](images/win-window-frames-image8.png)

    Im richtigen Beispiel befindet sich das Steuerelement innerhalb des Client Bereichs anstelle des Fensterrahmens.

### <a name="full-screen-mode"></a>Vollbildmodus

-   Für Programme, die einen optionalen Vollbildmodus aufweisen, um den Vollbildmodus zu aktivieren:
    -   Sie haben einen modalen Vollbild-Befehl in der Menüleiste oder in der Symbolleiste. Wenn der Benutzer auf den Befehl klickt, wird der Befehl im ausgewählten Zustand angezeigt.

        ![Screenshot des Fensters mit dem Menü Element "Vollbild" ](images/win-window-frames-image9.png)

        In diesem Beispiel wird der Vollbild-Befehl zusammen mit der Standard-Tastenkombination angezeigt.

-   Verwenden Sie F11 für die Tastenkombination für den Vollbildmodus.
-   Wenn eine Symbolleiste und der Vollbildmodus häufig verwendet werden, haben Sie auch eine Grafik Symbolleisten-Schaltfläche mit einer Vollbild-QuickInfo.

    ![Screenshot der Schaltflächen zum Vollbildmodus und zum Zurücksetzen ](images/win-window-frames-image10.png)

    Beispiele für Vollbild-Symbolleisten-Schaltflächen.

-   So kehren Sie den Vollbildmodus wieder her:
    -   Sie haben einen modalen Vollbild-Befehl in der Menüleiste oder in der Symbolleiste. Wenn der Benutzer auf den Befehl klickt, zeigen Sie den Befehl im Zustand "gelöscht" an.
    -   Verwenden Sie F11 für die Tastenkombination für den Vollbildmodus. Wenn die Zuordnung nicht bereits erfolgt ist, kann ESC auch zu diesem Zweck verwendet werden.

### <a name="glass"></a>Glas

Standard Fensterrahmen verwenden in Windows automatisch Glas, Sie können jedoch auch Glas in Regionen verwenden, die den Fensterrahmen berühren.

-   **Es empfiehlt sich, Glas strategisch in kleinen Regionen zu verwenden, die den Fensterrahmen ohne Text berühren.** Dies kann einem Programm ein einfacheres, helleres aussehen ermöglichen, indem die Region als Teil des Frames angezeigt wird.
-   ![Screenshot des Fensters mit der durchlässigen Kante ](images/win-window-frames-image3.png)
-   In diesem Beispiel konzentriert sich die Aufmerksamkeit des Benutzers auf den Inhalt und nicht auf die Steuerelemente.
-   **Verwenden Sie kein Glas in Situationen, in denen ein einfacher Fenster Hintergrund attraktiver oder leichter zu verwenden wäre.**

**Richtig:**

![Screenshot des Fensters mit vier Grafiken und Bezeichnungen ](images/win-window-frames-image11.png)

In diesem Beispiel wird Glas verwendet, um dem Alt + Tab-Fenster ein schlankes aussehen zu geben. Glas funktioniert für dieses Fenster, weil es aus Grafiken und einer einzelnen, starken Text Bezeichnung besteht.

**Falsch:**

![Screenshot des Fensters mit zwölf Grafiken ](images/win-window-frames-image12.png)

In diesem falschen Beispiel ist die Verwendung von Glas ablenkend. Ein einfacher Hintergrund ist eine bessere Wahl.

 

 