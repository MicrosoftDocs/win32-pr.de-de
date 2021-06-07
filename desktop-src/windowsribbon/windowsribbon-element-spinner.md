---
title: Spinner-Element
description: Stellt ein Spinner-Steuerelement dar.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Spinner-Element Windows-Menüband
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444811"
---
# <a name="spinner-element"></a><span data-ttu-id="58d0e-104">Spinner-Element</span><span class="sxs-lookup"><span data-stu-id="58d0e-104">Spinner element</span></span>

<span data-ttu-id="58d0e-105">Stellt ein [Spinner-Steuerelement](windowsribbon-controls-spinner.md) dar.</span><span class="sxs-lookup"><span data-stu-id="58d0e-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="58d0e-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="58d0e-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="58d0e-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="58d0e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58d0e-108">attribute</span><span class="sxs-lookup"><span data-stu-id="58d0e-108">Attribute</span></span></th>
<th><span data-ttu-id="58d0e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="58d0e-109">Type</span></span></th>
<th><span data-ttu-id="58d0e-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58d0e-110">Required</span></span></th>
<th><span data-ttu-id="58d0e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58d0e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58d0e-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="58d0e-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="58d0e-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="58d0e-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="58d0e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="58d0e-114">No</span></span><br/></td>
<td><span data-ttu-id="58d0e-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="58d0e-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="58d0e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="58d0e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="58d0e-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="58d0e-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="58d0e-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="58d0e-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="58d0e-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="58d0e-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="58d0e-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58d0e-120">Child elements</span></span>

<span data-ttu-id="58d0e-121">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="58d0e-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="58d0e-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58d0e-122">Parent elements</span></span>



| <span data-ttu-id="58d0e-123">Element</span><span class="sxs-lookup"><span data-stu-id="58d0e-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="58d0e-124">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="58d0e-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="58d0e-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="58d0e-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="58d0e-126">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="58d0e-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="58d0e-127">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="58d0e-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="58d0e-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="58d0e-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="58d0e-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58d0e-129">Remarks</span></span>

<span data-ttu-id="58d0e-130">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="58d0e-130">Optional.</span></span>

<span data-ttu-id="58d0e-131">Kann ein oder mehrere Male für jedes [**ControlGroup-**](windowsribbon-element-controlgroup.md) oder [**Group-Element**](windowsribbon-element-group.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="58d0e-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="58d0e-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58d0e-132">Examples</span></span>

<span data-ttu-id="58d0e-133">Im folgenden Beispiel wird das grundlegende Markup für den [Spinner](windowsribbon-controls-spinner.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="58d0e-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="58d0e-134">Dieser Codeabschnitt zeigt die **Spinner** Command-Deklarationen mit einem [**Group-Element,**](windowsribbon-element-group.md) das als übergeordneter Container für das **Spinner-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="58d0e-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


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



<span data-ttu-id="58d0e-135">Dieser Codeabschnitt zeigt die Spinner-Steuerelementdeklarationen. </span><span class="sxs-lookup"><span data-stu-id="58d0e-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="58d0e-136">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="58d0e-136">Element information</span></span>

- <span data-ttu-id="58d0e-137">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="58d0e-137">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="58d0e-138">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="58d0e-138">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="58d0e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58d0e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d0e-140">Spinner-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="58d0e-140">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





