---
title: ContextMenu-Element
description: Stellt ein Kontextmenüsteuerelement dar.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- ContextMenu-Element Windows-Menüband
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 916a031ed642a76fb22ecc58dbbe1ce29cbcd105
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443468"
---
# <a name="contextmenu-element"></a><span data-ttu-id="661e2-104">ContextMenu-Element</span><span class="sxs-lookup"><span data-stu-id="661e2-104">ContextMenu element</span></span>

<span data-ttu-id="661e2-105">Stellt ein Kontextmenüsteuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="661e2-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="661e2-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="661e2-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="661e2-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="661e2-107">Attributes</span></span>



| <span data-ttu-id="661e2-108">attribute</span><span class="sxs-lookup"><span data-stu-id="661e2-108">Attribute</span></span>           | <span data-ttu-id="661e2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="661e2-109">Type</span></span>                 | <span data-ttu-id="661e2-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="661e2-110">Required</span></span>       | <span data-ttu-id="661e2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661e2-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="661e2-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="661e2-112">**Name**</span></span><br/> | <span data-ttu-id="661e2-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="661e2-113">xs:string</span></span><br/> | <span data-ttu-id="661e2-114">Ja</span><span class="sxs-lookup"><span data-stu-id="661e2-114">Yes</span></span><br/> | <span data-ttu-id="661e2-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="661e2-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="661e2-116">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="661e2-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="661e2-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="661e2-117">Child elements</span></span>



| <span data-ttu-id="661e2-118">Element</span><span class="sxs-lookup"><span data-stu-id="661e2-118">Element</span></span>                                                         | <span data-ttu-id="661e2-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661e2-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="661e2-120">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="661e2-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="661e2-121">Muss mindestens einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="661e2-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="661e2-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="661e2-122">Parent elements</span></span>



| <span data-ttu-id="661e2-123">Element</span><span class="sxs-lookup"><span data-stu-id="661e2-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="661e2-124">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="661e2-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="661e2-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="661e2-125">Remarks</span></span>

<span data-ttu-id="661e2-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="661e2-126">Optional.</span></span>

<span data-ttu-id="661e2-127">Kann ein oder mehrere Male für jede [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="661e2-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="661e2-128">**Ein ContextMenu** kann keine [Kombinationsfeld-](windowsribbon-controls-combobox.md) oder [Spinner-Steuerelemente](windowsribbon-controls-spinner.md) hosten.</span><span class="sxs-lookup"><span data-stu-id="661e2-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="661e2-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="661e2-129">Examples</span></span>

<span data-ttu-id="661e2-130">Im folgenden Beispiel wird das grundlegende Markup für eine [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="661e2-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="661e2-131">Dieser Codeabschnitt zeigt einen Satz von **ContextMenu-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="661e2-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="661e2-132">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="661e2-132">Element information</span></span>

* <span data-ttu-id="661e2-133">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="661e2-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="661e2-134">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="661e2-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="661e2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="661e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661e2-136">Kontext-Popup-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="661e2-136">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





