---
title: SplitButton. menugroups (Eigenschaft)
description: Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem Standard Steuerelement für eine unterteilte Schaltfläche dar.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Fenster "SplitButton. menugroups"-Eigenschaft (Fenster)
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741464"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="a8aeb-104">SplitButton. menugroups (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8aeb-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="a8aeb-105">Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem Standard Steuerelement für eine unter [teilte Schaltfläche](windowsribbon-controls-splitbutton.md) dar.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a8aeb-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a8aeb-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="a8aeb-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8aeb-107">Attributes</span></span>

<span data-ttu-id="a8aeb-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8aeb-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8aeb-109">Child elements</span></span>



| <span data-ttu-id="a8aeb-110">Element</span><span class="sxs-lookup"><span data-stu-id="a8aeb-110">Element</span></span>                                                         | <span data-ttu-id="a8aeb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8aeb-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="a8aeb-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a8aeb-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="a8aeb-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a8aeb-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a8aeb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8aeb-114">Parent elements</span></span>



| <span data-ttu-id="a8aeb-115">Element</span><span class="sxs-lookup"><span data-stu-id="a8aeb-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="a8aeb-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a8aeb-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a8aeb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8aeb-117">Remarks</span></span>

<span data-ttu-id="a8aeb-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-118">Optional.</span></span>

<span data-ttu-id="a8aeb-119">Kann höchstens einmal für jedes [**SplitButton-Objekt**](windowsribbon-element-splitbutton.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8aeb-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8aeb-120">Examples</span></span>

<span data-ttu-id="a8aeb-121">Im folgenden Beispiel wird das grundlegende Markup für die [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="a8aeb-122">Dieser Code Abschnitt zeigt die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. menugroups** mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="a8aeb-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="a8aeb-123">Dieser Code Abschnitt zeigt die Steuer Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. menugroups** .</span><span class="sxs-lookup"><span data-stu-id="a8aeb-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a8aeb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8aeb-124">Requirements</span></span>



| <span data-ttu-id="a8aeb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8aeb-125">Requirement</span></span> | <span data-ttu-id="a8aeb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a8aeb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a8aeb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8aeb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a8aeb-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8aeb-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a8aeb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8aeb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a8aeb-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8aeb-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8aeb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8aeb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8aeb-132">Steuerelement "Split Button</span><span class="sxs-lookup"><span data-stu-id="a8aeb-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





