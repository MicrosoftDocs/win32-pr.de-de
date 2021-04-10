---
title: CheckBox-Element
description: Stellt ein Kontrollkästchen-Steuerelement dar.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox-Element Windows-Menüband
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104101226"
---
# <a name="checkbox-element"></a><span data-ttu-id="46850-104">CheckBox-Element</span><span class="sxs-lookup"><span data-stu-id="46850-104">CheckBox element</span></span>

<span data-ttu-id="46850-105">Stellt ein Kontroll [Kästchen](windowsribbon-controls-checkbox.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="46850-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="46850-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="46850-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="46850-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="46850-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46850-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="46850-108">Attribute</span></span></th>
<th><span data-ttu-id="46850-109">type</span><span class="sxs-lookup"><span data-stu-id="46850-109">Type</span></span></th>
<th><span data-ttu-id="46850-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="46850-110">Required</span></span></th>
<th><span data-ttu-id="46850-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46850-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46850-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="46850-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="46850-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="46850-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="46850-114">Nein</span><span class="sxs-lookup"><span data-stu-id="46850-114">No</span></span><br/></td>
<td><span data-ttu-id="46850-115">Dieses Attribut ist nur gültig, wenn das <strong>CheckBox</strong> -Element ein untergeordnetes Element von <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>quickaccesstoolbar. ApplicationDefaults</strong></a>ist.</span><span class="sxs-lookup"><span data-stu-id="46850-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="46850-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="46850-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="46850-117">Das <strong>Kontrollkästchen</strong> unterstützt keinen tertiären bzw. unbestimmten Zustand.</span><span class="sxs-lookup"><span data-stu-id="46850-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="46850-118">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="46850-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="46850-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="46850-119">Default.</span></span> <br/> </dd> <span data-ttu-id="46850-120"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="46850-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46850-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="46850-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="46850-122">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="46850-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="46850-123">Nein</span><span class="sxs-lookup"><span data-stu-id="46850-123">No</span></span><br/></td>
<td><span data-ttu-id="46850-124">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="46850-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="46850-125">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="46850-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="46850-126">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="46850-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="46850-127">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="46850-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="46850-128">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="46850-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="46850-129">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46850-129">Child elements</span></span>

<span data-ttu-id="46850-130">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="46850-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="46850-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46850-131">Parent elements</span></span>



| <span data-ttu-id="46850-132">Element</span><span class="sxs-lookup"><span data-stu-id="46850-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46850-133">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="46850-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="46850-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="46850-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="46850-135">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="46850-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="46850-136">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="46850-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="46850-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="46850-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="46850-138">**Quickaccesstoolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="46850-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="46850-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="46850-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="46850-140">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="46850-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="46850-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46850-141">Remarks</span></span>

<span data-ttu-id="46850-142">Optional oder erforderlich, abhängig vom übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="46850-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="46850-143">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="46850-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="46850-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46850-144">Examples</span></span>

<span data-ttu-id="46850-145">Im folgenden Beispiel wird das grundlegende Markup für das **CheckBox** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="46850-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="46850-146">In diesem Code Abschnitt werden die Befehls Deklarationen des **CheckBox** -Befehls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46850-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="46850-147">In diesem Code Abschnitt werden die **CheckBox** -Steuerelement Deklarationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46850-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="46850-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="46850-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="46850-149">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="46850-149">Minimum supported system</span></span><br/> | <span data-ttu-id="46850-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46850-150">Windows 7</span></span> |
| <span data-ttu-id="46850-151">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="46850-151">Can be empty</span></span>                        | <span data-ttu-id="46850-152">Ja</span><span class="sxs-lookup"><span data-stu-id="46850-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="46850-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46850-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46850-154">Kontrollkästchen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="46850-154">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





