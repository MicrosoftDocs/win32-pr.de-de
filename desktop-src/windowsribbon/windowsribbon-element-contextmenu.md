---
title: ContextMenu-Element
description: Stellt ein Kontextmenü-Steuerelement dar.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Fenster "ContextMenu-Element Fenster"
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718378"
---
# <a name="contextmenu-element"></a><span data-ttu-id="8d9ee-104">ContextMenu-Element</span><span class="sxs-lookup"><span data-stu-id="8d9ee-104">ContextMenu element</span></span>

<span data-ttu-id="8d9ee-105">Stellt ein Kontextmenü-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="8d9ee-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8d9ee-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="8d9ee-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d9ee-107">Attributes</span></span>



| <span data-ttu-id="8d9ee-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="8d9ee-108">Attribute</span></span>           | <span data-ttu-id="8d9ee-109">type</span><span class="sxs-lookup"><span data-stu-id="8d9ee-109">Type</span></span>                 | <span data-ttu-id="8d9ee-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d9ee-110">Required</span></span>       | <span data-ttu-id="8d9ee-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d9ee-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9ee-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d9ee-112">**Name**</span></span><br/> | <span data-ttu-id="8d9ee-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d9ee-113">xs:string</span></span><br/> | <span data-ttu-id="8d9ee-114">Ja</span><span class="sxs-lookup"><span data-stu-id="8d9ee-114">Yes</span></span><br/> | <span data-ttu-id="8d9ee-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="8d9ee-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8d9ee-116">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="8d9ee-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d9ee-117">Child elements</span></span>



| <span data-ttu-id="8d9ee-118">Element</span><span class="sxs-lookup"><span data-stu-id="8d9ee-118">Element</span></span>                                                         | <span data-ttu-id="8d9ee-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d9ee-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8d9ee-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="8d9ee-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="8d9ee-121">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="8d9ee-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8d9ee-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d9ee-122">Parent elements</span></span>



| <span data-ttu-id="8d9ee-123">Element</span><span class="sxs-lookup"><span data-stu-id="8d9ee-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d9ee-124">**Contextpopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="8d9ee-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8d9ee-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d9ee-125">Remarks</span></span>

<span data-ttu-id="8d9ee-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-126">Optional.</span></span>

<span data-ttu-id="8d9ee-127">Kann für jedes [**contextpopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)-Objekt einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d9ee-128">Ein **ContextMenu** kann keine Kombinations [Feld](windowsribbon-controls-combobox.md) -oder [Spinner](windowsribbon-controls-spinner.md) -Steuerelemente hosten.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8d9ee-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d9ee-129">Examples</span></span>

<span data-ttu-id="8d9ee-130">Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="8d9ee-131">Dieser Code Abschnitt zeigt einen Satz von **ContextMenu** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="8d9ee-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8d9ee-132">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8d9ee-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8d9ee-133">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="8d9ee-133">Minimum supported system</span></span><br/> | <span data-ttu-id="8d9ee-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d9ee-134">Windows 7</span></span> |
| <span data-ttu-id="8d9ee-135">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="8d9ee-135">Can be empty</span></span>                        | <span data-ttu-id="8d9ee-136">Nein</span><span class="sxs-lookup"><span data-stu-id="8d9ee-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="8d9ee-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8d9ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9ee-138">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8d9ee-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





