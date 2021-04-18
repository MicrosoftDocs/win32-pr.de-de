---
title: Application. views (Eigenschaft)
description: Stellt einen Container für jede Menüband-frameworkansicht dar, insbesondere das Menüband und das contextpopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Application. views-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339970"
---
# <a name="applicationviews-property"></a><span data-ttu-id="9acc1-104">Application. views (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9acc1-104">Application.Views property</span></span>

<span data-ttu-id="9acc1-105">Stellt einen Container für jede Menüband-frameworkansicht dar, insbesondere das [**Menüband**](windowsribbon-element-ribbon.md) und das [**contextpopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="9acc1-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="9acc1-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9acc1-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="9acc1-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="9acc1-107">Attributes</span></span>

<span data-ttu-id="9acc1-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9acc1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9acc1-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9acc1-109">Child elements</span></span>



| <span data-ttu-id="9acc1-110">Element</span><span class="sxs-lookup"><span data-stu-id="9acc1-110">Element</span></span>                                                               | <span data-ttu-id="9acc1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9acc1-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9acc1-112">**Contextpopup**</span><span class="sxs-lookup"><span data-stu-id="9acc1-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="9acc1-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="9acc1-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="9acc1-114">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="9acc1-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="9acc1-115">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="9acc1-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="9acc1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9acc1-116">Parent elements</span></span>



| <span data-ttu-id="9acc1-117">Element</span><span class="sxs-lookup"><span data-stu-id="9acc1-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="9acc1-118">**Application**</span><span class="sxs-lookup"><span data-stu-id="9acc1-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9acc1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9acc1-119">Remarks</span></span>

<span data-ttu-id="9acc1-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9acc1-120">Required.</span></span>

<span data-ttu-id="9acc1-121">Muss für jedes [**Anwendungs**](windowsribbon-element-application.md) Element genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="9acc1-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9acc1-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9acc1-122">Examples</span></span>

<span data-ttu-id="9acc1-123">Das folgende Beispiel zeigt ein **Application. views** -Element, das ein Manifest von Menü Band Steuerelementen enthält, die jeweils über einen Verweis auf einen Befehl verfügen, der im [**Application. Commands**](windowsribbon-element-application-commands.md) -Element deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="9acc1-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="9acc1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9acc1-124">Requirements</span></span>



| <span data-ttu-id="9acc1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9acc1-125">Requirement</span></span> | <span data-ttu-id="9acc1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9acc1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9acc1-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9acc1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9acc1-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9acc1-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9acc1-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9acc1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9acc1-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9acc1-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9acc1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9acc1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9acc1-132">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="9acc1-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





