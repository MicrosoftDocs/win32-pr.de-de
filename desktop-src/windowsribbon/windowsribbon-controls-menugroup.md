---
title: Menü Gruppe
description: Die Menü Gruppe organisiert verwandte Befehle und Steuerelemente in einem Menü oder einer Symbolleiste.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949008"
---
# <a name="menu-group"></a><span data-ttu-id="48193-103">Menü Gruppe</span><span class="sxs-lookup"><span data-stu-id="48193-103">Menu Group</span></span>

<span data-ttu-id="48193-104">Die Menü Gruppe organisiert verwandte Befehle und Steuerelemente in einem Menü oder einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="48193-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="48193-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="48193-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="48193-106">Menü Gruppen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48193-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="48193-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48193-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="48193-108">Einführung</span><span class="sxs-lookup"><span data-stu-id="48193-108">Introduction</span></span>

<span data-ttu-id="48193-109">Das Menü Gruppen Steuerelement, das über das [**MenuGroup**](windowsribbon-element-menugroup.md) -Markup Element verfügbar gemacht wird, ist ein logischer Container für Gruppen von Elementen oder Befehlen in menübasierten Steuerelementen, einschließlich der [Kontext-Popup](windowsribbon-controls-contextpopup.md) -Mini Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="48193-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="48193-110">Eine Bezeichnung kann für eine Menü Gruppe über das Attribut " *labeltitle* " oder die Eigenschaft " [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) " einer zugeordneten Befehls Deklaration angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="48193-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="48193-111">Der *labeltitle* zugewiesene Wert wird als Kategorieheader gerendert.</span><span class="sxs-lookup"><span data-stu-id="48193-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="48193-112">Das folgende Beispiel veranschaulicht das Befehls Markup für ein Steuerelement unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen, das zwei Menü Gruppen-Befehls Deklarationen enthält.</span><span class="sxs-lookup"><span data-stu-id="48193-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="48193-113">Das folgende Beispiel zeigt das Markup, das für ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Element mit drei [**MenuGroup**](windowsribbon-element-menugroup.md) -Element Deklarationen erforderlich ist, von denen zwei mit den Menü Gruppen Befehlen aus dem vorherigen Beispiel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="48193-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="48193-114">Das *Class* -Attribut des **MenuGroup** -Elements wird verwendet, um die Größe der Menü Elemente anzugeben.</span><span class="sxs-lookup"><span data-stu-id="48193-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="48193-115">Der folgende Screenshot veranschaulicht das Menü (mit drei Menü Gruppen-Steuerelementen), das aus dem Markup in den vorherigen Beispielen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="48193-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![Screenshot eines Menüs mit drei Menü Gruppen-Steuerelementen.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="48193-117">Menü Gruppen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48193-117">Menu Group Properties</span></span>

<span data-ttu-id="48193-118">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Menü Gruppen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="48193-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="48193-119">In der Regel wird eine Menü Gruppen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="48193-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="48193-120">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="48193-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="48193-121">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="48193-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="48193-122">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="48193-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="48193-123">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48193-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="48193-124">In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Menü Gruppen-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="48193-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="48193-125">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="48193-125">Property Key</span></span>                                                                                     | <span data-ttu-id="48193-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="48193-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48193-127">UI- \_ pkey \_ aktiviert</span><span class="sxs-lookup"><span data-stu-id="48193-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="48193-128">Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="48193-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="48193-129">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="48193-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="48193-130">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="48193-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="48193-131">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="48193-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="48193-132">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="48193-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="48193-133">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="48193-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="48193-134">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="48193-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="48193-135">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="48193-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="48193-136">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="48193-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="48193-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48193-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48193-138">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48193-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="48193-139">**MenuGroup-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="48193-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 