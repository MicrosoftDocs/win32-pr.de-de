---
title: Inribbongallery. menugroups (Eigenschaft)
description: Stellt einen Container für die Dropdown Menü Elemente eines In-Ribbon-Katalog Steuer Elements dar.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Inribbongallery. menugroups-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040668"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="d87ae-104">Inribbongallery. menugroups (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d87ae-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="d87ae-105">Stellt einen Container für den Satz von Dropdown-Menü Elementen eines [in-Ribbon Gallery-](windowsribbon-controls-inribbongallery.md) Steuer Elements dar.</span><span class="sxs-lookup"><span data-stu-id="d87ae-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="d87ae-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d87ae-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="d87ae-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d87ae-107">Attributes</span></span>

<span data-ttu-id="d87ae-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d87ae-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d87ae-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d87ae-109">Child elements</span></span>



| <span data-ttu-id="d87ae-110">Element</span><span class="sxs-lookup"><span data-stu-id="d87ae-110">Element</span></span>                                                         | <span data-ttu-id="d87ae-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d87ae-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="d87ae-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d87ae-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="d87ae-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="d87ae-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d87ae-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d87ae-114">Parent elements</span></span>



| <span data-ttu-id="d87ae-115">Element</span><span class="sxs-lookup"><span data-stu-id="d87ae-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="d87ae-116">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="d87ae-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d87ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d87ae-117">Remarks</span></span>

<span data-ttu-id="d87ae-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d87ae-118">Optional.</span></span>

<span data-ttu-id="d87ae-119">Kann höchstens einmal für jedes [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="d87ae-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d87ae-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d87ae-120">Examples</span></span>

<span data-ttu-id="d87ae-121">Im folgenden Beispiel wird das grundlegende Markup für ein [in-Ribbon-](windowsribbon-controls-inribbongallery.md) Katalog Steuerelement veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d87ae-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="d87ae-122">In diesem Code Abschnitt wird die Deklaration des **inribbongallery. menugroups** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d87ae-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="d87ae-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d87ae-123">Requirements</span></span>



| <span data-ttu-id="d87ae-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d87ae-124">Requirement</span></span> | <span data-ttu-id="d87ae-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d87ae-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d87ae-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d87ae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d87ae-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d87ae-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d87ae-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d87ae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d87ae-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d87ae-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d87ae-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d87ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87ae-131">In-Ribbon Gallery-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d87ae-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="d87ae-132">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="d87ae-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="d87ae-133">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d87ae-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





