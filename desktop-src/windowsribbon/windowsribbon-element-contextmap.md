---
title: ContextMap-Element
description: Stellt eine ContextMenu- und MiniToolbar-Paarzuordnung dar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- ContextMap-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754fc75ca09e39cdc7eabbeae2a0a2d2630c31f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443011"
---
# <a name="contextmap-element"></a><span data-ttu-id="fb9cf-104">ContextMap-Element</span><span class="sxs-lookup"><span data-stu-id="fb9cf-104">ContextMap element</span></span>

<span data-ttu-id="fb9cf-105">Stellt eine [**ContextMenu-**](windowsribbon-element-contextmenu.md) und [**MiniToolbar-Paarzuordnung**](windowsribbon-element-minitoolbar.md) dar.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="fb9cf-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="fb9cf-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="fb9cf-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb9cf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb9cf-108">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9cf-108">Attribute</span></span></th>
<th><span data-ttu-id="fb9cf-109">Typ</span><span class="sxs-lookup"><span data-stu-id="fb9cf-109">Type</span></span></th>
<th><span data-ttu-id="fb9cf-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb9cf-110">Required</span></span></th>
<th><span data-ttu-id="fb9cf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb9cf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb9cf-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fb9cf-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fb9cf-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="fb9cf-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fb9cf-114">Nein</span><span class="sxs-lookup"><span data-stu-id="fb9cf-114">No</span></span><br/></td>
<td><span data-ttu-id="fb9cf-115">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb9cf-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fb9cf-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="fb9cf-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fb9cf-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fb9cf-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fb9cf-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb9cf-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="fb9cf-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="fb9cf-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="fb9cf-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="fb9cf-122">Nein</span><span class="sxs-lookup"><span data-stu-id="fb9cf-122">No</span></span><br/></td>
<td><span data-ttu-id="fb9cf-123">Muss einem vorhandenen <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu-Namen</strong></a> <em>entsprechen.</em></span><span class="sxs-lookup"><span data-stu-id="fb9cf-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="fb9cf-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="fb9cf-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fb9cf-125">Eine Zeichenfolge, die aus einer beliebigen Folge von Zeichen besteht, einschließlich Leerzeichen und Zeilenumbruchzeichen.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb9cf-126"><strong>MiniToolbar</strong></span><span class="sxs-lookup"><span data-stu-id="fb9cf-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="fb9cf-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="fb9cf-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="fb9cf-128">Nein</span><span class="sxs-lookup"><span data-stu-id="fb9cf-128">No</span></span><br/></td>
<td><span data-ttu-id="fb9cf-129">Muss einem vorhandenen <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar-Namen</strong></a> <em>entsprechen.</em></span><span class="sxs-lookup"><span data-stu-id="fb9cf-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="fb9cf-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="fb9cf-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fb9cf-131">Eine Zeichenfolge, die aus einer beliebigen Folge von Zeichen besteht, einschließlich Leerzeichen und Zeilenumbruchzeichen.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fb9cf-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb9cf-132">Child elements</span></span>

<span data-ttu-id="fb9cf-133">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fb9cf-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb9cf-134">Parent elements</span></span>



| <span data-ttu-id="fb9cf-135">Element</span><span class="sxs-lookup"><span data-stu-id="fb9cf-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb9cf-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="fb9cf-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fb9cf-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb9cf-137">Remarks</span></span>

<span data-ttu-id="fb9cf-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-138">Optional.</span></span>

<span data-ttu-id="fb9cf-139">Kann ein oder mehrere Male für jedes [**ContextPopup.ContextMaps-Objekt auftreten.**](windowsribbon-element-contextpopup-contextmaps.md)</span><span class="sxs-lookup"><span data-stu-id="fb9cf-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb9cf-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb9cf-140">Examples</span></span>

<span data-ttu-id="fb9cf-141">Im folgenden Beispiel wird das grundlegende Markup für eine [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fb9cf-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="fb9cf-142">Dieser Codeabschnitt zeigt eine Reihe von **ContextMap-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="fb9cf-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="fb9cf-143">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fb9cf-143">Element information</span></span>


* <span data-ttu-id="fb9cf-144">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb9cf-144">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="fb9cf-145">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="fb9cf-145">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="fb9cf-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb9cf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9cf-147">Kontext-Popup-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fb9cf-147">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





