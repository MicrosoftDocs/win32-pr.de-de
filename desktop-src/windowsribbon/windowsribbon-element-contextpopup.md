---
title: Contextpopup-Element
description: Stellt das Kontext-Popup Steuerelement in der contextpopup-Ansicht dar.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Fenster "contextpopup-Element Fenster"
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4feb7c4fbd2ca538fe4d0c2b2584163ee8c9fcea
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038034"
---
# <a name="contextpopup-element"></a><span data-ttu-id="ea6cc-104">Contextpopup-Element</span><span class="sxs-lookup"><span data-stu-id="ea6cc-104">ContextPopup element</span></span>

<span data-ttu-id="ea6cc-105">Stellt das [Kontext-Popup](windowsribbon-controls-contextpopup.md) Steuerelement in der contextpopup-Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="ea6cc-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ea6cc-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="ea6cc-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea6cc-107">Attributes</span></span>

<span data-ttu-id="ea6cc-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea6cc-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea6cc-109">Child elements</span></span>



| <span data-ttu-id="ea6cc-110">Element</span><span class="sxs-lookup"><span data-stu-id="ea6cc-110">Element</span></span>                                                                                         | <span data-ttu-id="ea6cc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea6cc-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ea6cc-112">**Contextpopup. contextmaps**</span><span class="sxs-lookup"><span data-stu-id="ea6cc-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="ea6cc-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="ea6cc-114">**Contextpopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="ea6cc-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="ea6cc-115">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="ea6cc-116">**Contextpopup. minitoolbars**</span><span class="sxs-lookup"><span data-stu-id="ea6cc-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="ea6cc-117">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ea6cc-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea6cc-118">Parent elements</span></span>



| <span data-ttu-id="ea6cc-119">Element</span><span class="sxs-lookup"><span data-stu-id="ea6cc-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ea6cc-120">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="ea6cc-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ea6cc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-121">Remarks</span></span>

<span data-ttu-id="ea6cc-122">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-122">Optional.</span></span>

<span data-ttu-id="ea6cc-123">Kann höchstens einmal für jede [**Anwendung. views**](windowsribbon-element-application-views.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ea6cc-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea6cc-124">Examples</span></span>

<span data-ttu-id="ea6cc-125">Im folgenden Beispiel wird das grundlegende Markup für eine **contextpopup** -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ea6cc-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-126">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ea6cc-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="ea6cc-127">Minimum supported system</span></span><br/> | <span data-ttu-id="ea6cc-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea6cc-128">Windows 7</span></span> |
| <span data-ttu-id="ea6cc-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="ea6cc-129">Can be empty</span></span>                        | <span data-ttu-id="ea6cc-130">Nein</span><span class="sxs-lookup"><span data-stu-id="ea6cc-130">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ea6cc-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea6cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6cc-132">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ea6cc-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





