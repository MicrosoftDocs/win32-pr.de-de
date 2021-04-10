---
title: Inribbongallery. menulayout (Eigenschaft)
description: Stellt einen Container für In-Ribbon Katalog-Dropdown Menü Layouts dar.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Inribbongallery. menulayout-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040192"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="3c0c9-104">Inribbongallery. menulayout (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c0c9-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="3c0c9-105">Stellt einen Container für [in-Ribbon-](windowsribbon-controls-inribbongallery.md) Katalog-Dropdown Menü Layouts dar.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="3c0c9-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="3c0c9-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="3c0c9-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c0c9-107">Attributes</span></span>

<span data-ttu-id="3c0c9-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3c0c9-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c0c9-109">Child elements</span></span>



| <span data-ttu-id="3c0c9-110">Element</span><span class="sxs-lookup"><span data-stu-id="3c0c9-110">Element</span></span>                                                                           | <span data-ttu-id="3c0c9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c0c9-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="3c0c9-112">**Flowmenulayout**</span><span class="sxs-lookup"><span data-stu-id="3c0c9-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="3c0c9-113">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="3c0c9-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="3c0c9-114">**Verticalmenulayout**</span><span class="sxs-lookup"><span data-stu-id="3c0c9-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="3c0c9-115">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="3c0c9-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3c0c9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c0c9-116">Parent elements</span></span>



| <span data-ttu-id="3c0c9-117">Element</span><span class="sxs-lookup"><span data-stu-id="3c0c9-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3c0c9-118">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="3c0c9-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3c0c9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c0c9-119">Remarks</span></span>

<span data-ttu-id="3c0c9-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-120">Optional.</span></span>

<span data-ttu-id="3c0c9-121">Kann höchstens einmal für jedes [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="3c0c9-122">Maximal ein untergeordnetes Element ([**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) oder [**flowmenulayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3c0c9-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c0c9-123">Examples</span></span>

<span data-ttu-id="3c0c9-124">Im folgenden Beispiel wird das grundlegende Markup für den [in-Ribbon-](windowsribbon-controls-inribbongallery.md)Katalog veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="3c0c9-125">In diesem Code Abschnitt wird die Deklaration des **inribbongallery. menulayout** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3c0c9-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3c0c9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c0c9-126">Requirements</span></span>



| <span data-ttu-id="3c0c9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c0c9-127">Requirement</span></span> | <span data-ttu-id="3c0c9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3c0c9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3c0c9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c0c9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0c9-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c0c9-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3c0c9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c0c9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0c9-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c0c9-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c0c9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c0c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0c9-134">In-Ribbon Gallery-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3c0c9-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="3c0c9-135">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="3c0c9-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





