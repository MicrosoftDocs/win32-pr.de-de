---
description: Fügt eine C-oder IDL-include-Anweisung in den generierten Code ein.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalinclude-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356206"
---
# <a name="literalinclude-element"></a><span data-ttu-id="15072-103">literalinclude-Element</span><span class="sxs-lookup"><span data-stu-id="15072-103">literalInclude element</span></span>

<span data-ttu-id="15072-104">Fügt eine C-oder IDL-include-Anweisung in den generierten Code ein.</span><span class="sxs-lookup"><span data-stu-id="15072-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="15072-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="15072-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="15072-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="15072-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15072-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="15072-107">Attribute</span></span></th>
<th><span data-ttu-id="15072-108">type</span><span class="sxs-lookup"><span data-stu-id="15072-108">Type</span></span></th>
<th><span data-ttu-id="15072-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="15072-109">Required</span></span></th>
<th><span data-ttu-id="15072-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15072-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15072-111"><strong>Sprache</strong></span><span class="sxs-lookup"><span data-stu-id="15072-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="15072-112">sprach Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15072-112">language string</span></span><br/></td>
<td><span data-ttu-id="15072-113">Nein</span><span class="sxs-lookup"><span data-stu-id="15072-113">No</span></span><br/></td>
<td><span data-ttu-id="15072-114">Der Typ der Header Datei, die eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="15072-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="15072-115">
<dt><strong>Scher</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="15072-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="15072-116">Fügen Sie eine C-Header Datei ein.</span><span class="sxs-lookup"><span data-stu-id="15072-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="15072-117"><dt><strong>IDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="15072-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="15072-118">Fügen Sie eine IDL-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="15072-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15072-119"><strong>Lokal</strong></span><span class="sxs-lookup"><span data-stu-id="15072-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="15072-120">Boolesch</span><span class="sxs-lookup"><span data-stu-id="15072-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="15072-121">Nein</span><span class="sxs-lookup"><span data-stu-id="15072-121">No</span></span><br/></td>
<td><span data-ttu-id="15072-122">Dieses Attribut wird nur verwendet, wenn <strong>Language</strong> auf C festgelegt ist &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="15072-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="15072-123">
<dt><strong>Fall</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="15072-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="15072-124">Durchsucht das aktuelle Verzeichnis nach dem benannten Header, bevor die Systemverzeichnisse durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="15072-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="15072-125"><dt><strong>Alarm</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="15072-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="15072-126">Systemverzeichnisse werden nur nach dem benannten Header durchsucht.</span><span class="sxs-lookup"><span data-stu-id="15072-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="15072-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15072-127">Child elements</span></span>

<span data-ttu-id="15072-128">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="15072-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="15072-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15072-129">Parent elements</span></span>



| <span data-ttu-id="15072-130">Element</span><span class="sxs-lookup"><span data-stu-id="15072-130">Element</span></span>                         | <span data-ttu-id="15072-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15072-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="15072-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="15072-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="15072-133">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="15072-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="15072-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15072-134">Remarks</span></span>

<span data-ttu-id="15072-135">In den folgenden Beispielen wird der Code gezeigt, der aus verschiedenen **literalinclude** -Elementen generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="15072-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="15072-136">Beispiel 1: Erstellen einer C include-Anweisung</span><span class="sxs-lookup"><span data-stu-id="15072-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="15072-137">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="15072-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="15072-138">Ausgabe Code:</span><span class="sxs-lookup"><span data-stu-id="15072-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="15072-139">Beispiel 2: Erstellen einer C include-Anweisung</span><span class="sxs-lookup"><span data-stu-id="15072-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="15072-140">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="15072-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="15072-141">Ausgabe Code:</span><span class="sxs-lookup"><span data-stu-id="15072-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="15072-142">Beispiel 3: Erstellen einer IDL-Import Anweisung</span><span class="sxs-lookup"><span data-stu-id="15072-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="15072-143">Eingabe-XML:</span><span class="sxs-lookup"><span data-stu-id="15072-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="15072-144">Ausgabe Code:</span><span class="sxs-lookup"><span data-stu-id="15072-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="15072-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15072-145">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="15072-146">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="15072-146">Minimum supported system</span></span><br/> | <span data-ttu-id="15072-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15072-147">Windows Vista</span></span> |
| <span data-ttu-id="15072-148">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="15072-148">Can be empty</span></span>                        | <span data-ttu-id="15072-149">Ja</span><span class="sxs-lookup"><span data-stu-id="15072-149">Yes</span></span>           |



 

 




