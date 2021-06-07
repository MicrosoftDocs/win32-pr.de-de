---
title: String-Element
description: Stellt eine Zeichenfolgenressource dar.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Windows-Menüband für Zeichenfolgenelement
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443901"
---
# <a name="string-element"></a><span data-ttu-id="b4e30-104">String-Element</span><span class="sxs-lookup"><span data-stu-id="b4e30-104">String element</span></span>

<span data-ttu-id="b4e30-105">Stellt eine Zeichenfolgenressource dar.</span><span class="sxs-lookup"><span data-stu-id="b4e30-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="b4e30-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b4e30-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="b4e30-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4e30-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4e30-108">attribute</span><span class="sxs-lookup"><span data-stu-id="b4e30-108">Attribute</span></span></th>
<th><span data-ttu-id="b4e30-109">Typ</span><span class="sxs-lookup"><span data-stu-id="b4e30-109">Type</span></span></th>
<th><span data-ttu-id="b4e30-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e30-110">Required</span></span></th>
<th><span data-ttu-id="b4e30-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4e30-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4e30-112"><strong>Inhalt</strong></span><span class="sxs-lookup"><span data-stu-id="b4e30-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="b4e30-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4e30-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="b4e30-114">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e30-114">No</span></span><br/></td>
<td><span data-ttu-id="b4e30-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="b4e30-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b4e30-116">Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.</span><span class="sxs-lookup"><span data-stu-id="b4e30-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4e30-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="b4e30-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="b4e30-118">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="b4e30-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b4e30-119">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e30-119">No</span></span><br/></td>
<td><span data-ttu-id="b4e30-120">Die eindeutige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b4e30-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="b4e30-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="b4e30-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b4e30-122">Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="b4e30-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="b4e30-123">Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.</span><span class="sxs-lookup"><span data-stu-id="b4e30-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4e30-124"><strong>Symbol</strong></span><span class="sxs-lookup"><span data-stu-id="b4e30-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="b4e30-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4e30-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="b4e30-126">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e30-126">No</span></span><br/></td>
<td><span data-ttu-id="b4e30-127">Das Ressourcensymbol für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b4e30-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="b4e30-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="b4e30-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b4e30-129">Ein Buchstabe oder Unterstrich, gefolgt von einer beliebigen Sequenz von Buchstaben, Ziffern oder Unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="b4e30-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="b4e30-130">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b4e30-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b4e30-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e30-131">Child elements</span></span>



| <span data-ttu-id="b4e30-132">Element</span><span class="sxs-lookup"><span data-stu-id="b4e30-132">Element</span></span>                                                                   | <span data-ttu-id="b4e30-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4e30-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b4e30-134">**String.Content**</span><span class="sxs-lookup"><span data-stu-id="b4e30-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="b4e30-135">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="b4e30-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b4e30-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="b4e30-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="b4e30-137">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="b4e30-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="b4e30-138">**String.Symbol**</span><span class="sxs-lookup"><span data-stu-id="b4e30-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="b4e30-139">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="b4e30-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b4e30-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e30-140">Parent elements</span></span>



| <span data-ttu-id="b4e30-141">Element</span><span class="sxs-lookup"><span data-stu-id="b4e30-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4e30-142">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="b4e30-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="b4e30-143">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="b4e30-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="b4e30-144">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="b4e30-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="b4e30-145">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="b4e30-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="b4e30-146">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="b4e30-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="b4e30-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4e30-147">Remarks</span></span>

<span data-ttu-id="b4e30-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="b4e30-148">Optional.</span></span>

<span data-ttu-id="b4e30-149">Kann höchstens einmal für jedes [**Command.LabelTitle-,**](windowsribbon-element-command-labeltitle.md) [**Command.LabelDescription-,**](windowsribbon-element-command-labeldescription.md) [**Command.Keytip-,**](windowsribbon-element-command-keytip.md) [**Command.TooltipTitle-**](windowsribbon-element-command-tooltiptitle.md)oder [**Command.TooltipDescription-Element**](windowsribbon-element-command-tooltipdescription.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="b4e30-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="b4e30-150">Die Zeichenfolgendefinition wird der Menübandheaderdatei hinzugefügt, z. `#define strSave 59999` B. .</span><span class="sxs-lookup"><span data-stu-id="b4e30-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="b4e30-151">Die Zeichenfolge wird einer Zeichenfolgentabelle in der Menübandressourcendatei hinzugefügt, in der ein Name und eine ID vom Menübandframework generiert werden, wenn keine deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="b4e30-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="b4e30-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4e30-152">Examples</span></span>

<span data-ttu-id="b4e30-153">Im folgenden Beispiel wird das Markup für ein [**Command.LabelTitle-Element**](windowsribbon-element-command-labeltitle.md) mit einer **String-Deklaration** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b4e30-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="b4e30-154">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b4e30-154">Element information</span></span>

- <span data-ttu-id="b4e30-155">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4e30-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="b4e30-156">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="b4e30-156">**Can be empty**: No</span></span>



 

 





