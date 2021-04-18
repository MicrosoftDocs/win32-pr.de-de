---
title: Contextmap-Element
description: Stellt eine ContextMenu-und MiniToolbar-paar Zuordnung dar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Windows-Menüband für contextmap-Element
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2ddcc8bdea16f5e00974b2b2e58934941e44c68
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340681"
---
# <a name="contextmap-element"></a><span data-ttu-id="93023-104">Contextmap-Element</span><span class="sxs-lookup"><span data-stu-id="93023-104">ContextMap element</span></span>

<span data-ttu-id="93023-105">Stellt eine [**ContextMenu**](windowsribbon-element-contextmenu.md) -und [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -paar Zuordnung dar.</span><span class="sxs-lookup"><span data-stu-id="93023-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="93023-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="93023-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="93023-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="93023-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93023-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="93023-108">Attribute</span></span></th>
<th><span data-ttu-id="93023-109">type</span><span class="sxs-lookup"><span data-stu-id="93023-109">Type</span></span></th>
<th><span data-ttu-id="93023-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="93023-110">Required</span></span></th>
<th><span data-ttu-id="93023-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93023-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93023-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="93023-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="93023-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="93023-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="93023-114">Nein</span><span class="sxs-lookup"><span data-stu-id="93023-114">No</span></span><br/></td>
<td><span data-ttu-id="93023-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="93023-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="93023-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="93023-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="93023-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="93023-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="93023-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="93023-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="93023-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="93023-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93023-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="93023-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="93023-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="93023-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="93023-122">Nein</span><span class="sxs-lookup"><span data-stu-id="93023-122">No</span></span><br/></td>
<td><span data-ttu-id="93023-123">Muss einem vorhandenen <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> - <em>Namen</em>entsprechen.</span><span class="sxs-lookup"><span data-stu-id="93023-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="93023-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="93023-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="93023-125">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="93023-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93023-126"><strong>MiniToolbar</strong></span><span class="sxs-lookup"><span data-stu-id="93023-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="93023-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="93023-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="93023-128">Nein</span><span class="sxs-lookup"><span data-stu-id="93023-128">No</span></span><br/></td>
<td><span data-ttu-id="93023-129">Muss einem vorhandenen <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> - <em>Namen</em>entsprechen.</span><span class="sxs-lookup"><span data-stu-id="93023-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="93023-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="93023-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="93023-131">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="93023-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="93023-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93023-132">Child elements</span></span>

<span data-ttu-id="93023-133">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="93023-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="93023-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93023-134">Parent elements</span></span>



| <span data-ttu-id="93023-135">Element</span><span class="sxs-lookup"><span data-stu-id="93023-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93023-136">**Contextpopup. contextmaps**</span><span class="sxs-lookup"><span data-stu-id="93023-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="93023-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93023-137">Remarks</span></span>

<span data-ttu-id="93023-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="93023-138">Optional.</span></span>

<span data-ttu-id="93023-139">Kann für jede " [**contextpopup. contextmaps**](windowsribbon-element-contextpopup-contextmaps.md)" einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="93023-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="93023-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93023-140">Examples</span></span>

<span data-ttu-id="93023-141">Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="93023-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="93023-142">Dieser Code Abschnitt zeigt einen Satz von **contextmap** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="93023-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="93023-143">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="93023-143">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="93023-144">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="93023-144">Minimum supported system</span></span><br/> | <span data-ttu-id="93023-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93023-145">Windows 7</span></span> |
| <span data-ttu-id="93023-146">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="93023-146">Can be empty</span></span>                        | <span data-ttu-id="93023-147">Ja</span><span class="sxs-lookup"><span data-stu-id="93023-147">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="93023-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93023-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93023-149">Kontext-Popup Steuerelement</span><span class="sxs-lookup"><span data-stu-id="93023-149">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





