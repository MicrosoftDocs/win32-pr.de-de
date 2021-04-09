---
title: Recentitems-Element
description: Stellt das aktuelle Items-Steuerelement im Anwendungsmenü dar.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Fenster "recentitems"-Element Fenster
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038499"
---
# <a name="recentitems-element"></a><span data-ttu-id="6b192-104">Recentitems-Element</span><span class="sxs-lookup"><span data-stu-id="6b192-104">RecentItems element</span></span>

<span data-ttu-id="6b192-105">Stellt das [aktuelle Items](windowsribbon-controls-recentitems.md) -Steuerelement im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.</span><span class="sxs-lookup"><span data-stu-id="6b192-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="6b192-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6b192-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="6b192-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="6b192-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b192-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="6b192-108">Attribute</span></span></th>
<th><span data-ttu-id="6b192-109">type</span><span class="sxs-lookup"><span data-stu-id="6b192-109">Type</span></span></th>
<th><span data-ttu-id="6b192-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6b192-110">Required</span></span></th>
<th><span data-ttu-id="6b192-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b192-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b192-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6b192-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6b192-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="6b192-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6b192-114">Nein</span><span class="sxs-lookup"><span data-stu-id="6b192-114">No</span></span><br/></td>
<td><span data-ttu-id="6b192-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="6b192-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6b192-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="6b192-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6b192-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="6b192-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6b192-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="6b192-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6b192-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6b192-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b192-120"><strong>Wird festgesetzt</strong></span><span class="sxs-lookup"><span data-stu-id="6b192-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="6b192-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="6b192-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="6b192-122">Nein</span><span class="sxs-lookup"><span data-stu-id="6b192-122">No</span></span><br/></td>
<td><span data-ttu-id="6b192-123">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="6b192-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="6b192-124">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="6b192-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6b192-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="6b192-125">Default.</span></span> <br/> </dd> <span data-ttu-id="6b192-126"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="6b192-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b192-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="6b192-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="6b192-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="6b192-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="6b192-129">Nein</span><span class="sxs-lookup"><span data-stu-id="6b192-129">No</span></span><br/></td>
<td><span data-ttu-id="6b192-130">Die Anzahl der zuletzt angezeigten Elemente.</span><span class="sxs-lookup"><span data-stu-id="6b192-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="6b192-131">
<dt><span></span><span></span><strong></strong> (xs: nonnegativinteger)</span><span class="sxs-lookup"><span data-stu-id="6b192-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="6b192-132">Ein ganzzahliger Wert von 0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6b192-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="6b192-133">Der Standardwert ist <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b192-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6b192-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b192-134">Child elements</span></span>

<span data-ttu-id="6b192-135">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="6b192-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6b192-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b192-136">Parent elements</span></span>



| <span data-ttu-id="6b192-137">Element</span><span class="sxs-lookup"><span data-stu-id="6b192-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b192-138">**Applicationmenu. recentitems**</span><span class="sxs-lookup"><span data-stu-id="6b192-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6b192-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b192-139">Remarks</span></span>

<span data-ttu-id="6b192-140">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b192-140">Required.</span></span>

<span data-ttu-id="6b192-141">Muss für jedes [**applicationmenu. recentitems**](windowsribbon-element-applicationmenu-recentitems.md) -Element genau einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="6b192-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="6b192-142">Das Steuerelement zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menüband-Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="6b192-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="6b192-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b192-143">Examples</span></span>

<span data-ttu-id="6b192-144">Im folgenden Beispiel wird das grundlegende Markup für das Steuerelement " [zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6b192-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="6b192-145">Das folgende Beispiel zeigt eine Deklaration eines **recentitems** -Befehls.</span><span class="sxs-lookup"><span data-stu-id="6b192-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="6b192-146">Das folgende Beispiel zeigt die zugehörige Deklaration der **recentitems** -Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="6b192-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="6b192-147">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6b192-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="6b192-148">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="6b192-148">Minimum supported system</span></span><br/> | <span data-ttu-id="6b192-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b192-149">Windows 7</span></span> |
| <span data-ttu-id="6b192-150">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="6b192-150">Can be empty</span></span>                        | <span data-ttu-id="6b192-151">Ja</span><span class="sxs-lookup"><span data-stu-id="6b192-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="6b192-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b192-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b192-153">Anwendungsmenü-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6b192-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="6b192-154">Steuerelement für letzte Elemente</span><span class="sxs-lookup"><span data-stu-id="6b192-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





