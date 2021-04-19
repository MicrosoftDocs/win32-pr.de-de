---
title: Dropdowngallery. menugroups (Eigenschaft)
description: Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem Drop-Down-Katalog Steuerelement dar.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Dropdowngallery. menugroups-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346756"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="68646-104">Dropdowngallery. menugroups (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68646-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="68646-105">Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="68646-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="68646-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="68646-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="68646-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="68646-107">Attributes</span></span>

<span data-ttu-id="68646-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="68646-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="68646-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68646-109">Child elements</span></span>



| <span data-ttu-id="68646-110">Element</span><span class="sxs-lookup"><span data-stu-id="68646-110">Element</span></span>                                                         | <span data-ttu-id="68646-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68646-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="68646-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="68646-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="68646-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="68646-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="68646-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68646-114">Parent elements</span></span>



| <span data-ttu-id="68646-115">Element</span><span class="sxs-lookup"><span data-stu-id="68646-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="68646-116">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="68646-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="68646-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68646-117">Remarks</span></span>

<span data-ttu-id="68646-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68646-118">Required.</span></span>

<span data-ttu-id="68646-119">Muss für jedes [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) -Element genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="68646-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="68646-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68646-120">Examples</span></span>

<span data-ttu-id="68646-121">Im folgenden Beispiel wird das grundlegende Markup für das **dropdowngallery. menugroups** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="68646-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="68646-122">In diesem Code Abschnitt wird die Deklaration des **dropdowngallery. menugroups** -Steuer Elements in einem [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Befehlsbereich veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="68646-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="68646-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68646-123">Requirements</span></span>



| <span data-ttu-id="68646-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68646-124">Requirement</span></span> | <span data-ttu-id="68646-125">Wert</span><span class="sxs-lookup"><span data-stu-id="68646-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="68646-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68646-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68646-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68646-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="68646-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68646-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68646-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68646-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68646-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68646-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68646-131">**Dropdown-Katalog-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="68646-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="68646-132">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="68646-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





