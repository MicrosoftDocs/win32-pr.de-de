---
title: Menübandelement
description: Stellt das Menüband-Steuerelement in der Menübandansicht dar.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Menübandelement Windows-Menüband
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445001"
---
# <a name="ribbon-element"></a><span data-ttu-id="fbf00-104">Menübandelement</span><span class="sxs-lookup"><span data-stu-id="fbf00-104">Ribbon element</span></span>

<span data-ttu-id="fbf00-105">Stellt das Menüband-Steuerelement in der Menübandansicht dar.</span><span class="sxs-lookup"><span data-stu-id="fbf00-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="fbf00-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="fbf00-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="fbf00-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbf00-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbf00-108">attribute</span><span class="sxs-lookup"><span data-stu-id="fbf00-108">Attribute</span></span></th>
<th><span data-ttu-id="fbf00-109">Typ</span><span class="sxs-lookup"><span data-stu-id="fbf00-109">Type</span></span></th>
<th><span data-ttu-id="fbf00-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbf00-110">Required</span></span></th>
<th><span data-ttu-id="fbf00-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbf00-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbf00-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="fbf00-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="fbf00-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fbf00-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="fbf00-114">Nein</span><span class="sxs-lookup"><span data-stu-id="fbf00-114">No</span></span><br/></td>
<td><span data-ttu-id="fbf00-115"><dt><span></span><span></span><strong></strong> (Klein)</span><span class="sxs-lookup"><span data-stu-id="fbf00-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="fbf00-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="fbf00-116">Default.</span></span> <br/> </dd> <span data-ttu-id="fbf00-117"><dt><span></span><span></span><strong></strong> (Mittel)</span><span class="sxs-lookup"><span data-stu-id="fbf00-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="fbf00-118"><dt><span></span><span></span><strong></strong> (Groß)</span><span class="sxs-lookup"><span data-stu-id="fbf00-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbf00-119"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="fbf00-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="fbf00-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="fbf00-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="fbf00-121">Nein</span><span class="sxs-lookup"><span data-stu-id="fbf00-121">No</span></span><br/></td>
<td><span data-ttu-id="fbf00-122">Wird verwendet, um das Befehlselement zu kommentieren.</span><span class="sxs-lookup"><span data-stu-id="fbf00-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="fbf00-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="fbf00-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fbf00-124">Jede Sequenz von 0 (null) oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fbf00-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="fbf00-125">Die maximale Länge ist nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="fbf00-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fbf00-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf00-126">Child elements</span></span>



| <span data-ttu-id="fbf00-127">Element</span><span class="sxs-lookup"><span data-stu-id="fbf00-127">Element</span></span>                                                                                         | <span data-ttu-id="fbf00-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbf00-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="fbf00-129">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="fbf00-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="fbf00-130">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fbf00-131">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="fbf00-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="fbf00-132">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fbf00-133">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="fbf00-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="fbf00-134">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fbf00-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="fbf00-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="fbf00-136">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fbf00-137">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="fbf00-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="fbf00-138">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fbf00-139">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="fbf00-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="fbf00-140">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fbf00-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf00-141">Parent elements</span></span>



| <span data-ttu-id="fbf00-142">Element</span><span class="sxs-lookup"><span data-stu-id="fbf00-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="fbf00-143">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="fbf00-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fbf00-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbf00-144">Remarks</span></span>

<span data-ttu-id="fbf00-145">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fbf00-145">Required.</span></span>

<span data-ttu-id="fbf00-146">Muss für jedes [**Application.Views-Element**](windowsribbon-element-application-views.md) genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbf00-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fbf00-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbf00-147">Examples</span></span>

<span data-ttu-id="fbf00-148">Im folgenden Beispiel wird das grundlegende Markup für eine **Menübandansicht** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fbf00-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
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
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="fbf00-149">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fbf00-149">Element information</span></span>




* <span data-ttu-id="fbf00-150">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbf00-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="fbf00-151">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="fbf00-151">**Can be empty**: No</span></span>



 

 





