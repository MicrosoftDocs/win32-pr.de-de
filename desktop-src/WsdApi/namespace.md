---
description: Beschreibt einen Namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3e2735efbb99fbe404f2531336c2e2bd0f89d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994277"
---
# <a name="namespace-element"></a><span data-ttu-id="4e8a0-103">nameSpace-Element</span><span class="sxs-lookup"><span data-stu-id="4e8a0-103">nameSpace element</span></span>

<span data-ttu-id="4e8a0-104">Beschreibt einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-104">Describes a namespace.</span></span> <span data-ttu-id="4e8a0-105">Dieser Namespace kann für die Codegenerierung oder für die Behandlung von -Anweisungen verwendet \<wsdl:import> werden.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-105">This namespace may be used for code generation or for handling \<wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="4e8a0-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4e8a0-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="4e8a0-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="4e8a0-107">Attributes</span></span>



| <span data-ttu-id="4e8a0-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="4e8a0-108">Attribute</span></span>          | <span data-ttu-id="4e8a0-109">type</span><span class="sxs-lookup"><span data-stu-id="4e8a0-109">Type</span></span>                         | <span data-ttu-id="4e8a0-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4e8a0-110">Required</span></span>       | <span data-ttu-id="4e8a0-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e8a0-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="4e8a0-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-112">**uri**</span></span><br/> | <span data-ttu-id="4e8a0-113">Zeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="4e8a0-113">character\_string</span></span><br/> | <span data-ttu-id="4e8a0-114">Ja</span><span class="sxs-lookup"><span data-stu-id="4e8a0-114">Yes</span></span><br/> | <span data-ttu-id="4e8a0-115">Der eindeutige URI des Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="4e8a0-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e8a0-116">Child elements</span></span>



| <span data-ttu-id="4e8a0-117">Element</span><span class="sxs-lookup"><span data-stu-id="4e8a0-117">Element</span></span>                                               | <span data-ttu-id="4e8a0-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e8a0-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e8a0-119">**Codename**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="4e8a0-120">Der Name, der verwendet werden soll, um den Namespace im generierten Code zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="4e8a0-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="4e8a0-122">Das Präfix, das im generierten Code für Namen von Makros im Namespace verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="4e8a0-123">**Namen**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="4e8a0-124">Ein qualifizierter Name im Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="4e8a0-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="4e8a0-126">Das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="4e8a0-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="4e8a0-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="4e8a0-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e8a0-128">Parent elements</span></span>



| <span data-ttu-id="4e8a0-129">Element</span><span class="sxs-lookup"><span data-stu-id="4e8a0-129">Element</span></span>                                     | <span data-ttu-id="4e8a0-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e8a0-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e8a0-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="4e8a0-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="4e8a0-132">Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4e8a0-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e8a0-133">Remarks</span></span>

<span data-ttu-id="4e8a0-134">Dieses Element kann verwendet werden, um dem Codegenerator zusätzliche Informationen zu Namespaces bereitzustellen, die in WSDL- und XSD-Dateien auftreten, oder um neue Namespaces einzuführen.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="4e8a0-135">Namespaces, die durch Typreflektion impliziert oder in WSDL- und XSD-Dateien angegeben sind, werden automatisch vom Codegenerator analysiert und müssen nicht explizit im Skript definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="4e8a0-136">In einigen Fällen kann dieses Element verwendet werden, um einem Namespace, auf den durch Typreflektion oder WSDL/XSD verwiesen wird, zusätzliche Eigenschaften oder Namen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="4e8a0-137">Der Codegenerator betrachtet dies nicht als Konflikt.</span><span class="sxs-lookup"><span data-stu-id="4e8a0-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="4e8a0-138">Der folgende XML-Code zeigt ein nameSpace-Element (bei dem aus Kürze die unteren Elemente weggelassen werden).</span><span class="sxs-lookup"><span data-stu-id="4e8a0-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="4e8a0-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4e8a0-139">Element information</span></span>



| <span data-ttu-id="4e8a0-140">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="4e8a0-140">Label</span></span> | <span data-ttu-id="4e8a0-141">Wert</span><span class="sxs-lookup"><span data-stu-id="4e8a0-141">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="4e8a0-142">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4e8a0-142">Minimum supported system</span></span><br/> | <span data-ttu-id="4e8a0-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e8a0-143">Windows Vista</span></span> |
| <span data-ttu-id="4e8a0-144">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4e8a0-144">Can be empty</span></span>                        | <span data-ttu-id="4e8a0-145">Ja</span><span class="sxs-lookup"><span data-stu-id="4e8a0-145">Yes</span></span>           |



 

 




