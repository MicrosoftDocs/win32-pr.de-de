---
title: Spinner-Element
description: Stellt ein Spinner-Steuerelement dar.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Fensterleiste des Spinner-Elements
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1f9727dc7fbad8be24c15f0b1f551b021294dd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038493"
---
# <a name="spinner-element"></a><span data-ttu-id="2464b-104">Spinner-Element</span><span class="sxs-lookup"><span data-stu-id="2464b-104">Spinner element</span></span>

<span data-ttu-id="2464b-105">Stellt ein [Spinner](windowsribbon-controls-spinner.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="2464b-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2464b-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="2464b-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="2464b-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="2464b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2464b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="2464b-108">Attribute</span></span></th>
<th><span data-ttu-id="2464b-109">type</span><span class="sxs-lookup"><span data-stu-id="2464b-109">Type</span></span></th>
<th><span data-ttu-id="2464b-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2464b-110">Required</span></span></th>
<th><span data-ttu-id="2464b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2464b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2464b-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2464b-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2464b-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="2464b-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2464b-114">Nein</span><span class="sxs-lookup"><span data-stu-id="2464b-114">No</span></span><br/></td>
<td><span data-ttu-id="2464b-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="2464b-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2464b-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="2464b-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2464b-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="2464b-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2464b-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2464b-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2464b-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2464b-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2464b-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2464b-120">Child elements</span></span>

<span data-ttu-id="2464b-121">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="2464b-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2464b-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2464b-122">Parent elements</span></span>



| <span data-ttu-id="2464b-123">Element</span><span class="sxs-lookup"><span data-stu-id="2464b-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2464b-124">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="2464b-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="2464b-125">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="2464b-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="2464b-126">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="2464b-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="2464b-127">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="2464b-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="2464b-128">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="2464b-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2464b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2464b-129">Remarks</span></span>

<span data-ttu-id="2464b-130">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="2464b-130">Optional.</span></span>

<span data-ttu-id="2464b-131">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md) -oder [**Group**](windowsribbon-element-group.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="2464b-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2464b-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2464b-132">Examples</span></span>

<span data-ttu-id="2464b-133">Im folgenden Beispiel wird das grundlegende Markup für den [Spinner](windowsribbon-controls-spinner.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2464b-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="2464b-134">Dieser Code Abschnitt zeigt die **Spinner** -Befehls Deklarationen mit einem [**Group**](windowsribbon-element-group.md) -Element, das als übergeordneter Container für das **Spinner** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="2464b-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="2464b-135">Dieser Code Abschnitt zeigt die **Spinner** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="2464b-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="2464b-136">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2464b-136">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2464b-137">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="2464b-137">Minimum supported system</span></span><br/> | <span data-ttu-id="2464b-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2464b-138">Windows 7</span></span> |
| <span data-ttu-id="2464b-139">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="2464b-139">Can be empty</span></span>                        | <span data-ttu-id="2464b-140">Ja</span><span class="sxs-lookup"><span data-stu-id="2464b-140">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="2464b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2464b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2464b-142">Spinner-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2464b-142">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





