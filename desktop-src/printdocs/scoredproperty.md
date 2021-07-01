---
description: Hier finden Sie Informationen zum ScoredProperty-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119115"
---
# <a name="scoredproperty"></a><span data-ttu-id="dee5c-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="dee5c-105">ScoredProperty</span></span>

<span data-ttu-id="dee5c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="dee5c-106">This topic is not current.</span></span> <span data-ttu-id="dee5c-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="dee5c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dee5c-108">Ein ScoredProperty-Element deklariert eine Eigenschaft, die für eine Optionsdefinition intrinsisch ist.</span><span class="sxs-lookup"><span data-stu-id="dee5c-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="dee5c-109">Solche Eigenschaften sollten verglichen werden, wenn bewertet wird, wie genau eine angeforderte Option mit einer vom Gerät unterstützten Option abglichen wird.</span><span class="sxs-lookup"><span data-stu-id="dee5c-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="dee5c-110">Elementtag</span><span class="sxs-lookup"><span data-stu-id="dee5c-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="dee5c-111">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="dee5c-111">XML Attributes</span></span>

<span data-ttu-id="dee5c-112">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.</span><span class="sxs-lookup"><span data-stu-id="dee5c-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="dee5c-113">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="dee5c-113">XML Attribute</span></span>   | <span data-ttu-id="dee5c-114">Details</span><span class="sxs-lookup"><span data-stu-id="dee5c-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee5c-115">name</span><span class="sxs-lookup"><span data-stu-id="dee5c-115">name</span></span><br/> | <span data-ttu-id="dee5c-116">Enthält das Namensattribut der ScoredProperty, entweder eine Standardeigenschaft oder eine privat definierte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dee5c-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="dee5c-117">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="dee5c-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="dee5c-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dee5c-118">Element Information</span></span>

<span data-ttu-id="dee5c-119">In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dee5c-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="dee5c-120">Category</span><span class="sxs-lookup"><span data-stu-id="dee5c-120">Category</span></span>                   | <span data-ttu-id="dee5c-121">Details</span><span class="sxs-lookup"><span data-stu-id="dee5c-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee5c-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dee5c-122">Parent elements</span></span><br/> | <span data-ttu-id="dee5c-123">*Option*</span><span class="sxs-lookup"><span data-stu-id="dee5c-123">*Option*</span></span><br/> <span data-ttu-id="dee5c-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="dee5c-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="dee5c-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dee5c-125">Child elements</span></span><br/>  | <span data-ttu-id="dee5c-126">Sowohl als auch</span><span class="sxs-lookup"><span data-stu-id="dee5c-126">Either</span></span><br/> <span data-ttu-id="dee5c-127">*ParameterRef* (eins)</span><span class="sxs-lookup"><span data-stu-id="dee5c-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="dee5c-128">oder</span><span class="sxs-lookup"><span data-stu-id="dee5c-128">or</span></span><br/> <span data-ttu-id="dee5c-129">*Wert* (eins)</span><span class="sxs-lookup"><span data-stu-id="dee5c-129">*Value* (one)</span></span><br/> <span data-ttu-id="dee5c-130">*Eigenschaft* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="dee5c-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="dee5c-131">*ScoredProperty* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="dee5c-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="dee5c-132">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="dee5c-132">This element</span></span><br/>    | <span data-ttu-id="dee5c-133">Zeichendaten sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="dee5c-133">No character data is permitted.</span></span><br/> <span data-ttu-id="dee5c-134">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="dee5c-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="dee5c-135">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="dee5c-135">Configuration Dependencies</span></span>

<span data-ttu-id="dee5c-136">Ein ScoredProperty-Element hat möglicherweise keine Konfigurationsabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="dee5c-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="dee5c-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dee5c-137">Example</span></span>

<span data-ttu-id="dee5c-138">Deklarieren Sie ein ScoredProperty-Element mit dem Namen MediaSizeWidth mit dem Wert 11.</span><span class="sxs-lookup"><span data-stu-id="dee5c-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="dee5c-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dee5c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dee5c-140">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="dee5c-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




