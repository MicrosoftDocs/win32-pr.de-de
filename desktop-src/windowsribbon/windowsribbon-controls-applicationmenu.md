---
title: Anwendungsmenü
description: Das Anwendungsmenü ist das Hauptmenü für eine Anwendung, die das Windows-Menü Band Framework implementiert.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858262"
---
# <a name="application-menu"></a>Anwendungsmenü

Das Anwendungsmenü ist das Hauptmenü für eine Anwendung, die das Windows-Menü Band Framework implementiert.

-   [Introduction (Einführung)](#introduction)
-   [Komponenten des Anwendungs Menüs](#components-of-the-application-menu)
    -   [Menü "Anwendungsmenü"](#application-menu-menugroup)
-   [Anpassen des Anwendungs Menüs](#sizing-the-application-menu)
-   [Eigenschaften des Anwendungs Menüs](#application-menu-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das Anwendungsmenü besteht aus einem Dropdown-Schaltflächen-Steuerelement, das ein Menü mit Befehlen anzeigt, die Funktionen für ein vollständiges Projekt, z. b. ein gesamtes Dokument, Bild oder einen Film, verfügbar machen. Beispiele hierfür sind die Befehle **New**, **Open**, **Save** und **Exit** .

Der folgende Screenshot veranschaulicht das Anwendungsmenü.

![Screenshot des Menüs "Anwendung" und der Liste "zuletzt verwendete Elemente" des Menübands "Paint for Windows 7".](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Komponenten des Anwendungs Menüs

Das Anwendungsmenü ist ein obligatorisches Element in einer beliebigen Multifunktionsleistenanwendung. Der Einstiegspunkt im Anwendungsmenü ist eine unterschiedliche Schaltfläche, die als erstes Element in der [Register](windowsribbon-controls-tab.md) Karten Zeile angezeigt wird, wie im folgenden Screenshot gezeigt.

> [!Note]  
> Windows 8 und höher: das Bild der Anwendungsmenü Schaltfläche wurde in Bezeichnung: **File** geändert. Es wird empfohlen, die Datei nicht als Bezeichnung für eine ihrer eigenen Registerkarten zu verwenden.

 

![Screenshot der Schaltfläche "Anwendungsmenü" von WordPad für Windows 7.](images/overviews/applicationmenu-button.png)

Wenn Sie auf diese Schaltfläche klicken, wird das umfangreiche Menü angezeigt, das im folgenden Screenshot angezeigt wird (das Anwendungsmenü von WordPad für Windows 7).

![Screenshot des Menüs "Anwendung" von WordPad für Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> Beim Klicken auf die Menü Schaltfläche für die Anwendung gibt es keine Auswirkung auf den Registerkarten Satz. Stattdessen wechselt der Fokus in das Menü.

 

Das Anwendungsmenü enthält zwei Bereiche: eine Liste der Befehle, die durch ein oder mehrere [**MenuGroup**](windowsribbon-element-menugroup.md) -Elemente dargestellt werden, und eine Liste der [zuletzt geöffneten Elemente](windowsribbon-controls-recentitems.md) , die durch ein [**applicationmenu. recentitems**](windowsribbon-element-applicationmenu-recentitems.md) -Element dargestellt wird.

### <a name="application-menu-menugroup"></a>Menü "Anwendungsmenü"

Das [**applicationmenu**](windowsribbon-element-applicationmenu.md) -Element muss mindestens ein untergeordnetes [**MenuGroup**](windowsribbon-element-menugroup.md) -Element enthalten, das eine Liste von Befehlen auf Anwendungsebene verfügbar macht. Wenn mehrere **MenuGroup** -Elemente deklariert sind, wird eine Trennlinie zwischen den Gruppen gezeichnet, wie im folgenden Screenshot gezeigt.

![Screenshot einer Anwendungsmenü-MenuGroup.](images/overviews/applicationmenu-menugroup.png)

Im folgenden finden Sie eine Liste der Einschränkungen für ein [**MenuGroup**](windowsribbon-element-menugroup.md) -Element eines Anwendungs Menüs:

-   Alle [**MenuGroup**](windowsribbon-element-menugroup.md) -Elemente müssen mit einem *Class* -Attribut Wert von deklariert werden `MajorItems` .
-   Eine Anwendungsmenü- [**MenuGroup**](windowsribbon-element-menugroup.md) unterstützt nur die [Schaltflächen Schalt](windowsribbon-controls-button.md)Fläche, [UMSCHALT](windowsribbon-controls-togglebutton.md)Fläche, [Dropdown-](windowsribbon-controls-dropdownbutton.md)Schaltfläche, [Trenn](windowsribbon-controls-splitbutton.md) [Schaltfläche, Dropdown-](windowsribbon-controls-dropdowngallery.md)Katalog und unter [teilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog-Steuerelemente.
    > \[! Wichtig\]  
    > Befehls Galerien sind der einzige Typ des Katalogs, der im Anwendungsmenü unterstützt wird. Weitere Informationen zu Katalog Steuerelementen finden Sie unter [Arbeiten mit Galerien](./ribbon-controls-galleries.md).

     

Wenn eine [Schalt](windowsribbon-controls-button.md) [Fläche oder UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) in einer [**MenuGroup**](windowsribbon-element-menugroup.md)verwendet wird, wird der Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) im Menü angezeigt, und die Werte von [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md) und [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md) werden als QuickInfo angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot eines Schaltflächen-Steuer Elements in einem Anwendungsmenü.](images/overviews/applicationmenu-menubutton.png)

Wenn eine [Dropdown-Schalt](windowsribbon-controls-dropdownbutton.md)Fläche [, eine](windowsribbon-controls-splitbutton.md) [Unterbrechungs Schaltfläche, ein Dropdown](windowsribbon-controls-dropdowngallery.md)Katalog oder eine unter [teilte Schaltflächen Galerie](windowsribbon-controls-splitbuttongallery.md) im Menü Anwendung verwendet wird, wird der Menüteil als Flyout angezeigt, das den Bereich zuletzt verwendete **Elemente** abdeckt und verbirgt.

Für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen-und [Dropdown-Schaltflächen-](windowsribbon-controls-dropdownbutton.md) Steuerelemente wird der Wert von [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md) Inline im Flyout-Menü angezeigt, um Benutzer bei der Ermittlung der Befehls Funktionalität visuell zu unterstützen. Der angezeigte Wert von **Command. labeldescription** wird Programm gesteuert über eine zweizeilige Spanne getrennt, und es wird versucht, den Wert genau über den Bereich für die **zuletzt verwendeten Elemente** zu anpassen. Wenn der **Command. labeldescription** -Wert nicht passt, wird das Flyout erweitert, um den längsten [**Command. Comment**](windowsribbon-element-command-comment.md) -Wert in der [**MenuGroup**](windowsribbon-element-menugroup.md)zu erfüllen.

Der folgende Screenshot veranschaulicht diese Verhaltensweisen in einem Flyout für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen.

![Screenshot eines Listen Steuerelement-Flyout in einem Anwendungsmenü.](images/overviews/applicationmenu-menuflyout.png)

Mithilfe eines [Dropdown](windowsribbon-controls-dropdowngallery.md) Katalogs und einer unter [teilten Schaltflächen Galerie](windowsribbon-controls-splitbuttongallery.md)werden nur eine Bezeichnung und ein Bild angezeigt.

## <a name="sizing-the-application-menu"></a>Anpassen des Anwendungs Menüs

Die Größe des Anwendungs Menüs wird vom Menüband-Framework behandelt. Wenn sehr lange Zeichen folgen für den Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)angegeben werden oder eine lange Liste mit Befehlen verwendet wird, wird die Größe des Menüs angepasst, um den Inhalt aufzunehmen. Einige Formen der Anpassung umfassen das Erweitern der Größe von Flyouts oder Menü Bereichen und das Hinzufügen von schwenken-Viewern, wenn ein Bildlauf erforderlich ist.

## <a name="application-menu-properties"></a>Eigenschaften des Anwendungs Menüs

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Menü Steuerelement der Anwendung.

In der Regel wird eine Anwendungsmenü Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen-Befehl für die [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird behandelt, und die Eigenschafts Aktualisierungen werden durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird erst nach einem aktualisierten Eigenschafts Wert abgefragt, wenn die Eigenschaft vom Framework benötigt wird. Das Framework benötigt z. b. die-Eigenschaft, wenn eine Registerkarte aktiviert wird und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.



| Eigenschafts Schlüssel                                                                                     | Notizen                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Invalidierung aktualisiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Applicationmenu-Markup Element**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 