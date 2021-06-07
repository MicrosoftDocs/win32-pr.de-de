---
title: HelpButton-Element
description: Stellt das Steuerelement Hilfeschaltfläche dar.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442841"
---
# <a name="helpbutton-element"></a><span data-ttu-id="dd303-104">HelpButton-Element</span><span class="sxs-lookup"><span data-stu-id="dd303-104">HelpButton element</span></span>

<span data-ttu-id="dd303-105">Stellt das Steuerelement [Hilfeschaltfläche](windowsribbon-controls-helpbutton.md) dar.</span><span class="sxs-lookup"><span data-stu-id="dd303-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="dd303-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="dd303-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="dd303-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd303-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd303-108">attribute</span><span class="sxs-lookup"><span data-stu-id="dd303-108">Attribute</span></span></th>
<th><span data-ttu-id="dd303-109">Typ</span><span class="sxs-lookup"><span data-stu-id="dd303-109">Type</span></span></th>
<th><span data-ttu-id="dd303-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd303-110">Required</span></span></th>
<th><span data-ttu-id="dd303-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd303-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd303-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="dd303-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="dd303-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="dd303-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="dd303-114">Nein</span><span class="sxs-lookup"><span data-stu-id="dd303-114">No</span></span><br/></td>
<td><span data-ttu-id="dd303-115">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd303-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="dd303-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="dd303-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="dd303-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="dd303-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="dd303-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="dd303-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="dd303-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dd303-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="dd303-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd303-120">Child elements</span></span>

<span data-ttu-id="dd303-121">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd303-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="dd303-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd303-122">Parent elements</span></span>



| <span data-ttu-id="dd303-123">Element</span><span class="sxs-lookup"><span data-stu-id="dd303-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="dd303-124">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="dd303-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="dd303-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd303-125">Remarks</span></span>

<span data-ttu-id="dd303-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd303-126">Optional.</span></span>

<span data-ttu-id="dd303-127">Kann für jedes [**Ribbon.HelpButton--Menüband nur einmal auftreten.**](windowsribbon-element-ribbon-helpbutton.md)</span><span class="sxs-lookup"><span data-stu-id="dd303-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="dd303-128">Öffnet ein Anwendungshilfedialogfeld, wenn darauf geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="dd303-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="dd303-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd303-129">Examples</span></span>

<span data-ttu-id="dd303-130">Im folgenden Beispiel wird das grundlegende Markup veranschaulicht, das zum Implementieren eines [Menüband-Hilfeschaltfläche-Steuerelements erforderlich](windowsribbon-controls-helpbutton.md) ist.</span><span class="sxs-lookup"><span data-stu-id="dd303-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="dd303-131">Dieser Codeabschnitt zeigt die **HelpButton-Befehlsdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="dd303-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="dd303-132">Dieser Codeabschnitt zeigt die **HelpButton-Steuerelementdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="dd303-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="dd303-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dd303-133">Element information</span></span>

* <span data-ttu-id="dd303-134">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd303-134">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="dd303-135">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="dd303-135">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="dd303-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd303-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd303-137">Schaltflächen-Steuerelement "Hilfe"</span><span class="sxs-lookup"><span data-stu-id="dd303-137">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





