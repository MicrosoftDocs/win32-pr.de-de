---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353280"
---
# <a name="scoredproperty"></a><span data-ttu-id="7eca8-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="7eca8-104">ScoredProperty</span></span>

<span data-ttu-id="7eca8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7eca8-105">This topic is not current.</span></span> <span data-ttu-id="7eca8-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7eca8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7eca8-107">Ein ScoredProperty-Element deklariert eine Eigenschaft, die in einer Options Definition intrinsisch ist.</span><span class="sxs-lookup"><span data-stu-id="7eca8-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="7eca8-108">Diese Eigenschaften sollten verglichen werden, wenn ausgewertet wird, wie eng eine angeforderte Option mit einer Geräte gestützten Option übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7eca8-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="7eca8-109">Elementtag</span><span class="sxs-lookup"><span data-stu-id="7eca8-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="7eca8-110">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="7eca8-110">XML Attributes</span></span>

<span data-ttu-id="7eca8-111">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="7eca8-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="7eca8-112">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="7eca8-112">XML Attribute</span></span>   | <span data-ttu-id="7eca8-113">Details</span><span class="sxs-lookup"><span data-stu-id="7eca8-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eca8-114">name</span><span class="sxs-lookup"><span data-stu-id="7eca8-114">name</span></span><br/> | <span data-ttu-id="7eca8-115">Enthält das Name-Attribut der ScoredProperty, entweder eine Standard Eigenschaft oder eine privat definierte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7eca8-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="7eca8-116">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="7eca8-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="7eca8-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7eca8-117">Element Information</span></span>

<span data-ttu-id="7eca8-118">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="7eca8-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="7eca8-119">Category</span><span class="sxs-lookup"><span data-stu-id="7eca8-119">Category</span></span>                   | <span data-ttu-id="7eca8-120">Details</span><span class="sxs-lookup"><span data-stu-id="7eca8-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eca8-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7eca8-121">Parent elements</span></span><br/> | <span data-ttu-id="7eca8-122">*Option*</span><span class="sxs-lookup"><span data-stu-id="7eca8-122">*Option*</span></span><br/> <span data-ttu-id="7eca8-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="7eca8-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="7eca8-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7eca8-124">Child elements</span></span><br/>  | <span data-ttu-id="7eca8-125">Sowohl als auch</span><span class="sxs-lookup"><span data-stu-id="7eca8-125">Either</span></span><br/> <span data-ttu-id="7eca8-126">*ParameterRef* (eins)</span><span class="sxs-lookup"><span data-stu-id="7eca8-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="7eca8-127">oder</span><span class="sxs-lookup"><span data-stu-id="7eca8-127">or</span></span><br/> <span data-ttu-id="7eca8-128">*Wert* (eins)</span><span class="sxs-lookup"><span data-stu-id="7eca8-128">*Value* (one)</span></span><br/> <span data-ttu-id="7eca8-129">*Property* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="7eca8-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="7eca8-130">*ScoredProperty* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="7eca8-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="7eca8-131">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="7eca8-131">This element</span></span><br/>    | <span data-ttu-id="7eca8-132">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="7eca8-132">No character data is permitted.</span></span><br/> <span data-ttu-id="7eca8-133">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="7eca8-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="7eca8-134">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="7eca8-134">Configuration Dependencies</span></span>

<span data-ttu-id="7eca8-135">Ein ScoredProperty-Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="7eca8-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="7eca8-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7eca8-136">Example</span></span>

<span data-ttu-id="7eca8-137">Deklarieren Sie ein ScoredProperty-Element mit dem Namen mediasizewidth mit dem Wert 11.</span><span class="sxs-lookup"><span data-stu-id="7eca8-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="7eca8-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7eca8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eca8-139">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="7eca8-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




