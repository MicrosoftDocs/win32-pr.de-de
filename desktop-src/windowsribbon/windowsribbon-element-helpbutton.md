---
title: HelpButton-Element
description: Stellt das Hilfe Button-Steuerelement dar.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton-Element Windows-Menüband
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106341911"
---
# <a name="helpbutton-element"></a><span data-ttu-id="d4819-104">HelpButton-Element</span><span class="sxs-lookup"><span data-stu-id="d4819-104">HelpButton element</span></span>

<span data-ttu-id="d4819-105">Stellt das [Hilfe Button](windowsribbon-controls-helpbutton.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="d4819-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="d4819-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d4819-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="d4819-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4819-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4819-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="d4819-108">Attribute</span></span></th>
<th><span data-ttu-id="d4819-109">type</span><span class="sxs-lookup"><span data-stu-id="d4819-109">Type</span></span></th>
<th><span data-ttu-id="d4819-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d4819-110">Required</span></span></th>
<th><span data-ttu-id="d4819-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4819-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4819-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d4819-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d4819-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="d4819-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d4819-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d4819-114">No</span></span><br/></td>
<td><span data-ttu-id="d4819-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="d4819-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d4819-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="d4819-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d4819-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d4819-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d4819-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d4819-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d4819-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d4819-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d4819-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4819-120">Child elements</span></span>

<span data-ttu-id="d4819-121">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d4819-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d4819-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4819-122">Parent elements</span></span>



| <span data-ttu-id="d4819-123">Element</span><span class="sxs-lookup"><span data-stu-id="d4819-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d4819-124">**Menüband. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="d4819-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d4819-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4819-125">Remarks</span></span>

<span data-ttu-id="d4819-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d4819-126">Optional.</span></span>

<span data-ttu-id="d4819-127">Kann höchstens einmal für jede [**Multifunktionsleiste. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="d4819-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="d4819-128">Öffnet das Dialogfeld Anwendungs Hilfe, wenn darauf geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="d4819-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="d4819-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4819-129">Examples</span></span>

<span data-ttu-id="d4819-130">Das folgende Beispiel veranschaulicht das grundlegende Markup, das zum Implementieren eines [Schalt](windowsribbon-controls-helpbutton.md) Flächen-Steuer Elements für die Multifunktionsleiste erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d4819-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="d4819-131">Dieser Code Abschnitt zeigt die **HelpButton** -Befehls Deklaration.</span><span class="sxs-lookup"><span data-stu-id="d4819-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="d4819-132">In diesem Code Abschnitt wird die **HelpButton** -Steuerelement Deklaration gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4819-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="d4819-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d4819-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d4819-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d4819-134">Minimum supported system</span></span><br/> | <span data-ttu-id="d4819-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4819-135">Windows 7</span></span> |
| <span data-ttu-id="d4819-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d4819-136">Can be empty</span></span>                        | <span data-ttu-id="d4819-137">Ja</span><span class="sxs-lookup"><span data-stu-id="d4819-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="d4819-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4819-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4819-139">Hilfe Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d4819-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





