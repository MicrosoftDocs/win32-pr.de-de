---
title: Ribbon. quickaccesstoolbar (Eigenschaft)
description: Stellt einen Container für die Symbolleiste für den schnell Zugriff (QAT) dar.
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Menüband. quickaccesstoolbar-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391552"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="442c1-104">Ribbon. quickaccesstoolbar (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="442c1-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="442c1-105">Stellt einen Container für die Symbolleiste für den schnell Zugriff (QAT) dar.</span><span class="sxs-lookup"><span data-stu-id="442c1-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="442c1-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="442c1-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="442c1-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="442c1-107">Attributes</span></span>

<span data-ttu-id="442c1-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="442c1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="442c1-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="442c1-109">Child elements</span></span>



| <span data-ttu-id="442c1-110">Element</span><span class="sxs-lookup"><span data-stu-id="442c1-110">Element</span></span>                                                                           | <span data-ttu-id="442c1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="442c1-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="442c1-112">**Quickaccesstoolbar**</span><span class="sxs-lookup"><span data-stu-id="442c1-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="442c1-113">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="442c1-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="442c1-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="442c1-114">Parent elements</span></span>



| <span data-ttu-id="442c1-115">Element</span><span class="sxs-lookup"><span data-stu-id="442c1-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="442c1-116">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="442c1-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="442c1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="442c1-117">Remarks</span></span>

<span data-ttu-id="442c1-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="442c1-118">Required.</span></span>

<span data-ttu-id="442c1-119">Kann für jedes [**Menüband**](windowsribbon-element-ribbon.md)einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="442c1-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="442c1-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="442c1-120">Examples</span></span>

<span data-ttu-id="442c1-121">Das folgende Beispiel veranschaulicht das einfache Markup für das **Ribbon. quickaccesstoolbar** -Element.</span><span class="sxs-lookup"><span data-stu-id="442c1-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="442c1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="442c1-122">Requirements</span></span>



| <span data-ttu-id="442c1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="442c1-123">Requirement</span></span> | <span data-ttu-id="442c1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="442c1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="442c1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="442c1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="442c1-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="442c1-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="442c1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="442c1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="442c1-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="442c1-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





