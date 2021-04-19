---
title: Dropdowngallery. menulayout (Eigenschaft)
description: Stellt einen Container für Dropdown Gallery-Dropdown Menü Layouts dar.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Dropdowngallery. menulayout-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346755"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="51aca-104">Dropdowngallery. menulayout (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51aca-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="51aca-105">Stellt einen Container für [**Dropdown Gallery-Dropdown**](windowsribbon-element-dropdowngallery.md) Menü Layouts dar.</span><span class="sxs-lookup"><span data-stu-id="51aca-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="51aca-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="51aca-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="51aca-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="51aca-107">Attributes</span></span>

<span data-ttu-id="51aca-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="51aca-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="51aca-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51aca-109">Child elements</span></span>



| <span data-ttu-id="51aca-110">Element</span><span class="sxs-lookup"><span data-stu-id="51aca-110">Element</span></span>                                                                           | <span data-ttu-id="51aca-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51aca-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="51aca-112">**Flowmenulayout**</span><span class="sxs-lookup"><span data-stu-id="51aca-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="51aca-113">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="51aca-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="51aca-114">**Verticalmenulayout**</span><span class="sxs-lookup"><span data-stu-id="51aca-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="51aca-115">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="51aca-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="51aca-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51aca-116">Parent elements</span></span>



| <span data-ttu-id="51aca-117">Element</span><span class="sxs-lookup"><span data-stu-id="51aca-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="51aca-118">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="51aca-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="51aca-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51aca-119">Remarks</span></span>

<span data-ttu-id="51aca-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="51aca-120">Optional.</span></span>

<span data-ttu-id="51aca-121">Kann höchstens einmal für jedes [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="51aca-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="51aca-122">Maximal ein untergeordnetes Element ([**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) oder [**flowmenulayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="51aca-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="51aca-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51aca-123">Examples</span></span>

<span data-ttu-id="51aca-124">Im folgenden Beispiel wird das grundlegende Markup für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="51aca-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="51aca-125">In diesem Code Abschnitt wird die Deklaration des **dropdowngallery. menulayout** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="51aca-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="51aca-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51aca-126">Requirements</span></span>



| <span data-ttu-id="51aca-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51aca-127">Requirement</span></span> | <span data-ttu-id="51aca-128">Wert</span><span class="sxs-lookup"><span data-stu-id="51aca-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="51aca-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51aca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51aca-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51aca-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="51aca-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51aca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51aca-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51aca-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51aca-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51aca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51aca-134">**Dropdown-Katalog-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="51aca-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="51aca-135">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="51aca-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





