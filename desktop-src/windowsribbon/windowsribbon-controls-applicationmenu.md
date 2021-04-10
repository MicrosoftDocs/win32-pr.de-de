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
# <a name="application-menu"></a><span data-ttu-id="30b0d-103">Anwendungsmenü</span><span class="sxs-lookup"><span data-stu-id="30b0d-103">Application Menu</span></span>

<span data-ttu-id="30b0d-104">Das Anwendungsmenü ist das Hauptmenü für eine Anwendung, die das Windows-Menü Band Framework implementiert.</span><span class="sxs-lookup"><span data-stu-id="30b0d-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="30b0d-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="30b0d-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="30b0d-106">Komponenten des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="30b0d-107">Menü "Anwendungsmenü"</span><span class="sxs-lookup"><span data-stu-id="30b0d-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="30b0d-108">Anpassen des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="30b0d-109">Eigenschaften des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="30b0d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30b0d-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="30b0d-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="30b0d-111">Introduction</span></span>

<span data-ttu-id="30b0d-112">Das Anwendungsmenü besteht aus einem Dropdown-Schaltflächen-Steuerelement, das ein Menü mit Befehlen anzeigt, die Funktionen für ein vollständiges Projekt, z. b. ein gesamtes Dokument, Bild oder einen Film, verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="30b0d-113">Beispiele hierfür sind die Befehle **New**, **Open**, **Save** und **Exit** .</span><span class="sxs-lookup"><span data-stu-id="30b0d-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="30b0d-114">Der folgende Screenshot veranschaulicht das Anwendungsmenü.</span><span class="sxs-lookup"><span data-stu-id="30b0d-114">The following screen shot illustrates the Application Menu.</span></span>

![Screenshot des Menüs "Anwendung" und der Liste "zuletzt verwendete Elemente" des Menübands "Paint for Windows 7".](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="30b0d-116">Komponenten des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-116">Components of the Application Menu</span></span>

<span data-ttu-id="30b0d-117">Das Anwendungsmenü ist ein obligatorisches Element in einer beliebigen Multifunktionsleistenanwendung.</span><span class="sxs-lookup"><span data-stu-id="30b0d-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="30b0d-118">Der Einstiegspunkt im Anwendungsmenü ist eine unterschiedliche Schaltfläche, die als erstes Element in der [Register](windowsribbon-controls-tab.md) Karten Zeile angezeigt wird, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="30b0d-119">Windows 8 und höher: das Bild der Anwendungsmenü Schaltfläche wurde in Bezeichnung: **File** geändert.</span><span class="sxs-lookup"><span data-stu-id="30b0d-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="30b0d-120">Es wird empfohlen, die Datei nicht als Bezeichnung für eine ihrer eigenen Registerkarten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="30b0d-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![Screenshot der Schaltfläche "Anwendungsmenü" von WordPad für Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="30b0d-122">Wenn Sie auf diese Schaltfläche klicken, wird das umfangreiche Menü angezeigt, das im folgenden Screenshot angezeigt wird (das Anwendungsmenü von WordPad für Windows 7).</span><span class="sxs-lookup"><span data-stu-id="30b0d-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![Screenshot des Menüs "Anwendung" von WordPad für Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="30b0d-124">Beim Klicken auf die Menü Schaltfläche für die Anwendung gibt es keine Auswirkung auf den Registerkarten Satz. Stattdessen wechselt der Fokus in das Menü.</span><span class="sxs-lookup"><span data-stu-id="30b0d-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="30b0d-125">Das Anwendungsmenü enthält zwei Bereiche: eine Liste der Befehle, die durch ein oder mehrere [**MenuGroup**](windowsribbon-element-menugroup.md) -Elemente dargestellt werden, und eine Liste der [zuletzt geöffneten Elemente](windowsribbon-controls-recentitems.md) , die durch ein [**applicationmenu. recentitems**](windowsribbon-element-applicationmenu-recentitems.md) -Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30b0d-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="30b0d-126">Menü "Anwendungsmenü"</span><span class="sxs-lookup"><span data-stu-id="30b0d-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="30b0d-127">Das [**applicationmenu**](windowsribbon-element-applicationmenu.md) -Element muss mindestens ein untergeordnetes [**MenuGroup**](windowsribbon-element-menugroup.md) -Element enthalten, das eine Liste von Befehlen auf Anwendungsebene verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="30b0d-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="30b0d-128">Wenn mehrere **MenuGroup** -Elemente deklariert sind, wird eine Trennlinie zwischen den Gruppen gezeichnet, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![Screenshot einer Anwendungsmenü-MenuGroup.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="30b0d-130">Im folgenden finden Sie eine Liste der Einschränkungen für ein [**MenuGroup**](windowsribbon-element-menugroup.md) -Element eines Anwendungs Menüs:</span><span class="sxs-lookup"><span data-stu-id="30b0d-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="30b0d-131">Alle [**MenuGroup**](windowsribbon-element-menugroup.md) -Elemente müssen mit einem *Class* -Attribut Wert von deklariert werden `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="30b0d-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="30b0d-132">Eine Anwendungsmenü- [**MenuGroup**](windowsribbon-element-menugroup.md) unterstützt nur die [Schaltflächen Schalt](windowsribbon-controls-button.md)Fläche, [UMSCHALT](windowsribbon-controls-togglebutton.md)Fläche, [Dropdown-](windowsribbon-controls-dropdownbutton.md)Schaltfläche, [Trenn](windowsribbon-controls-splitbutton.md) [Schaltfläche, Dropdown-](windowsribbon-controls-dropdowngallery.md)Katalog und unter [teilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="30b0d-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="30b0d-133">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="30b0d-133">\[!Important\]</span></span>  
    > <span data-ttu-id="30b0d-134">Befehls Galerien sind der einzige Typ des Katalogs, der im Anwendungsmenü unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="30b0d-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="30b0d-135">Weitere Informationen zu Katalog Steuerelementen finden Sie unter [Arbeiten mit Galerien](./ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="30b0d-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="30b0d-136">Wenn eine [Schalt](windowsribbon-controls-button.md) [Fläche oder UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) in einer [**MenuGroup**](windowsribbon-element-menugroup.md)verwendet wird, wird der Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) im Menü angezeigt, und die Werte von [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md) und [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md) werden als QuickInfo angezeigt, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![Screenshot eines Schaltflächen-Steuer Elements in einem Anwendungsmenü.](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="30b0d-138">Wenn eine [Dropdown-Schalt](windowsribbon-controls-dropdownbutton.md)Fläche [, eine](windowsribbon-controls-splitbutton.md) [Unterbrechungs Schaltfläche, ein Dropdown](windowsribbon-controls-dropdowngallery.md)Katalog oder eine unter [teilte Schaltflächen Galerie](windowsribbon-controls-splitbuttongallery.md) im Menü Anwendung verwendet wird, wird der Menüteil als Flyout angezeigt, das den Bereich zuletzt verwendete **Elemente** abdeckt und verbirgt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="30b0d-139">Für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen-und [Dropdown-Schaltflächen-](windowsribbon-controls-dropdownbutton.md) Steuerelemente wird der Wert von [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md) Inline im Flyout-Menü angezeigt, um Benutzer bei der Ermittlung der Befehls Funktionalität visuell zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="30b0d-140">Der angezeigte Wert von **Command. labeldescription** wird Programm gesteuert über eine zweizeilige Spanne getrennt, und es wird versucht, den Wert genau über den Bereich für die **zuletzt verwendeten Elemente** zu anpassen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="30b0d-141">Wenn der **Command. labeldescription** -Wert nicht passt, wird das Flyout erweitert, um den längsten [**Command. Comment**](windowsribbon-element-command-comment.md) -Wert in der [**MenuGroup**](windowsribbon-element-menugroup.md)zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="30b0d-142">Der folgende Screenshot veranschaulicht diese Verhaltensweisen in einem Flyout für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![Screenshot eines Listen Steuerelement-Flyout in einem Anwendungsmenü.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="30b0d-144">Mithilfe eines [Dropdown](windowsribbon-controls-dropdowngallery.md) Katalogs und einer unter [teilten Schaltflächen Galerie](windowsribbon-controls-splitbuttongallery.md)werden nur eine Bezeichnung und ein Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="30b0d-145">Anpassen des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-145">Sizing the Application Menu</span></span>

<span data-ttu-id="30b0d-146">Die Größe des Anwendungs Menüs wird vom Menüband-Framework behandelt.</span><span class="sxs-lookup"><span data-stu-id="30b0d-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="30b0d-147">Wenn sehr lange Zeichen folgen für den Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)angegeben werden oder eine lange Liste mit Befehlen verwendet wird, wird die Größe des Menüs angepasst, um den Inhalt aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="30b0d-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="30b0d-148">Einige Formen der Anpassung umfassen das Erweitern der Größe von Flyouts oder Menü Bereichen und das Hinzufügen von schwenken-Viewern, wenn ein Bildlauf erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="30b0d-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="30b0d-149">Eigenschaften des Anwendungs Menüs</span><span class="sxs-lookup"><span data-stu-id="30b0d-149">Application Menu Properties</span></span>

<span data-ttu-id="30b0d-150">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Menü Steuerelement der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="30b0d-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="30b0d-151">In der Regel wird eine Anwendungsmenü Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen-Befehl für die [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="30b0d-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="30b0d-152">Das Invalidierung-Ereignis wird behandelt, und die Eigenschafts Aktualisierungen werden durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="30b0d-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="30b0d-153">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird erst nach einem aktualisierten Eigenschafts Wert abgefragt, wenn die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="30b0d-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="30b0d-154">Das Framework benötigt z. b. die-Eigenschaft, wenn eine Registerkarte aktiviert wird und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="30b0d-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="30b0d-155">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="30b0d-155">Property key</span></span>                                                                                     | <span data-ttu-id="30b0d-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="30b0d-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="30b0d-157">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="30b0d-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="30b0d-158">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="30b0d-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="30b0d-159">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="30b0d-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="30b0d-160">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="30b0d-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="30b0d-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30b0d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b0d-162">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30b0d-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="30b0d-163">**Applicationmenu-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="30b0d-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 