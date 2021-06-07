---
title: ContextPopup-Element
description: Stellt das Kontextpopup-Steuerelement in der ContextPopup-Ansicht dar.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- ContextPopup-Element im Windows-Menüband
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f779b0196d14fb42246c2a10d476352d835b6cf8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443463"
---
# <a name="contextpopup-element"></a><span data-ttu-id="54fdd-104">ContextPopup-Element</span><span class="sxs-lookup"><span data-stu-id="54fdd-104">ContextPopup element</span></span>

<span data-ttu-id="54fdd-105">Stellt das [Kontextpopup-Steuerelement](windowsribbon-controls-contextpopup.md) in der ContextPopup-Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="54fdd-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="54fdd-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="54fdd-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="54fdd-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="54fdd-107">Attributes</span></span>

<span data-ttu-id="54fdd-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="54fdd-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="54fdd-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54fdd-109">Child elements</span></span>



| <span data-ttu-id="54fdd-110">Element</span><span class="sxs-lookup"><span data-stu-id="54fdd-110">Element</span></span>                                                                                         | <span data-ttu-id="54fdd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54fdd-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="54fdd-112">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="54fdd-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="54fdd-113">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="54fdd-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="54fdd-114">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="54fdd-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="54fdd-115">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="54fdd-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="54fdd-116">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="54fdd-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="54fdd-117">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="54fdd-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="54fdd-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54fdd-118">Parent elements</span></span>



| <span data-ttu-id="54fdd-119">Element</span><span class="sxs-lookup"><span data-stu-id="54fdd-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="54fdd-120">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="54fdd-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="54fdd-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54fdd-121">Remarks</span></span>

<span data-ttu-id="54fdd-122">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="54fdd-122">Optional.</span></span>

<span data-ttu-id="54fdd-123">Kann für jede [**Application.Views--Anwendung mindestens einmal auftreten.**](windowsribbon-element-application-views.md)</span><span class="sxs-lookup"><span data-stu-id="54fdd-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54fdd-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54fdd-124">Examples</span></span>

<span data-ttu-id="54fdd-125">Im folgenden Beispiel wird das grundlegende Markup für eine **ContextPopup-Ansicht** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="54fdd-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="54fdd-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54fdd-126">Element information</span></span>

* <span data-ttu-id="54fdd-127">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="54fdd-127">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="54fdd-128">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="54fdd-128">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="54fdd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54fdd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fdd-130">Kontext-Popup-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="54fdd-130">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





