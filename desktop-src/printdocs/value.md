---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370353"
---
# <a name="value"></a><span data-ttu-id="d3668-104">Wert</span><span class="sxs-lookup"><span data-stu-id="d3668-104">Value</span></span>

<span data-ttu-id="d3668-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d3668-105">This topic is not current.</span></span> <span data-ttu-id="d3668-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d3668-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d3668-107">Ein Value-Element ordnet ein Literale einem Typ zu.</span><span class="sxs-lookup"><span data-stu-id="d3668-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d3668-108">Elementtag</span><span class="sxs-lookup"><span data-stu-id="d3668-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="d3668-109">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="d3668-109">XML Attributes</span></span>

<span data-ttu-id="d3668-110">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="d3668-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d3668-111">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="d3668-111">XML Attribute</span></span>       | <span data-ttu-id="d3668-112">Details</span><span class="sxs-lookup"><span data-stu-id="d3668-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3668-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d3668-113">xsi:type</span></span><br/> | <span data-ttu-id="d3668-114">Gibt den Datentyp des Werts an, bei dem es sich um einen der folgenden XSD-definierten Typen handeln muss: String, Integer, Decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="d3668-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="d3668-115">Wenn Sie nicht vorhanden ist, ist der Standard Datentyp String.</span><span class="sxs-lookup"><span data-stu-id="d3668-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="d3668-116">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d3668-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d3668-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d3668-117">Element Information</span></span>

<span data-ttu-id="d3668-118">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="d3668-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="d3668-119">Category</span><span class="sxs-lookup"><span data-stu-id="d3668-119">Category</span></span>                   | <span data-ttu-id="d3668-120">Details</span><span class="sxs-lookup"><span data-stu-id="d3668-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3668-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3668-121">Parent elements</span></span><br/> | <span data-ttu-id="d3668-122">Parameterinit</span><span class="sxs-lookup"><span data-stu-id="d3668-122">ParameterInit</span></span> <br/> <span data-ttu-id="d3668-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d3668-123">Property</span></span><br/> <span data-ttu-id="d3668-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="d3668-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="d3668-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3668-125">Child elements</span></span><br/>  | <span data-ttu-id="d3668-126">Nur Zeichen-oder ganzzahlige Inhalte sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="d3668-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="d3668-127">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="d3668-127">This element</span></span><br/>    | <span data-ttu-id="d3668-128">NULL-Inhalt ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="d3668-128">Null content is allowed.</span></span> <span data-ttu-id="d3668-129">Der Zeichen Inhalt muss der durch den-Datentyp definierten Syntax entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d3668-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="d3668-130">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d3668-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d3668-131">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="d3668-131">Configuration Dependencies</span></span>

<span data-ttu-id="d3668-132">Werte Elemente, die im ScoredProperty-Element angezeigt werden, verfügen möglicherweise nicht über Konfigurations Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d3668-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="d3668-133">Werte Elemente, die innerhalb von Eigenschafts Elementen angezeigt werden, haben möglicherweise beliebige Abhängigkeiten von der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d3668-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="d3668-134">Element Verwendung</span><span class="sxs-lookup"><span data-stu-id="d3668-134">Element Usage</span></span>

<span data-ttu-id="d3668-135">Ein Value-Element kann in einer Eigenschaft oder einem ScoredProperty-Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d3668-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="d3668-136">Der Zweck des Value-Elements ist die Darstellung eines Werts als Standard-XML-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="d3668-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="d3668-137">Der-Datentyp wird als XML-Attribut des Value-Elements, xsi: Type, angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3668-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="d3668-138">Beachten Sie, dass nicht alle XSD-definierten oder XML-definierten Typen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d3668-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="d3668-139">Eine Liste der unterstützten Typen finden Sie unter [Zusammenfassung der Element Typen](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="d3668-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="d3668-140">Ein Value-Element kann nur Zeichen Inhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3668-140">A Value element can contain only character content.</span></span> <span data-ttu-id="d3668-141">In einem Value-Element kann nichts anderes als Inhalt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3668-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="d3668-142">Einige vom Druck Schema definierte Eigenschaft und ScoredProperty-Elemente enthalten kein Value-Element, da ihr Zweck lediglich übergeordnete Elemente von untergeordneten Eigenschaften ist.</span><span class="sxs-lookup"><span data-stu-id="d3668-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="d3668-143">Sie sollten diesen Eigenschaften nicht ein Value-Element hinzufügen, da diese Eigenschaften nicht ein Value-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3668-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="d3668-144">Um dem Print Schema-Framework zu entsprechen, das entweder ein Value-Element oder unter Elemente in den Elementen enthalten muss, die-Werte unterstützen, sollte ein fehlender oder nicht definierter Wert durch Darstellung des Value-Elements als leeres Element dargestellt werden. Das heißt, als</span><span class="sxs-lookup"><span data-stu-id="d3668-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="d3668-145">.</span><span class="sxs-lookup"><span data-stu-id="d3668-145">.</span></span>

## <a name="example"></a><span data-ttu-id="d3668-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3668-146">Example</span></span>

<span data-ttu-id="d3668-147">Definieren Sie einen Wert vom Typ Decimal, und initialisieren Sie ihn mit "128,5".</span><span class="sxs-lookup"><span data-stu-id="d3668-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="d3668-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3668-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3668-149">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="d3668-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




