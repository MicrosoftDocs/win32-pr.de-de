---
title: Ribbon. applicationmenu (Eigenschaft)
description: Stellt das Anwendungsmenü dar. | Ribbon. applicationmenu (Eigenschaft)
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Menüband. applicationmenu-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357212"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="f29e2-105">Ribbon. applicationmenu (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f29e2-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="f29e2-106">Stellt das Anwendungsmenü dar.</span><span class="sxs-lookup"><span data-stu-id="f29e2-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="f29e2-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f29e2-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="f29e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f29e2-108">Attributes</span></span>

<span data-ttu-id="f29e2-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="f29e2-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f29e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f29e2-110">Child elements</span></span>



| <span data-ttu-id="f29e2-111">Element</span><span class="sxs-lookup"><span data-stu-id="f29e2-111">Element</span></span>                                                                     | <span data-ttu-id="f29e2-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f29e2-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="f29e2-113">**Applicationmenu**</span><span class="sxs-lookup"><span data-stu-id="f29e2-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="f29e2-114">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="f29e2-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f29e2-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f29e2-115">Parent elements</span></span>



| <span data-ttu-id="f29e2-116">Element</span><span class="sxs-lookup"><span data-stu-id="f29e2-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="f29e2-117">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="f29e2-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f29e2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f29e2-118">Remarks</span></span>

<span data-ttu-id="f29e2-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f29e2-119">Required.</span></span>

<span data-ttu-id="f29e2-120">Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="f29e2-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f29e2-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f29e2-121">Examples</span></span>

<span data-ttu-id="f29e2-122">Im folgenden Beispiel wird das grundlegende Markup für das **Ribbon. applicationmenu** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f29e2-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="f29e2-123">In diesem Code Abschnitt wird die Deklaration des **Ribbon. applicationmenu** -Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f29e2-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="f29e2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f29e2-124">Requirements</span></span>



| <span data-ttu-id="f29e2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f29e2-125">Requirement</span></span> | <span data-ttu-id="f29e2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f29e2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f29e2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f29e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f29e2-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f29e2-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f29e2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f29e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f29e2-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f29e2-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





