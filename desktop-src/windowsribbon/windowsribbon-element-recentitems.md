---
title: RecentItems-Element
description: Stellt das Steuerelement Letzte Elemente im Anwendungsmenü dar.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems-Element Windows-Menüband
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444111"
---
# <a name="recentitems-element"></a><span data-ttu-id="d450d-104">RecentItems-Element</span><span class="sxs-lookup"><span data-stu-id="d450d-104">RecentItems element</span></span>

<span data-ttu-id="d450d-105">Stellt das Steuerelement [Letzte Elemente](windowsribbon-controls-recentitems.md) im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d450d-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d450d-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d450d-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="d450d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d450d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d450d-108">attribute</span><span class="sxs-lookup"><span data-stu-id="d450d-108">Attribute</span></span></th>
<th><span data-ttu-id="d450d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d450d-109">Type</span></span></th>
<th><span data-ttu-id="d450d-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d450d-110">Required</span></span></th>
<th><span data-ttu-id="d450d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d450d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d450d-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d450d-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d450d-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="d450d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d450d-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d450d-114">No</span></span><br/></td>
<td><span data-ttu-id="d450d-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d450d-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d450d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="d450d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d450d-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d450d-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d450d-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d450d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d450d-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d450d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d450d-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="d450d-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="d450d-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d450d-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="d450d-122">Nein</span><span class="sxs-lookup"><span data-stu-id="d450d-122">No</span></span><br/></td>
<td><span data-ttu-id="d450d-123">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d450d-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d450d-124">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d450d-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="d450d-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="d450d-125">Default.</span></span> <br/> </dd> <span data-ttu-id="d450d-126"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d450d-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d450d-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="d450d-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="d450d-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="d450d-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="d450d-129">Nein</span><span class="sxs-lookup"><span data-stu-id="d450d-129">No</span></span><br/></td>
<td><span data-ttu-id="d450d-130">Die Anzahl der zuletzt anzuzeigende Elemente.</span><span class="sxs-lookup"><span data-stu-id="d450d-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="d450d-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="d450d-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d450d-132">Ein ganzzahliger Wert von 0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d450d-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="d450d-133">Der Standardwert ist <strong>10.</strong></span><span class="sxs-lookup"><span data-stu-id="d450d-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d450d-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d450d-134">Child elements</span></span>

<span data-ttu-id="d450d-135">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d450d-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d450d-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d450d-136">Parent elements</span></span>



| <span data-ttu-id="d450d-137">Element</span><span class="sxs-lookup"><span data-stu-id="d450d-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d450d-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="d450d-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d450d-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d450d-139">Remarks</span></span>

<span data-ttu-id="d450d-140">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d450d-140">Required.</span></span>

<span data-ttu-id="d450d-141">Muss für jedes [**ApplicationMenu.RecentItems-Element**](windowsribbon-element-applicationmenu-recentitems.md) genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="d450d-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="d450d-142">Das Steuerelement Zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menübandanwendung an.</span><span class="sxs-lookup"><span data-stu-id="d450d-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="d450d-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d450d-143">Examples</span></span>

<span data-ttu-id="d450d-144">Im folgenden Beispiel wird das grundlegende Markup für das [Steuerelement Recent Items](windowsribbon-controls-recentitems.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d450d-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="d450d-145">Das folgende Beispiel zeigt eine **RecentItems** Command-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="d450d-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="d450d-146">Das folgende Beispiel zeigt die **zugeordnete RecentItems-Steuerelementdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="d450d-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="d450d-147">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d450d-147">Element information</span></span>

* <span data-ttu-id="d450d-148">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d450d-148">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d450d-149">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="d450d-149">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="d450d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d450d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d450d-151">Anwendungsmenü-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d450d-151">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="d450d-152">Steuerelement "Zuletzt durchgeführte Elemente"</span><span class="sxs-lookup"><span data-stu-id="d450d-152">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





