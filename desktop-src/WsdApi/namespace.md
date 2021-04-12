---
description: Beschreibt einen Namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: Namespace-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528580"
---
# <a name="namespace-element"></a><span data-ttu-id="e17d9-103">Namespace-Element</span><span class="sxs-lookup"><span data-stu-id="e17d9-103">nameSpace element</span></span>

<span data-ttu-id="e17d9-104">Beschreibt einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="e17d9-104">Describes a namespace.</span></span> <span data-ttu-id="e17d9-105">Dieser Namespace kann für die Codegenerierung oder für die Behandlung von <WSDL: Import-> Direktiven verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e17d9-105">This namespace may be used for code generation or for handling <wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="e17d9-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e17d9-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="e17d9-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="e17d9-107">Attributes</span></span>



| <span data-ttu-id="e17d9-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e17d9-108">Attribute</span></span>          | <span data-ttu-id="e17d9-109">type</span><span class="sxs-lookup"><span data-stu-id="e17d9-109">Type</span></span>                         | <span data-ttu-id="e17d9-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e17d9-110">Required</span></span>       | <span data-ttu-id="e17d9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e17d9-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="e17d9-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="e17d9-112">**uri**</span></span><br/> | <span data-ttu-id="e17d9-113">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="e17d9-113">character\_string</span></span><br/> | <span data-ttu-id="e17d9-114">Ja</span><span class="sxs-lookup"><span data-stu-id="e17d9-114">Yes</span></span><br/> | <span data-ttu-id="e17d9-115">Der eindeutige URI des Namespace.</span><span class="sxs-lookup"><span data-stu-id="e17d9-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="e17d9-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e17d9-116">Child elements</span></span>



| <span data-ttu-id="e17d9-117">Element</span><span class="sxs-lookup"><span data-stu-id="e17d9-117">Element</span></span>                                               | <span data-ttu-id="e17d9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e17d9-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e17d9-119">**codeName**</span><span class="sxs-lookup"><span data-stu-id="e17d9-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="e17d9-120">Der Name, der zum Identifizieren des Namespace in generiertem Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17d9-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="e17d9-121">**makroprefix**</span><span class="sxs-lookup"><span data-stu-id="e17d9-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="e17d9-122">Das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17d9-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="e17d9-123">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="e17d9-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="e17d9-124">Ein qualifizierter Name im-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e17d9-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="e17d9-125">**preferredprefix**</span><span class="sxs-lookup"><span data-stu-id="e17d9-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="e17d9-126">Das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.</span><span class="sxs-lookup"><span data-stu-id="e17d9-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="e17d9-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="e17d9-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="e17d9-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e17d9-128">Parent elements</span></span>



| <span data-ttu-id="e17d9-129">Element</span><span class="sxs-lookup"><span data-stu-id="e17d9-129">Element</span></span>                                     | <span data-ttu-id="e17d9-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e17d9-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e17d9-131">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="e17d9-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="e17d9-132">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="e17d9-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e17d9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e17d9-133">Remarks</span></span>

<span data-ttu-id="e17d9-134">Dieses Element kann verwendet werden, um dem Code Generator zusätzliche Informationen zu Namespaces, die in WSDL-und XSD-Dateien auftreten, oder zum Einführen neuer Namespaces bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e17d9-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="e17d9-135">Namespaces, die durch eine Typreflektion oder in WSDL-und XSD-Dateien angegeben werden, werden automatisch vom Code-Generator analysiert und müssen nicht explizit im Skript definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e17d9-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="e17d9-136">In einigen Fällen kann dieses Element verwendet werden, um einem Namespace, auf den von der Typreflektion oder WSDL/XSD verwiesen wird, zusätzliche Eigenschaften oder Namen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e17d9-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="e17d9-137">Der Code-Generator berücksichtigt dies nicht als Konflikt.</span><span class="sxs-lookup"><span data-stu-id="e17d9-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="e17d9-138">Der folgende XML-Code zeigt ein Namespace-Element (mit untergeordneten Elementen, die ausgelassen werden).</span><span class="sxs-lookup"><span data-stu-id="e17d9-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="e17d9-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e17d9-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e17d9-140">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="e17d9-140">Minimum supported system</span></span><br/> | <span data-ttu-id="e17d9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e17d9-141">Windows Vista</span></span> |
| <span data-ttu-id="e17d9-142">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="e17d9-142">Can be empty</span></span>                        | <span data-ttu-id="e17d9-143">Ja</span><span class="sxs-lookup"><span data-stu-id="e17d9-143">Yes</span></span>           |



 

 




