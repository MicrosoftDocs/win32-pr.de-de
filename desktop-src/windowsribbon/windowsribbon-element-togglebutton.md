---
title: "\"Element\"-Element"
description: Stellt ein UMSCHALT Fläche-Steuerelement dar.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Menüband für das Fenster "Element" (Fenster)
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104314135"
---
# <a name="togglebutton-element"></a><span data-ttu-id="0b67c-104">"Element"-Element</span><span class="sxs-lookup"><span data-stu-id="0b67c-104">ToggleButton element</span></span>

<span data-ttu-id="0b67c-105">Stellt ein [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="0b67c-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="0b67c-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0b67c-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="0b67c-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b67c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b67c-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="0b67c-108">Attribute</span></span></th>
<th><span data-ttu-id="0b67c-109">type</span><span class="sxs-lookup"><span data-stu-id="0b67c-109">Type</span></span></th>
<th><span data-ttu-id="0b67c-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b67c-110">Required</span></span></th>
<th><span data-ttu-id="0b67c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b67c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b67c-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="0b67c-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="0b67c-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="0b67c-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="0b67c-114">Nein</span><span class="sxs-lookup"><span data-stu-id="0b67c-114">No</span></span><br/></td>
<td><span data-ttu-id="0b67c-115">Dieses Attribut ist nur gültig, wenn das <strong>ToggleButton</strong> -Element ein untergeordnetes Element von <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>quickaccesstoolbar. ApplicationDefaults</strong></a>ist.</span><span class="sxs-lookup"><span data-stu-id="0b67c-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="0b67c-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="0b67c-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="0b67c-117">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="0b67c-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0b67c-118">Standard.</span><span class="sxs-lookup"><span data-stu-id="0b67c-118">Default.</span></span> <br/> </dd> <span data-ttu-id="0b67c-119"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="0b67c-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b67c-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0b67c-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0b67c-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="0b67c-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0b67c-122">Nein</span><span class="sxs-lookup"><span data-stu-id="0b67c-122">No</span></span><br/></td>
<td><span data-ttu-id="0b67c-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="0b67c-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0b67c-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="0b67c-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b67c-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="0b67c-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0b67c-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0b67c-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0b67c-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0b67c-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0b67c-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b67c-128">Child elements</span></span>

<span data-ttu-id="0b67c-129">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0b67c-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0b67c-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b67c-130">Parent elements</span></span>



| <span data-ttu-id="0b67c-131">Element</span><span class="sxs-lookup"><span data-stu-id="0b67c-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b67c-132">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="0b67c-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="0b67c-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="0b67c-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="0b67c-134">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="0b67c-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="0b67c-135">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="0b67c-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="0b67c-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="0b67c-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="0b67c-137">**Quickaccesstoolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="0b67c-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="0b67c-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="0b67c-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="0b67c-139">**SplitButton. buttonitem**</span><span class="sxs-lookup"><span data-stu-id="0b67c-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="0b67c-140">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="0b67c-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="0b67c-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b67c-141">Remarks</span></span>

<span data-ttu-id="0b67c-142">Optional oder erforderlich, abhängig vom übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="0b67c-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="0b67c-143">Kann höchstens einmal für jedes [**SplitButton. buttonitem**](windowsribbon-element-splitbutton-buttonitem.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b67c-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="0b67c-144">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**Group**](windowsribbon-element-group.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0b67c-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="0b67c-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b67c-145">Examples</span></span>

<span data-ttu-id="0b67c-146">Im folgenden Beispiel wird das grundlegende Markup für **das Element "** -Element" veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="0b67c-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="0b67c-147">Dieser Code Abschnitt zeigt eine **ToggleButton** -Element Deklaration innerhalb des [**quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="0b67c-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0b67c-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b67c-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0b67c-149">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0b67c-149">Minimum supported system</span></span><br/> | <span data-ttu-id="0b67c-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b67c-150">Windows 7</span></span> |
| <span data-ttu-id="0b67c-151">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0b67c-151">Can be empty</span></span>                        | <span data-ttu-id="0b67c-152">Ja</span><span class="sxs-lookup"><span data-stu-id="0b67c-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="0b67c-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b67c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b67c-154">Umschalten des Schaltflächen-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="0b67c-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





