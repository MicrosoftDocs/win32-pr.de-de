---
title: Command-Element
description: Stellt eine Befehlsdefinition dar.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Befehlselement Windows-Menüband
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443481"
---
# <a name="command-element"></a><span data-ttu-id="04d66-104">Command-Element</span><span class="sxs-lookup"><span data-stu-id="04d66-104">Command element</span></span>

<span data-ttu-id="04d66-105">Stellt eine Befehlsdefinition dar.</span><span class="sxs-lookup"><span data-stu-id="04d66-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="04d66-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="04d66-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="04d66-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="04d66-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04d66-108">attribute</span><span class="sxs-lookup"><span data-stu-id="04d66-108">Attribute</span></span></th>
<th><span data-ttu-id="04d66-109">Typ</span><span class="sxs-lookup"><span data-stu-id="04d66-109">Type</span></span></th>
<th><span data-ttu-id="04d66-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="04d66-110">Required</span></span></th>
<th><span data-ttu-id="04d66-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04d66-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04d66-112"><strong>Kommentar</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-114">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-114">No</span></span><br/></td>
<td><span data-ttu-id="04d66-115">Wird verwendet, um das Befehlselement zu kommentieren.</span><span class="sxs-lookup"><span data-stu-id="04d66-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="04d66-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-117">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="04d66-118">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d66-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-120">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-121">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-121">No</span></span><br/></td>
<td><span data-ttu-id="04d66-122">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="04d66-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="04d66-123">
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs:positiveInteger und xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-124">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="04d66-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="04d66-125">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="04d66-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d66-126"><strong>Keytip</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-128">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-128">No</span></span><br/></td>
<td><span data-ttu-id="04d66-129">Eine Zeichenfolge, die die Tastenkombination eines Befehlselements darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d66-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="04d66-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-131">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d66-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-134">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-134">No</span></span><br/></td>
<td><span data-ttu-id="04d66-135">Eine Zeichenfolge, die den in einem Befehlselement angezeigten Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d66-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="04d66-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-137">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d66-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-140">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-140">No</span></span><br/></td>
<td><span data-ttu-id="04d66-141">Eine Zeichenfolge, die den in einem Befehlselement angezeigten Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d66-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="04d66-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-143">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d66-144"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-146">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-146">No</span></span><br/></td>
<td><span data-ttu-id="04d66-147"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-148">Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Sequenz von Ziffern, Buchstaben oder Unterstrichen besteht.</span><span class="sxs-lookup"><span data-stu-id="04d66-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="04d66-149">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d66-150"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-152">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-152">No</span></span><br/></td>
<td><span data-ttu-id="04d66-153"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-154">Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Sequenz von Ziffern, Buchstaben oder Unterstrichen besteht.</span><span class="sxs-lookup"><span data-stu-id="04d66-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="04d66-155">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04d66-156"><strong>QuickInfoDescription</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-158">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-158">No</span></span><br/></td>
<td><span data-ttu-id="04d66-159">Eine Zeichenfolge, die den in einem Befehlselement angezeigten Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d66-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="04d66-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-161">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04d66-162"><strong>QuickInfoTitle</strong></span><span class="sxs-lookup"><span data-stu-id="04d66-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="04d66-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="04d66-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="04d66-164">Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-164">No</span></span><br/></td>
<td><span data-ttu-id="04d66-165">Eine Zeichenfolge, die den in einem Befehlselement angezeigten Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d66-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="04d66-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="04d66-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04d66-167">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="04d66-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="04d66-168">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04d66-168">Child elements</span></span>



| <span data-ttu-id="04d66-169">Element</span><span class="sxs-lookup"><span data-stu-id="04d66-169">Element</span></span>                                                                                                     | <span data-ttu-id="04d66-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04d66-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="04d66-171">**Command.Comment**</span><span class="sxs-lookup"><span data-stu-id="04d66-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="04d66-172">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="04d66-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="04d66-174">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-175">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="04d66-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="04d66-176">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-177">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="04d66-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="04d66-178">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-179">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="04d66-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="04d66-180">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-181">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="04d66-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="04d66-182">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-183">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="04d66-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="04d66-184">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="04d66-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="04d66-186">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-187">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="04d66-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="04d66-188">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-189">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="04d66-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="04d66-190">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-191">**Command.Symbol**</span><span class="sxs-lookup"><span data-stu-id="04d66-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="04d66-192">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-193">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="04d66-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="04d66-194">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="04d66-195">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="04d66-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="04d66-196">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="04d66-197">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04d66-197">Parent elements</span></span>



| <span data-ttu-id="04d66-198">Element</span><span class="sxs-lookup"><span data-stu-id="04d66-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="04d66-199">**Application.Commands**</span><span class="sxs-lookup"><span data-stu-id="04d66-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="04d66-200">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04d66-200">Remarks</span></span>

<span data-ttu-id="04d66-201">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04d66-201">Required.</span></span>

<span data-ttu-id="04d66-202">Kann ein oder mehrere Male für jedes [**Application.Commands-Element**](windowsribbon-element-application-commands.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="04d66-203">Die untergeordneten Elemente des **Command-Elements** können in beliebiger Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="04d66-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="04d66-204">In der Regel werden Befehlsressourcen im Menübandmarkup deklariert, können aber auch zur Laufzeit mit einem Aufruf von [**SetUICommandProperty festgelegt werden.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)</span><span class="sxs-lookup"><span data-stu-id="04d66-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="04d66-205">Beispielsweise ist es möglich, die [ \_ PKEY \_ Keytip-Eigenschaft](windowsribbon-reference-properties-uipkey-keytip.md) der Benutzeroberfläche für einen Befehl zu setzen, anstatt einen Wert im Markup mit dem [**Command.Keytip-Element zu deklarieren.**](windowsribbon-element-command-keytip.md)</span><span class="sxs-lookup"><span data-stu-id="04d66-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="04d66-206">In Fällen, in denen Befehlseigenschaften wie Bezeichnungen und Bilder nicht mit [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden können, können sie mit einem Aufruf von [**InvalidateUICommand für**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)ungültig erklärt werden.</span><span class="sxs-lookup"><span data-stu-id="04d66-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="04d66-207">Nach der Ungültigkeit fragt das Framework die Hostanwendung nach den Ressourcendetails ab.</span><span class="sxs-lookup"><span data-stu-id="04d66-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="04d66-208">Eine Ressource kann nicht erneut aus der Markupressourcentabelle restatiert werden, nachdem sie für ungültig erklärt wurde.</span><span class="sxs-lookup"><span data-stu-id="04d66-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="04d66-209">Der Markupheaderdatei des Menübands wird für jeden Befehl, der im Markup deklariert ist, eine **Befehlsdefinition** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="04d66-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="04d66-210">Der Wert von *Keytip* fungiert als Zugriffstaste für einen Befehl, es sei denn, dieser Befehl wird über ein Menüelement verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="04d66-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="04d66-211">In diesem Fall ignoriert das Framework den *Keytip-Wert* und verwendet stattdessen ein Zeichen, dem ein ampersand voran geht, wie durch *LabelTitle* oder [UI \_ PKEY \_ Label angegeben.](windowsribbon-reference-properties-uipkey-label.md)</span><span class="sxs-lookup"><span data-stu-id="04d66-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="04d66-212">Wenn kein ampersand durch *LabelTitle* oder UI PKEY Label angegeben wird, wird keine Tastenkombination oder \_ \_ Tastenkombination verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="04d66-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="04d66-213">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04d66-213">Examples</span></span>

<span data-ttu-id="04d66-214">Das folgende Beispiel zeigt ein Manifest von **Command-Elementen** für eine **Registerkarte Start.**</span><span class="sxs-lookup"><span data-stu-id="04d66-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="04d66-215">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="04d66-215">Element information</span></span>

* <span data-ttu-id="04d66-216">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="04d66-216">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="04d66-217">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="04d66-217">**Can be empty**: No</span></span>



 

