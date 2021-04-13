---
title: Ribbon. Tabs (Eigenschaft)
description: Stellt einen Container für alle Kern Registerkarten in einem Menüband dar.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Menüband. Registerkarten-Eigenschaften Fenster
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475417"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="84783-104">Ribbon. Tabs (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="84783-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="84783-105">Stellt einen Container für alle Kern Registerkarten in einem Menüband dar.</span><span class="sxs-lookup"><span data-stu-id="84783-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="84783-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="84783-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="84783-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="84783-107">Attributes</span></span>

<span data-ttu-id="84783-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="84783-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="84783-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84783-109">Child elements</span></span>



| <span data-ttu-id="84783-110">Element</span><span class="sxs-lookup"><span data-stu-id="84783-110">Element</span></span>                                             | <span data-ttu-id="84783-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84783-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="84783-112">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="84783-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="84783-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="84783-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="84783-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84783-114">Parent elements</span></span>



| <span data-ttu-id="84783-115">Element</span><span class="sxs-lookup"><span data-stu-id="84783-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="84783-116">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="84783-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="84783-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84783-117">Remarks</span></span>

<span data-ttu-id="84783-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="84783-118">Required.</span></span>

<span data-ttu-id="84783-119">Kann für jedes [**Menüband**](windowsribbon-element-ribbon.md)einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="84783-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="84783-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84783-120">Examples</span></span>

<span data-ttu-id="84783-121">Das folgende Beispiel veranschaulicht das einfache Markup für ein **Ribbon. Tabs** -Element mit einer Registerkarten Deklaration der [**Registerkarte**](windowsribbon-element-tab.md) **Home** .</span><span class="sxs-lookup"><span data-stu-id="84783-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a><span data-ttu-id="84783-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84783-122">Requirements</span></span>



| <span data-ttu-id="84783-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84783-123">Requirement</span></span> | <span data-ttu-id="84783-124">Wert</span><span class="sxs-lookup"><span data-stu-id="84783-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="84783-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84783-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84783-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84783-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="84783-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84783-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84783-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84783-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84783-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84783-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84783-130">**Menüband. contextualtabs**</span><span class="sxs-lookup"><span data-stu-id="84783-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





