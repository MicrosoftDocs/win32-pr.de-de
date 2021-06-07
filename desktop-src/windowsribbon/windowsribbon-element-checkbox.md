---
title: CheckBox-Element
description: Stellt ein Kontrollkästchen-Steuerelement dar.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443041"
---
# <a name="checkbox-element"></a><span data-ttu-id="1d164-104">CheckBox-Element</span><span class="sxs-lookup"><span data-stu-id="1d164-104">CheckBox element</span></span>

<span data-ttu-id="1d164-105">Stellt ein [Kontrollkästchen-Steuerelement](windowsribbon-controls-checkbox.md) dar.</span><span class="sxs-lookup"><span data-stu-id="1d164-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="1d164-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="1d164-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="1d164-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d164-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d164-108">attribute</span><span class="sxs-lookup"><span data-stu-id="1d164-108">Attribute</span></span></th>
<th><span data-ttu-id="1d164-109">Typ</span><span class="sxs-lookup"><span data-stu-id="1d164-109">Type</span></span></th>
<th><span data-ttu-id="1d164-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1d164-110">Required</span></span></th>
<th><span data-ttu-id="1d164-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d164-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d164-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="1d164-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="1d164-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="1d164-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="1d164-114">Nein</span><span class="sxs-lookup"><span data-stu-id="1d164-114">No</span></span><br/></td>
<td><span data-ttu-id="1d164-115">Dieses Attribut ist nur gültig, wenn das <strong>CheckBox-Element</strong> ein untergeordnetes Element von <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults ist.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d164-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="1d164-116">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="1d164-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d164-117">Das <strong>CheckBox-Kontrollkästchen</strong> unterstützt keinen tertiären oder unbestimmten Zustand.</span><span class="sxs-lookup"><span data-stu-id="1d164-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="1d164-118">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="1d164-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1d164-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="1d164-119">Default.</span></span> <br/> </dd> <span data-ttu-id="1d164-120"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="1d164-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d164-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1d164-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1d164-122">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="1d164-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1d164-123">Nein</span><span class="sxs-lookup"><span data-stu-id="1d164-123">No</span></span><br/></td>
<td><span data-ttu-id="1d164-124">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d164-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1d164-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="1d164-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1d164-126">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="1d164-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1d164-127">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1d164-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1d164-128">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1d164-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1d164-129">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d164-129">Child elements</span></span>

<span data-ttu-id="1d164-130">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1d164-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1d164-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d164-131">Parent elements</span></span>



| <span data-ttu-id="1d164-132">Element</span><span class="sxs-lookup"><span data-stu-id="1d164-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d164-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="1d164-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="1d164-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="1d164-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="1d164-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="1d164-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="1d164-136">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="1d164-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="1d164-137">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="1d164-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="1d164-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="1d164-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="1d164-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1d164-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="1d164-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="1d164-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="1d164-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d164-141">Remarks</span></span>

<span data-ttu-id="1d164-142">Optional oder erforderlich, je nach übergeordnetem Element.</span><span class="sxs-lookup"><span data-stu-id="1d164-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="1d164-143">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) [**QuickAccessToolbar.ApplicationDefaults-,**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="1d164-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="1d164-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d164-144">Examples</span></span>

<span data-ttu-id="1d164-145">Im folgenden Beispiel wird das grundlegende Markup für das **CheckBox-Element** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1d164-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="1d164-146">Dieser Codeabschnitt zeigt die **Deklarationen des** CheckBox-Befehls.</span><span class="sxs-lookup"><span data-stu-id="1d164-146">This section of code shows the **CheckBox** Command declarations.</span></span>


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



<span data-ttu-id="1d164-147">Dieser Codeabschnitt zeigt die **CheckBox-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="1d164-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="1d164-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1d164-148">Element information</span></span>

* <span data-ttu-id="1d164-149">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d164-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="1d164-150">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="1d164-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="1d164-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d164-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d164-152">Kontrollkästchen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1d164-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





