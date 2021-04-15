---
title: SplitButton. buttonitem (Eigenschaft)
description: Stellt einen Container für eine Schaltfläche oder UMSCHALT Fläche dar, die den Standardbefehl einer unterteilten Schaltfläche verfügbar macht.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Fenster "SplitButton. buttonitem"-Eigenschaft (Fenster)
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475765"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="3d09e-104">SplitButton. buttonitem (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d09e-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="3d09e-105">Stellt einen Container für eine [Schalt](windowsribbon-controls-button.md) Fläche oder [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) dar, die den Standardbefehl einer unter [teilten Schaltfläche](windowsribbon-controls-splitbutton.md)verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3d09e-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="3d09e-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="3d09e-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="3d09e-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d09e-107">Attributes</span></span>

<span data-ttu-id="3d09e-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="3d09e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3d09e-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d09e-109">Child elements</span></span>



| <span data-ttu-id="3d09e-110">Element</span><span class="sxs-lookup"><span data-stu-id="3d09e-110">Element</span></span>                                                               | <span data-ttu-id="3d09e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d09e-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3d09e-112">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="3d09e-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="3d09e-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="3d09e-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3d09e-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3d09e-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="3d09e-115">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="3d09e-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3d09e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d09e-116">Parent elements</span></span>



| <span data-ttu-id="3d09e-117">Element</span><span class="sxs-lookup"><span data-stu-id="3d09e-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="3d09e-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3d09e-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3d09e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d09e-119">Remarks</span></span>

<span data-ttu-id="3d09e-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3d09e-120">Optional.</span></span>

<span data-ttu-id="3d09e-121">Kann höchstens einmal für jedes [**SplitButton-Objekt**](windowsribbon-element-splitbutton.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="3d09e-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="3d09e-122">Jedes **SplitButton. buttonitem** -Element darf nur ein untergeordnetes [**Schalt**](windowsribbon-element-button.md) Flächen [**-oder-**](windowsribbon-element-togglebutton.md) Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d09e-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="3d09e-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d09e-123">Examples</span></span>

<span data-ttu-id="3d09e-124">Im folgenden Beispiel wird das grundlegende Markup für die [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3d09e-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="3d09e-125">Dieser Code Abschnitt zeigt die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. buttonitem** mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="3d09e-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="3d09e-126">In diesem Code Abschnitt werden die Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. buttonitem** -Steuerelement gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d09e-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="3d09e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d09e-127">Requirements</span></span>



| <span data-ttu-id="3d09e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d09e-128">Requirement</span></span> | <span data-ttu-id="3d09e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3d09e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d09e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d09e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3d09e-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d09e-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3d09e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d09e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3d09e-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d09e-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d09e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d09e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d09e-135">Steuerelement "Split Button</span><span class="sxs-lookup"><span data-stu-id="3d09e-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





