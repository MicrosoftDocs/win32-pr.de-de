---
title: MiniToolbar-Element
description: Stellt eine kontextbezogene Symbolleiste dar.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- MiniToolbar-Element Windows-Menüband
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443261"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="ce761-104">MiniToolbar-Element</span><span class="sxs-lookup"><span data-stu-id="ce761-104">MiniToolbar element</span></span>

<span data-ttu-id="ce761-105">Stellt eine kontextbezogene Symbolleiste dar.</span><span class="sxs-lookup"><span data-stu-id="ce761-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="ce761-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ce761-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="ce761-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce761-107">Attributes</span></span>



| <span data-ttu-id="ce761-108">attribute</span><span class="sxs-lookup"><span data-stu-id="ce761-108">Attribute</span></span>           | <span data-ttu-id="ce761-109">Typ</span><span class="sxs-lookup"><span data-stu-id="ce761-109">Type</span></span>                 | <span data-ttu-id="ce761-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ce761-110">Required</span></span>       | <span data-ttu-id="ce761-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce761-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce761-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce761-112">**Name**</span></span><br/> | <span data-ttu-id="ce761-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ce761-113">xs:string</span></span><br/> | <span data-ttu-id="ce761-114">Ja</span><span class="sxs-lookup"><span data-stu-id="ce761-114">Yes</span></span><br/> | <span data-ttu-id="ce761-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="ce761-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ce761-116">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="ce761-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="ce761-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce761-117">Child elements</span></span>



| <span data-ttu-id="ce761-118">Element</span><span class="sxs-lookup"><span data-stu-id="ce761-118">Element</span></span>                                                         | <span data-ttu-id="ce761-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce761-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ce761-120">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="ce761-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="ce761-121">Muss mindestens einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="ce761-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ce761-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce761-122">Parent elements</span></span>



| <span data-ttu-id="ce761-123">Element</span><span class="sxs-lookup"><span data-stu-id="ce761-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce761-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="ce761-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ce761-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce761-125">Remarks</span></span>

<span data-ttu-id="ce761-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce761-126">Optional.</span></span>

<span data-ttu-id="ce761-127">Kann ein oder mehrere Male für jede [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="ce761-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="ce761-128">Im Gegensatz zum [**ContextMenu-Element**](windowsribbon-element-contextmenu.md) bleibt die **MiniToolbar** sichtbar, wenn auf ein Element auf der Symbolleiste geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="ce761-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="ce761-129">Wenn die **Minitoolleiste** ohne [**ContextMenu**](windowsribbon-element-contextmenu.md)angezeigt wird, wird sie ausgeblendet, wenn der Mauszeiger entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ce761-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="ce761-130">Aufgrund dieses verblassenden Verhaltens sollte ein [**ContextMenu**](windowsribbon-element-contextmenu.md) in unmittelbarer Nähe zum Mauszeiger angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce761-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="ce761-131">Da auf Steuerelemente in der **MiniToolbar** nicht über die Tastatur zugegriffen werden kann, sollten die verfügbar gemachten Befehle an anderer Stelle auf der Menübandbenutzeroberfläche verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ce761-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="ce761-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce761-132">Examples</span></span>

<span data-ttu-id="ce761-133">Im folgenden Beispiel wird das grundlegende Markup für eine [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ce761-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="ce761-134">Dieser Codeabschnitt zeigt eine Reihe von **MiniToolbar-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="ce761-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a><span data-ttu-id="ce761-135">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce761-135">Element information</span></span>

* <span data-ttu-id="ce761-136">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce761-136">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="ce761-137">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="ce761-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ce761-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce761-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce761-139">Kontext-Popup-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ce761-139">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





