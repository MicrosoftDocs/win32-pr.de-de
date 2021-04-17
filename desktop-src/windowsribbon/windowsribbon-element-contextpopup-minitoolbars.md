---
title: Contextpopup. minitoolbars (Eigenschaft)
description: Stellt einen Container für MiniToolbar-Elemente dar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Contextpopup. minitoolbars-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478609"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="7f926-104">Contextpopup. minitoolbars (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7f926-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="7f926-105">Stellt einen Container für [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="7f926-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="7f926-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7f926-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="7f926-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f926-107">Attributes</span></span>

<span data-ttu-id="7f926-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7f926-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7f926-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f926-109">Child elements</span></span>



| <span data-ttu-id="7f926-110">Element</span><span class="sxs-lookup"><span data-stu-id="7f926-110">Element</span></span>                                                             | <span data-ttu-id="7f926-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f926-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7f926-112">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="7f926-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="7f926-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="7f926-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7f926-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f926-114">Parent elements</span></span>



| <span data-ttu-id="7f926-115">Element</span><span class="sxs-lookup"><span data-stu-id="7f926-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="7f926-116">**Contextpopup**</span><span class="sxs-lookup"><span data-stu-id="7f926-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7f926-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f926-117">Remarks</span></span>

<span data-ttu-id="7f926-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="7f926-118">Optional.</span></span>

<span data-ttu-id="7f926-119">Kann höchstens einmal für jedes [**contextpopup**](windowsribbon-element-contextpopup.md)vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7f926-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="7f926-120">Da Steuerelemente in der [**MiniToolbar**](windowsribbon-element-minitoolbar.md) nicht auf Tastatur zugänglich sind, sollten die von Ihnen verfügbar gemachten Befehle an anderer Stelle in der Multifunktionsleisten-Benutzeroberfläche verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="7f926-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="7f926-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f926-121">Examples</span></span>

<span data-ttu-id="7f926-122">Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7f926-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="7f926-123">In diesem Code Abschnitt wird die **contextpopup. minitoolbars** -Steuerelement Deklaration gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f926-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7f926-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f926-124">Requirements</span></span>



| <span data-ttu-id="7f926-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f926-125">Requirement</span></span> | <span data-ttu-id="7f926-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7f926-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7f926-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f926-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f926-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f926-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7f926-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f926-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f926-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f926-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f926-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f926-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f926-132">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7f926-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





