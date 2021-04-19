---
title: Ribbon-Element
description: Stellt das Menüband-Steuerelement in der Menü Band Ansicht dar.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Menüband Element Windows-Menüband
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342312"
---
# <a name="ribbon-element"></a><span data-ttu-id="a2df8-104">Ribbon-Element</span><span class="sxs-lookup"><span data-stu-id="a2df8-104">Ribbon element</span></span>

<span data-ttu-id="a2df8-105">Stellt das Menüband-Steuerelement in der Menü Band Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="a2df8-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="a2df8-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a2df8-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="a2df8-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="a2df8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2df8-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="a2df8-108">Attribute</span></span></th>
<th><span data-ttu-id="a2df8-109">type</span><span class="sxs-lookup"><span data-stu-id="a2df8-109">Type</span></span></th>
<th><span data-ttu-id="a2df8-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a2df8-110">Required</span></span></th>
<th><span data-ttu-id="a2df8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2df8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a2df8-112"><strong>Groupspacing</strong></span><span class="sxs-lookup"><span data-stu-id="a2df8-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="a2df8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2df8-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="a2df8-114">Nein</span><span class="sxs-lookup"><span data-stu-id="a2df8-114">No</span></span><br/></td>
<td><span data-ttu-id="a2df8-115"><dt><span></span><span></span><strong></strong> Zuletzt</span><span class="sxs-lookup"><span data-stu-id="a2df8-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="a2df8-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="a2df8-116">Default.</span></span> <br/> </dd> <span data-ttu-id="a2df8-117"><dt><span></span><span></span><strong></strong> Mittelalter</span><span class="sxs-lookup"><span data-stu-id="a2df8-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a2df8-118"><dt><span></span><span></span><strong></strong> Viele</span><span class="sxs-lookup"><span data-stu-id="a2df8-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2df8-119"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="a2df8-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="a2df8-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2df8-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="a2df8-121">Nein</span><span class="sxs-lookup"><span data-stu-id="a2df8-121">No</span></span><br/></td>
<td><span data-ttu-id="a2df8-122">Wird verwendet, um das Command-Element mit Anmerkungen zu versehen.</span><span class="sxs-lookup"><span data-stu-id="a2df8-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="a2df8-123">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="a2df8-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a2df8-124">Eine beliebige Sequenz von NULL oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a2df8-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="a2df8-125">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="a2df8-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a2df8-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2df8-126">Child elements</span></span>



| <span data-ttu-id="a2df8-127">Element</span><span class="sxs-lookup"><span data-stu-id="a2df8-127">Element</span></span>                                                                                         | <span data-ttu-id="a2df8-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2df8-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a2df8-129">**Menü Band. applicationmenu**</span><span class="sxs-lookup"><span data-stu-id="a2df8-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="a2df8-130">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a2df8-131">**Menüband. contextualtabs**</span><span class="sxs-lookup"><span data-stu-id="a2df8-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="a2df8-132">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a2df8-133">**Menüband. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="a2df8-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="a2df8-134">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a2df8-135">**Menüband. quickaccesstoolbar**</span><span class="sxs-lookup"><span data-stu-id="a2df8-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="a2df8-136">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a2df8-137">**Ribbon. sizedefinitions**</span><span class="sxs-lookup"><span data-stu-id="a2df8-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="a2df8-138">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a2df8-139">**Menüband. Registerkarten**</span><span class="sxs-lookup"><span data-stu-id="a2df8-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="a2df8-140">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="a2df8-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a2df8-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2df8-141">Parent elements</span></span>



| <span data-ttu-id="a2df8-142">Element</span><span class="sxs-lookup"><span data-stu-id="a2df8-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="a2df8-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="a2df8-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a2df8-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2df8-144">Remarks</span></span>

<span data-ttu-id="a2df8-145">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2df8-145">Required.</span></span>

<span data-ttu-id="a2df8-146">Muss für jedes [**Application. views**](windowsribbon-element-application-views.md) -Element genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="a2df8-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a2df8-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2df8-147">Examples</span></span>

<span data-ttu-id="a2df8-148">Im folgenden Beispiel wird das grundlegende Markup für eine Menü **Band** Ansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a2df8-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a2df8-149">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a2df8-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a2df8-150">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="a2df8-150">Minimum supported system</span></span><br/> | <span data-ttu-id="a2df8-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2df8-151">Windows 7</span></span> |
| <span data-ttu-id="a2df8-152">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="a2df8-152">Can be empty</span></span>                        | <span data-ttu-id="a2df8-153">Nein</span><span class="sxs-lookup"><span data-stu-id="a2df8-153">No</span></span>        |



 

 





