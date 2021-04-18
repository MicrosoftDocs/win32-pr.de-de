---
title: Applicationmenu. recentitems (Eigenschaft)
description: Stellt einen Container für das Steuerelement "zuletzt verwendete Elemente" im Anwendungsmenü dar.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Applicationmenu. recentitems-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391947"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="c9bfa-104">Applicationmenu. recentitems (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c9bfa-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="c9bfa-105">Stellt einen Container für das Steuerelement " [zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) " im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="c9bfa-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c9bfa-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="c9bfa-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9bfa-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9bfa-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="c9bfa-108">Attribute</span></span></th>
<th><span data-ttu-id="c9bfa-109">type</span><span class="sxs-lookup"><span data-stu-id="c9bfa-109">Type</span></span></th>
<th><span data-ttu-id="c9bfa-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c9bfa-110">Required</span></span></th>
<th><span data-ttu-id="c9bfa-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9bfa-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9bfa-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c9bfa-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c9bfa-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="c9bfa-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c9bfa-114">Nein</span><span class="sxs-lookup"><span data-stu-id="c9bfa-114">No</span></span><br/></td>
<td><span data-ttu-id="c9bfa-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c9bfa-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="c9bfa-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c9bfa-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="c9bfa-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c9bfa-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c9bfa-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c9bfa-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9bfa-120">Child elements</span></span>



| <span data-ttu-id="c9bfa-121">Element</span><span class="sxs-lookup"><span data-stu-id="c9bfa-121">Element</span></span>                                                             | <span data-ttu-id="c9bfa-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9bfa-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="c9bfa-123">**"Recentitems"**</span><span class="sxs-lookup"><span data-stu-id="c9bfa-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="c9bfa-124">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="c9bfa-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c9bfa-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9bfa-125">Parent elements</span></span>



| <span data-ttu-id="c9bfa-126">Element</span><span class="sxs-lookup"><span data-stu-id="c9bfa-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="c9bfa-127">**Applicationmenu**</span><span class="sxs-lookup"><span data-stu-id="c9bfa-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c9bfa-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9bfa-128">Remarks</span></span>

<span data-ttu-id="c9bfa-129">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-129">Optional.</span></span>

<span data-ttu-id="c9bfa-130">Kann höchstens einmal für jedes [**applicationmenu**](windowsribbon-element-applicationmenu.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="c9bfa-131">Das Steuerelement zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menüband-Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="c9bfa-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9bfa-132">Examples</span></span>

<span data-ttu-id="c9bfa-133">Im folgenden Beispiel wird das grundlegende Markup für das Steuerelement " [zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="c9bfa-134">Das folgende Beispiel zeigt eine Deklaration eines [**recentitems**](windowsribbon-element-recentitems.md) -Befehls.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="c9bfa-135">Das folgende Beispiel zeigt die zugehörige **applicationmenu. recentitems** -und die [**recentitems**](windowsribbon-element-recentitems.md) -Steuerelement Deklaration.</span><span class="sxs-lookup"><span data-stu-id="c9bfa-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="c9bfa-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9bfa-136">Requirements</span></span>



| <span data-ttu-id="c9bfa-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9bfa-137">Requirement</span></span> | <span data-ttu-id="c9bfa-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c9bfa-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c9bfa-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9bfa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c9bfa-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9bfa-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c9bfa-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9bfa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c9bfa-142">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9bfa-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9bfa-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9bfa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9bfa-144">Anwendungsmenü-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c9bfa-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="c9bfa-145">Steuerelement für letzte Elemente</span><span class="sxs-lookup"><span data-stu-id="c9bfa-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





