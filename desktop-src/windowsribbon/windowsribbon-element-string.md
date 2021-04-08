---
title: String-Element
description: Stellt eine Zeichen folgen Ressource dar.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- String-Element Windows-Menüband
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038048"
---
# <a name="string-element"></a><span data-ttu-id="32011-104">String-Element</span><span class="sxs-lookup"><span data-stu-id="32011-104">String element</span></span>

<span data-ttu-id="32011-105">Stellt eine Zeichen folgen Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="32011-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="32011-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="32011-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="32011-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="32011-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32011-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="32011-108">Attribute</span></span></th>
<th><span data-ttu-id="32011-109">type</span><span class="sxs-lookup"><span data-stu-id="32011-109">Type</span></span></th>
<th><span data-ttu-id="32011-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="32011-110">Required</span></span></th>
<th><span data-ttu-id="32011-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32011-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32011-112"><strong>Inhalt</strong></span><span class="sxs-lookup"><span data-stu-id="32011-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="32011-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="32011-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="32011-114">Nein</span><span class="sxs-lookup"><span data-stu-id="32011-114">No</span></span><br/></td>
<td><span data-ttu-id="32011-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="32011-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32011-116">Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="32011-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32011-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="32011-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="32011-118">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="32011-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="32011-119">Nein</span><span class="sxs-lookup"><span data-stu-id="32011-119">No</span></span><br/></td>
<td><span data-ttu-id="32011-120">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="32011-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="32011-121">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="32011-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32011-122">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="32011-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="32011-123">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="32011-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32011-124"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="32011-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="32011-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="32011-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="32011-126">Nein</span><span class="sxs-lookup"><span data-stu-id="32011-126">No</span></span><br/></td>
<td><span data-ttu-id="32011-127">Das Ressourcen Symbol für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="32011-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="32011-128">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="32011-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32011-129">Ein Buchstabe oder Unterstrich, gefolgt von einer beliebigen Reihenfolge von Buchstaben, Ziffern oder unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="32011-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="32011-130">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="32011-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="32011-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32011-131">Child elements</span></span>



| <span data-ttu-id="32011-132">Element</span><span class="sxs-lookup"><span data-stu-id="32011-132">Element</span></span>                                                                   | <span data-ttu-id="32011-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32011-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="32011-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="32011-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="32011-135">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="32011-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="32011-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="32011-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="32011-137">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="32011-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="32011-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="32011-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="32011-139">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="32011-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="32011-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32011-140">Parent elements</span></span>



| <span data-ttu-id="32011-141">Element</span><span class="sxs-lookup"><span data-stu-id="32011-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32011-142">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="32011-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="32011-143">**Command. labeldescription**</span><span class="sxs-lookup"><span data-stu-id="32011-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="32011-144">**Command. labeltitle**</span><span class="sxs-lookup"><span data-stu-id="32011-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="32011-145">**Command. tooltipdescription**</span><span class="sxs-lookup"><span data-stu-id="32011-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="32011-146">**Command. ToolTipTitle**</span><span class="sxs-lookup"><span data-stu-id="32011-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="32011-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32011-147">Remarks</span></span>

<span data-ttu-id="32011-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="32011-148">Optional.</span></span>

<span data-ttu-id="32011-149">Kann höchstens einmal für jedes [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md)-, [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)-, [**Command. KeyTip**](windowsribbon-element-command-keytip.md)-, [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)-oder [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="32011-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="32011-150">Die Zeichen folgen Definition wird der Menüband-Header Datei hinzugefügt, z `#define strSave 59999` . b..</span><span class="sxs-lookup"><span data-stu-id="32011-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="32011-151">Die Zeichenfolge wird einer Zeichen folgen Tabelle in der Ressourcen Datei des Menübands hinzugefügt, in der ein Name und eine ID vom Menüband-Framework generiert werden, wenn keine deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="32011-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="32011-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32011-152">Examples</span></span>

<span data-ttu-id="32011-153">Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **Zeichen** folgen Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="32011-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="32011-154">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="32011-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="32011-155">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="32011-155">Minimum supported system</span></span><br/> | <span data-ttu-id="32011-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32011-156">Windows 7</span></span> |
| <span data-ttu-id="32011-157">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="32011-157">Can be empty</span></span>                        | <span data-ttu-id="32011-158">Nein</span><span class="sxs-lookup"><span data-stu-id="32011-158">No</span></span>        |



 

 





