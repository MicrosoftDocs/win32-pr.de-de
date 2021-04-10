---
title: MiniToolbar-Element
description: Stellt eine kontextabhängige Symbolleiste dar.
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
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100842"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="02e5e-104">MiniToolbar-Element</span><span class="sxs-lookup"><span data-stu-id="02e5e-104">MiniToolbar element</span></span>

<span data-ttu-id="02e5e-105">Stellt eine kontextabhängige Symbolleiste dar.</span><span class="sxs-lookup"><span data-stu-id="02e5e-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="02e5e-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="02e5e-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="02e5e-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="02e5e-107">Attributes</span></span>



| <span data-ttu-id="02e5e-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="02e5e-108">Attribute</span></span>           | <span data-ttu-id="02e5e-109">type</span><span class="sxs-lookup"><span data-stu-id="02e5e-109">Type</span></span>                 | <span data-ttu-id="02e5e-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02e5e-110">Required</span></span>       | <span data-ttu-id="02e5e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e5e-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e5e-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="02e5e-112">**Name**</span></span><br/> | <span data-ttu-id="02e5e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="02e5e-113">xs:string</span></span><br/> | <span data-ttu-id="02e5e-114">Ja</span><span class="sxs-lookup"><span data-stu-id="02e5e-114">Yes</span></span><br/> | <span data-ttu-id="02e5e-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="02e5e-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="02e5e-116">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="02e5e-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="02e5e-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02e5e-117">Child elements</span></span>



| <span data-ttu-id="02e5e-118">Element</span><span class="sxs-lookup"><span data-stu-id="02e5e-118">Element</span></span>                                                         | <span data-ttu-id="02e5e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e5e-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="02e5e-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="02e5e-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="02e5e-121">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="02e5e-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="02e5e-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02e5e-122">Parent elements</span></span>



| <span data-ttu-id="02e5e-123">Element</span><span class="sxs-lookup"><span data-stu-id="02e5e-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02e5e-124">**Contextpopup. minitoolbars**</span><span class="sxs-lookup"><span data-stu-id="02e5e-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="02e5e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e5e-125">Remarks</span></span>

<span data-ttu-id="02e5e-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="02e5e-126">Optional.</span></span>

<span data-ttu-id="02e5e-127">Kann für jede " [**contextpopup. minitoolbars**](windowsribbon-element-contextpopup-minitoolbars.md)" einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="02e5e-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="02e5e-128">Anders als das [**ContextMenu**](windowsribbon-element-contextmenu.md) -Element bleibt die **MiniToolbar** sichtbar, wenn auf ein Element auf der Symbolleiste geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="02e5e-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="02e5e-129">Wenn es ohne [**ContextMenu**](windowsribbon-element-contextmenu.md)angezeigt wird, wird die **MiniToolbar** ausgeblendet, wenn der Mauszeiger entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="02e5e-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="02e5e-130">Aufgrund dieses verblassenden Verhaltens sollte ein [**ContextMenu**](windowsribbon-element-contextmenu.md) in der Nähe des Mauszeigers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="02e5e-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="02e5e-131">Da Steuerelemente in der **MiniToolbar** nicht auf Tastatur zugänglich sind, sollten die von Ihnen verfügbar gemachten Befehle an anderer Stelle in der Multifunktionsleisten-Benutzeroberfläche verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="02e5e-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="02e5e-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02e5e-132">Examples</span></span>

<span data-ttu-id="02e5e-133">Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="02e5e-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="02e5e-134">Dieser Code Abschnitt zeigt einen Satz von **MiniToolbar** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="02e5e-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="02e5e-135">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="02e5e-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="02e5e-136">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="02e5e-136">Minimum supported system</span></span><br/> | <span data-ttu-id="02e5e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02e5e-137">Windows 7</span></span> |
| <span data-ttu-id="02e5e-138">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="02e5e-138">Can be empty</span></span>                        | <span data-ttu-id="02e5e-139">Nein</span><span class="sxs-lookup"><span data-stu-id="02e5e-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="02e5e-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02e5e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e5e-141">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="02e5e-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





