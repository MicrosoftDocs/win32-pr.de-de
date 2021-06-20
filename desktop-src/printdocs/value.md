---
description: Erfahren Sie mehr über das Value-Element, das einem Typ ein Literal zuteilt. Der Datentyp von Value muss string, integer, decimal oder QName sein.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405983"
---
# <a name="value"></a><span data-ttu-id="b78dc-104">Wert</span><span class="sxs-lookup"><span data-stu-id="b78dc-104">Value</span></span>

<span data-ttu-id="b78dc-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b78dc-105">This topic is not current.</span></span> <span data-ttu-id="b78dc-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b78dc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b78dc-107">Ein Value-Element ordnet einem Typ ein Literal zu.</span><span class="sxs-lookup"><span data-stu-id="b78dc-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="b78dc-108">Elementtag</span><span class="sxs-lookup"><span data-stu-id="b78dc-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="b78dc-109">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="b78dc-109">XML Attributes</span></span>

<span data-ttu-id="b78dc-110">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.</span><span class="sxs-lookup"><span data-stu-id="b78dc-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="b78dc-111">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="b78dc-111">XML Attribute</span></span>       | <span data-ttu-id="b78dc-112">Details</span><span class="sxs-lookup"><span data-stu-id="b78dc-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78dc-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b78dc-113">xsi:type</span></span><br/> | <span data-ttu-id="b78dc-114">Gibt den Datentyp von Value an, bei dem es sich um einen der folgenden XSD-definierten Typen handelt: string, integer, decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="b78dc-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="b78dc-115">Wenn der Datentyp fehlt, ist der Standarddatentyp string.</span><span class="sxs-lookup"><span data-stu-id="b78dc-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="b78dc-116">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="b78dc-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="b78dc-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b78dc-117">Element Information</span></span>

<span data-ttu-id="b78dc-118">In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b78dc-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="b78dc-119">Category</span><span class="sxs-lookup"><span data-stu-id="b78dc-119">Category</span></span>                   | <span data-ttu-id="b78dc-120">Details</span><span class="sxs-lookup"><span data-stu-id="b78dc-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78dc-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b78dc-121">Parent elements</span></span><br/> | <span data-ttu-id="b78dc-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="b78dc-122">ParameterInit</span></span> <br/> <span data-ttu-id="b78dc-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b78dc-123">Property</span></span><br/> <span data-ttu-id="b78dc-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="b78dc-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="b78dc-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b78dc-125">Child elements</span></span><br/>  | <span data-ttu-id="b78dc-126">Nur Zeichen- oder Ganzzahlinhalte sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="b78dc-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="b78dc-127">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="b78dc-127">This element</span></span><br/>    | <span data-ttu-id="b78dc-128">NULL-Inhalt ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b78dc-128">Null content is allowed.</span></span> <span data-ttu-id="b78dc-129">Der Zeicheninhalt muss der vom Datentyp definierten Syntax entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b78dc-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="b78dc-130">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b78dc-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="b78dc-131">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="b78dc-131">Configuration Dependencies</span></span>

<span data-ttu-id="b78dc-132">Wertelemente, die im ScoredProperty-Element angezeigt werden, verfügen möglicherweise nicht über Konfigurationsabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="b78dc-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="b78dc-133">Wertelemente, die in Property-Elementen angezeigt werden, können beliebige Abhängigkeiten von der Konfiguration aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b78dc-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="b78dc-134">Elementverwendung</span><span class="sxs-lookup"><span data-stu-id="b78dc-134">Element Usage</span></span>

<span data-ttu-id="b78dc-135">Ein Value-Element kann innerhalb eines Property- oder ScoredProperty-Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b78dc-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="b78dc-136">Der Zweck des Value-Elements besteht in der Darstellung eines Werts als XML-Standarddatentyp.</span><span class="sxs-lookup"><span data-stu-id="b78dc-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="b78dc-137">Der Datentyp wird als XML-Attribut des Value-Elements xsi:type angegeben.</span><span class="sxs-lookup"><span data-stu-id="b78dc-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="b78dc-138">Beachten Sie, dass nicht alle XSD-definierten oder XML-definierten Typen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b78dc-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="b78dc-139">Eine Liste der unterstützten Typen finden Sie unter [Zusammenfassung der Elementtypen](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="b78dc-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="b78dc-140">Ein Value-Element kann nur Zeicheninhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="b78dc-140">A Value element can contain only character content.</span></span> <span data-ttu-id="b78dc-141">Nichts anderes kann als Inhalt in einem Value-Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b78dc-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="b78dc-142">Einige Vom Druckschema definierte Property- und ScoredProperty-Elemente enthalten kein Value-Element, da ihr Zweck einfach die über- und untergeordneten Eigenschaften sein soll.</span><span class="sxs-lookup"><span data-stu-id="b78dc-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="b78dc-143">Sie sollten solchen Eigenschaften wie diesen, Eigenschaften, die kein Value-Element enthalten, kein Value-Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b78dc-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="b78dc-144">Um dem Druckschemaframework zu entsprechen, das erfordert, dass entweder ein Value-Element oder Unterelemente in den Elementen vorhanden sind, die Werte unterstützen, sollte ein fehlender oder nicht definierter Wert dargestellt werden, indem das Value-Element als leeres Element dargestellt wird. das heißt, als</span><span class="sxs-lookup"><span data-stu-id="b78dc-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="b78dc-145">.</span><span class="sxs-lookup"><span data-stu-id="b78dc-145">.</span></span>

## <a name="example"></a><span data-ttu-id="b78dc-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b78dc-146">Example</span></span>

<span data-ttu-id="b78dc-147">Definieren Sie einen Wert vom Typ decimal, und initialisieren Sie ihn mit "128.5".</span><span class="sxs-lookup"><span data-stu-id="b78dc-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="b78dc-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b78dc-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b78dc-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b78dc-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




