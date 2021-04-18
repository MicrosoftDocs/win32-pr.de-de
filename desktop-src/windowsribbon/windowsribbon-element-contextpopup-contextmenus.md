---
title: Contextpopup. ContextMenus (Eigenschaft)
description: Stellt einen Container für ContextMenu-Elemente dar.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- Contextpopup. ContextMenus-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343466"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="5a291-104">Contextpopup. ContextMenus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a291-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="5a291-105">Stellt einen Container für [**ContextMenu**](windowsribbon-element-contextmenu.md) -Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="5a291-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="5a291-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="5a291-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="5a291-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a291-107">Attributes</span></span>

<span data-ttu-id="5a291-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="5a291-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5a291-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a291-109">Child elements</span></span>



| <span data-ttu-id="5a291-110">Element</span><span class="sxs-lookup"><span data-stu-id="5a291-110">Element</span></span>                                                             | <span data-ttu-id="5a291-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a291-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5a291-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="5a291-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="5a291-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="5a291-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5a291-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a291-114">Parent elements</span></span>



| <span data-ttu-id="5a291-115">Element</span><span class="sxs-lookup"><span data-stu-id="5a291-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="5a291-116">**Contextpopup**</span><span class="sxs-lookup"><span data-stu-id="5a291-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5a291-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a291-117">Remarks</span></span>

<span data-ttu-id="5a291-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5a291-118">Optional.</span></span>

<span data-ttu-id="5a291-119">Kann höchstens einmal für jedes [**contextpopup**](windowsribbon-element-contextpopup.md)vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5a291-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a291-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a291-120">Examples</span></span>

<span data-ttu-id="5a291-121">Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5a291-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="5a291-122">Dieser Code Abschnitt zeigt eine **contextpopup. ContextMenus** -Steuerelement Deklaration.</span><span class="sxs-lookup"><span data-stu-id="5a291-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5a291-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a291-123">Requirements</span></span>



| <span data-ttu-id="5a291-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a291-124">Requirement</span></span> | <span data-ttu-id="5a291-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5a291-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5a291-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a291-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a291-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a291-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5a291-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a291-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a291-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a291-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a291-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a291-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a291-131">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5a291-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





