---
description: Platziert eine C- oder IDL-Include-Anweisung im generierten Code.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995127"
---
# <a name="literalinclude-element"></a><span data-ttu-id="afa01-103">literalInclude-Element</span><span class="sxs-lookup"><span data-stu-id="afa01-103">literalInclude element</span></span>

<span data-ttu-id="afa01-104">Platziert eine C- oder IDL-Include-Anweisung im generierten Code.</span><span class="sxs-lookup"><span data-stu-id="afa01-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="afa01-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="afa01-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="afa01-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="afa01-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afa01-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="afa01-107">Attribute</span></span></th>
<th><span data-ttu-id="afa01-108">type</span><span class="sxs-lookup"><span data-stu-id="afa01-108">Type</span></span></th>
<th><span data-ttu-id="afa01-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="afa01-109">Required</span></span></th>
<th><span data-ttu-id="afa01-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afa01-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="afa01-111"><strong>Sprache</strong></span><span class="sxs-lookup"><span data-stu-id="afa01-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="afa01-112">Sprachzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="afa01-112">language string</span></span><br/></td>
<td><span data-ttu-id="afa01-113">Nein</span><span class="sxs-lookup"><span data-stu-id="afa01-113">No</span></span><br/></td>
<td><span data-ttu-id="afa01-114">Der Typ der header-Datei, die eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="afa01-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="afa01-115">
<dt><strong>C</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afa01-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="afa01-116">Schließen Sie eine C-Headerdatei ein.</span><span class="sxs-lookup"><span data-stu-id="afa01-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="afa01-117"><dt><strong>Idl</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afa01-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="afa01-118">Schließen Sie eine IDL-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="afa01-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afa01-119"><strong>Lokal</strong></span><span class="sxs-lookup"><span data-stu-id="afa01-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="afa01-120">Boolesch</span><span class="sxs-lookup"><span data-stu-id="afa01-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="afa01-121">Nein</span><span class="sxs-lookup"><span data-stu-id="afa01-121">No</span></span><br/></td>
<td><span data-ttu-id="afa01-122">Dieses Attribut wird nur verwendet, wenn <strong>Language</strong> auf C festgelegt &quot; &quot; ist.</span><span class="sxs-lookup"><span data-stu-id="afa01-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="afa01-123">
<dt><strong>STIMMT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afa01-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="afa01-124">Durchsucht das aktuelle Verzeichnis nach dem benannten Header, bevor die Systemverzeichnisse durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="afa01-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="afa01-125"><dt><strong>FALSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afa01-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="afa01-126">Durchsuchen Sie nur Systemverzeichnisse nach dem benannten Header.</span><span class="sxs-lookup"><span data-stu-id="afa01-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="afa01-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afa01-127">Child elements</span></span>

<span data-ttu-id="afa01-128">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="afa01-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="afa01-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afa01-129">Parent elements</span></span>



| <span data-ttu-id="afa01-130">Element</span><span class="sxs-lookup"><span data-stu-id="afa01-130">Element</span></span>                         | <span data-ttu-id="afa01-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afa01-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="afa01-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="afa01-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="afa01-133">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="afa01-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="afa01-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="afa01-134">Remarks</span></span>

<span data-ttu-id="afa01-135">Die folgenden Beispiele zeigen den Code, der aus verschiedenen **literalInclude-Elementen** generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="afa01-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="afa01-136">Beispiel 1: Generieren einer C-Include-Anweisung</span><span class="sxs-lookup"><span data-stu-id="afa01-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="afa01-137">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="afa01-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="afa01-138">Ausgabecode:</span><span class="sxs-lookup"><span data-stu-id="afa01-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="afa01-139">Beispiel 2: Generieren einer Include-Anweisung in C</span><span class="sxs-lookup"><span data-stu-id="afa01-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="afa01-140">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="afa01-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="afa01-141">Ausgabecode:</span><span class="sxs-lookup"><span data-stu-id="afa01-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="afa01-142">Beispiel 3: Generieren einer IDL-Import-Anweisung</span><span class="sxs-lookup"><span data-stu-id="afa01-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="afa01-143">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="afa01-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="afa01-144">Ausgabecode:</span><span class="sxs-lookup"><span data-stu-id="afa01-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="afa01-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="afa01-145">Element information</span></span>



| <span data-ttu-id="afa01-146">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="afa01-146">Label</span></span> | <span data-ttu-id="afa01-147">Wert</span><span class="sxs-lookup"><span data-stu-id="afa01-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="afa01-148">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="afa01-148">Minimum supported system</span></span><br/> | <span data-ttu-id="afa01-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afa01-149">Windows Vista</span></span> |
| <span data-ttu-id="afa01-150">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="afa01-150">Can be empty</span></span>                        | <span data-ttu-id="afa01-151">Ja</span><span class="sxs-lookup"><span data-stu-id="afa01-151">Yes</span></span>           |



 

 




