---
title: Command-Element
description: Stellt eine Befehls Definition dar.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Windows-Menüband des Befehls Elements
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316137"
---
# <a name="command-element"></a><span data-ttu-id="b3243-104">Command-Element</span><span class="sxs-lookup"><span data-stu-id="b3243-104">Command element</span></span>

<span data-ttu-id="b3243-105">Stellt eine Befehls Definition dar.</span><span class="sxs-lookup"><span data-stu-id="b3243-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="b3243-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b3243-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="b3243-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3243-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3243-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="b3243-108">Attribute</span></span></th>
<th><span data-ttu-id="b3243-109">type</span><span class="sxs-lookup"><span data-stu-id="b3243-109">Type</span></span></th>
<th><span data-ttu-id="b3243-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3243-110">Required</span></span></th>
<th><span data-ttu-id="b3243-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3243-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3243-112"><strong>Kommentar</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-114">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-114">No</span></span><br/></td>
<td><span data-ttu-id="b3243-115">Wird verwendet, um das Command-Element mit Anmerkungen zu versehen.</span><span class="sxs-lookup"><span data-stu-id="b3243-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="b3243-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-117">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="b3243-118">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3243-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-120">xs: positivan teger Union xs: String</span><span class="sxs-lookup"><span data-stu-id="b3243-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-121">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-121">No</span></span><br/></td>
<td><span data-ttu-id="b3243-122">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b3243-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="b3243-123">
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs: positiveingeteger und xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-124">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="b3243-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="b3243-125">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="b3243-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3243-126"><strong>KeyTip</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-128">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-128">No</span></span><br/></td>
<td><span data-ttu-id="b3243-129">Eine Zeichenfolge, die die Tastenkombination eines Command-Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3243-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="b3243-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-131">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3243-132"><strong>Labeldescription</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-134">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-134">No</span></span><br/></td>
<td><span data-ttu-id="b3243-135">Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b3243-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="b3243-136">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-137">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3243-138"><strong>Labeltitle</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-140">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-140">No</span></span><br/></td>
<td><span data-ttu-id="b3243-141">Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b3243-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="b3243-142">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-143">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3243-144"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-146">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-146">No</span></span><br/></td>
<td><span data-ttu-id="b3243-147"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-148">Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Ziffern, Buchstaben oder unterstrichen besteht.</span><span class="sxs-lookup"><span data-stu-id="b3243-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="b3243-149">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3243-150"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-152">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-152">No</span></span><br/></td>
<td><span data-ttu-id="b3243-153"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-154">Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Ziffern, Buchstaben oder unterstrichen besteht.</span><span class="sxs-lookup"><span data-stu-id="b3243-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="b3243-155">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3243-156"><strong>Tooltipdescription</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-158">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-158">No</span></span><br/></td>
<td><span data-ttu-id="b3243-159">Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b3243-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="b3243-160">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-161">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3243-162"><strong>ToolTipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="b3243-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="b3243-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3243-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3243-164">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-164">No</span></span><br/></td>
<td><span data-ttu-id="b3243-165">Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b3243-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="b3243-166">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3243-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3243-167">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3243-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b3243-168">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3243-168">Child elements</span></span>



| <span data-ttu-id="b3243-169">Element</span><span class="sxs-lookup"><span data-stu-id="b3243-169">Element</span></span>                                                                                                     | <span data-ttu-id="b3243-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3243-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b3243-171">**Command. Comment**</span><span class="sxs-lookup"><span data-stu-id="b3243-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="b3243-172">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="b3243-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="b3243-174">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-175">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="b3243-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="b3243-176">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-177">**Command. labeldescription**</span><span class="sxs-lookup"><span data-stu-id="b3243-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="b3243-178">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-179">**Command. labeltitle**</span><span class="sxs-lookup"><span data-stu-id="b3243-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="b3243-180">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-181">**Command. largehighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="b3243-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="b3243-182">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-183">**Command. largeimages**</span><span class="sxs-lookup"><span data-stu-id="b3243-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="b3243-184">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="b3243-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="b3243-186">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-187">**Command. smallhighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="b3243-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="b3243-188">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-189">**Command. smallimages**</span><span class="sxs-lookup"><span data-stu-id="b3243-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="b3243-190">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-191">**Command. Symbol**</span><span class="sxs-lookup"><span data-stu-id="b3243-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="b3243-192">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-193">**Command. tooltipdescription**</span><span class="sxs-lookup"><span data-stu-id="b3243-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="b3243-194">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b3243-195">**Command. ToolTipTitle**</span><span class="sxs-lookup"><span data-stu-id="b3243-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="b3243-196">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="b3243-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b3243-197">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3243-197">Parent elements</span></span>



| <span data-ttu-id="b3243-198">Element</span><span class="sxs-lookup"><span data-stu-id="b3243-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3243-199">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="b3243-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b3243-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3243-200">Remarks</span></span>

<span data-ttu-id="b3243-201">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3243-201">Required.</span></span>

<span data-ttu-id="b3243-202">Kann für jedes [**Application. Commands**](windowsribbon-element-application-commands.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="b3243-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="b3243-203">Die untergeordneten Elemente des **Command** -Elements können in beliebiger Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="b3243-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="b3243-204">In der Regel werden Befehls Ressourcen in Menüband-Markup deklariert, Sie können jedoch auch zur Laufzeit mit einem Aufruf von [**setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b3243-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="b3243-205">Beispielsweise ist es möglich, die Benutzeroberflächen [- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md) -Eigenschaft für einen Befehl festzulegen, anstatt einen Wert im Markup mit dem [**Command. KeyTip**](windowsribbon-element-command-keytip.md) -Element zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b3243-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="b3243-206">In Fällen, in denen Befehls Eigenschaften, z. b. Bezeichnungen und Bilder, nicht mit [**setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden können, können Sie mit einem- [**Befehl von invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)ungültig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="b3243-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="b3243-207">Nach der Invalidierung fragt das Framework die Host Anwendung nach den Ressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="b3243-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="b3243-208">Eine Ressource kann nicht aus der Markup Ressourcen Tabelle wieder hergestellt werden, nachdem Sie ungültig gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="b3243-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="b3243-209">Der Menüband-Markup Header Datei wird für jeden **Befehl** , der im Markup deklariert ist, eine Befehls Definition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b3243-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="b3243-210">Der Wert von *KeyTip* fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b3243-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="b3243-211">In diesem Fall ignoriert das Framework den *KeyTip* -Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen gemäß der Bezeichnung " *labeltitle* " oder " [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md)" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="b3243-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="b3243-212">Wenn kein kaufmännisches und-Zeichen von der Bezeichnung " *labeltitle* " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b3243-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="b3243-213">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3243-213">Examples</span></span>

<span data-ttu-id="b3243-214">Das folgende Beispiel zeigt ein Manifest der **Befehls** Elemente für eine Registerkarte **Home** .</span><span class="sxs-lookup"><span data-stu-id="b3243-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="b3243-215">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b3243-215">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b3243-216">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="b3243-216">Minimum supported system</span></span><br/> | <span data-ttu-id="b3243-217">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3243-217">Windows 7</span></span> |
| <span data-ttu-id="b3243-218">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="b3243-218">Can be empty</span></span>                        | <span data-ttu-id="b3243-219">Nein</span><span class="sxs-lookup"><span data-stu-id="b3243-219">No</span></span>        |



 

