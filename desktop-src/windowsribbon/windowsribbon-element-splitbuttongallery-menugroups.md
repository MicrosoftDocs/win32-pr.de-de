---
title: Splitbuttongallery. menugroups (Eigenschaft)
description: Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem splitbuttongallery-Steuerelement dar.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Windows-Menüband "splitbuttongallery. menugroups"
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103641"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="06bc5-104">Splitbuttongallery. menugroups (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06bc5-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="06bc5-105">Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="06bc5-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="06bc5-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="06bc5-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="06bc5-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="06bc5-107">Attributes</span></span>

<span data-ttu-id="06bc5-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="06bc5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="06bc5-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06bc5-109">Child elements</span></span>



| <span data-ttu-id="06bc5-110">Element</span><span class="sxs-lookup"><span data-stu-id="06bc5-110">Element</span></span>                                                         | <span data-ttu-id="06bc5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06bc5-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="06bc5-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="06bc5-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="06bc5-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="06bc5-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="06bc5-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06bc5-114">Parent elements</span></span>



| <span data-ttu-id="06bc5-115">Element</span><span class="sxs-lookup"><span data-stu-id="06bc5-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="06bc5-116">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="06bc5-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="06bc5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06bc5-117">Remarks</span></span>

<span data-ttu-id="06bc5-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06bc5-118">Required.</span></span>

<span data-ttu-id="06bc5-119">Muss für jedes [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="06bc5-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="06bc5-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06bc5-120">Examples</span></span>

<span data-ttu-id="06bc5-121">Im folgenden Beispiel wird das grundlegende Markup für das **splitbuttongallery. menugroups** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="06bc5-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="06bc5-122">In diesem Code Abschnitt wird die Deklaration des **splitbuttongallery. menugroups** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="06bc5-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="06bc5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06bc5-123">Requirements</span></span>



| <span data-ttu-id="06bc5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06bc5-124">Requirement</span></span> | <span data-ttu-id="06bc5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="06bc5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="06bc5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06bc5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06bc5-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06bc5-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="06bc5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06bc5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06bc5-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06bc5-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06bc5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06bc5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bc5-131">Steuerelement "Split Button Gallery"</span><span class="sxs-lookup"><span data-stu-id="06bc5-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="06bc5-132">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="06bc5-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





