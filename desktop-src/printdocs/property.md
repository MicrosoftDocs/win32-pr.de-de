---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Eigenschaft (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351868"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="16ba5-104">Eigenschaft (Dokumente und Drucken)</span><span class="sxs-lookup"><span data-stu-id="16ba5-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="16ba5-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="16ba5-105">This topic is not current.</span></span> <span data-ttu-id="16ba5-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16ba5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16ba5-107">Ein Property-Element deklariert ein Gerät, eine Auftrags Formatierung oder eine andere relevante Eigenschaft, deren Name durch das Name-Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="16ba5-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="16ba5-108">Ein Value-Element wird verwendet, um der Eigenschaft einen Wert zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="16ba5-109">Eine Eigenschaft kann komplex sein und möglicherweise mehrere untergeordnete Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="16ba5-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="16ba5-110">Unter Eigenschaften werden auch durch Eigenschafts Elemente dargestellt.</span><span class="sxs-lookup"><span data-stu-id="16ba5-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="16ba5-111">Elementtag</span><span class="sxs-lookup"><span data-stu-id="16ba5-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="16ba5-112">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="16ba5-112">XML Attributes</span></span>

<span data-ttu-id="16ba5-113">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="16ba5-114">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="16ba5-114">XML Attribute</span></span>   | <span data-ttu-id="16ba5-115">Details</span><span class="sxs-lookup"><span data-stu-id="16ba5-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ba5-116">name</span><span class="sxs-lookup"><span data-stu-id="16ba5-116">name</span></span><br/> | <span data-ttu-id="16ba5-117">Enthält das Name-Attribut der Eigenschaft, bei der es sich entweder um eine Standard Eigenschaft oder eine privat definierte Eigenschaft handelt.</span><span class="sxs-lookup"><span data-stu-id="16ba5-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="16ba5-118">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="16ba5-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="16ba5-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="16ba5-119">Element Information</span></span>

<span data-ttu-id="16ba5-120">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="16ba5-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="16ba5-121">Category</span><span class="sxs-lookup"><span data-stu-id="16ba5-121">Category</span></span>                   | <span data-ttu-id="16ba5-122">Details</span><span class="sxs-lookup"><span data-stu-id="16ba5-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ba5-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16ba5-123">Parent elements</span></span><br/> | <span data-ttu-id="16ba5-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="16ba5-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="16ba5-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="16ba5-125">Feature</span></span><br/> <span data-ttu-id="16ba5-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="16ba5-126">PrintTicket</span></span><br/> <span data-ttu-id="16ba5-127">Option</span><span class="sxs-lookup"><span data-stu-id="16ba5-127">Option</span></span><br/> <span data-ttu-id="16ba5-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="16ba5-128">ParameterDef</span></span><br/> <span data-ttu-id="16ba5-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16ba5-129">Property</span></span><br/> <span data-ttu-id="16ba5-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="16ba5-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="16ba5-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16ba5-131">Child elements</span></span><br/>  | <span data-ttu-id="16ba5-132">Das System weist der Reihenfolge der Elemente keine Bedeutung zu.</span><span class="sxs-lookup"><span data-stu-id="16ba5-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="16ba5-133">Wenn Clients eine gewisse Bedeutung in der Reihenfolge der Elemente festlegen möchten, können Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="16ba5-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="16ba5-134">*Eigenschaft* (mindestens ein *Wert* ) (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="16ba5-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="16ba5-135">oder</span><span class="sxs-lookup"><span data-stu-id="16ba5-135">or</span></span> <br/> <span data-ttu-id="16ba5-136">*Eigenschafts* Wert (null oder mehr) (mindestens ein *Wert* )</span><span class="sxs-lookup"><span data-stu-id="16ba5-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="16ba5-137">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="16ba5-137">This element</span></span><br/>    | <span data-ttu-id="16ba5-138">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="16ba5-138">No character data is permitted.</span></span><br/> <span data-ttu-id="16ba5-139">Doppelte untergeordnete Element Elemente, die gleich geordnete Elemente sind, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="16ba5-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="16ba5-140">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="16ba5-140">Configuration Dependencies</span></span>

<span data-ttu-id="16ba5-141">Eine Eigenschaft kann Konfigurations Abhängigkeiten aufweisen, außer wenn Sie in einem ParameterDef-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="16ba5-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="16ba5-142">Element Verwendung</span><span class="sxs-lookup"><span data-stu-id="16ba5-142">Element Usage</span></span>

<span data-ttu-id="16ba5-143">Eigenschaften Elemente können nicht nur innerhalb von Funktions-und Options Elementen angezeigt werden, sondern auch auf der Stamm Ebene der jeweiligen zugrunde liegenden Technologien.</span><span class="sxs-lookup"><span data-stu-id="16ba5-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="16ba5-144">Das Druck Schema definiert einen Satz von Eigenschaften Elementen, die verwendet werden können, um ein Gerät portabel zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="16ba5-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="16ba5-145">Wenn diese Eigenschaften jedoch nicht Ihren Anforderungen als Print-Funktions Anbieter genügt (in der Regel, weil das Gerät, das unterstützt wird, über neue Aspekte verfügt, die vom Druck Schema nicht erwartet werden), können Sie eigene private Eigenschaften Elemente einführen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="16ba5-146">Sie können die von einer öffentlichen Eigenschaft bereitgestellten Informationen verbessern oder vertiefen, indem Sie eine oder mehrere private unter Eigenschaften als Element Inhalt der Public-Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="16ba5-147">Eigenschafts Elemente werden mithilfe eines XML-Element Tags definiert <Property> .</span><span class="sxs-lookup"><span data-stu-id="16ba5-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="16ba5-148">Jeder Eigenschaft wird anhand des Namens Attributs ein Name zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="16ba5-149">Der Name muss ein XML-QName sein und muss der Namespace Konvention entsprechen.</span><span class="sxs-lookup"><span data-stu-id="16ba5-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="16ba5-150">Weitere Informationen finden Sie unter [XML-Attribute](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="16ba5-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="16ba5-151">Das Eigenschaftsnamen Attribut und seine Position in der Hierarchie der übergeordneten Eigenschaften Elemente (wenn es sich um eine untergeordnete Eigenschaft handelt) identifizieren die Eigenschaft innerhalb des Printworks-Dokuments oder des PrintTicket eindeutig.</span><span class="sxs-lookup"><span data-stu-id="16ba5-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="16ba5-152">Eine Eigenschaft kann ein oder mehrere value-Elemente oder ein oder mehrere untergeordnete Eigenschaften Elemente (als untergeordnete Eigenschaften bezeichnet) oder eine Kombination aus beidem enthalten.</span><span class="sxs-lookup"><span data-stu-id="16ba5-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="16ba5-153">Unter Eigenschaften sind nützlich, wenn die Eigenschaft selbst aus mehreren Komponenten besteht.</span><span class="sxs-lookup"><span data-stu-id="16ba5-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="16ba5-154">Beispielsweise kann eine "consumablecolor"-Eigenschaft "C"-, "M"-und "Y"-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="16ba5-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="16ba5-155">Beispiel</span><span class="sxs-lookup"><span data-stu-id="16ba5-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="16ba5-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16ba5-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16ba5-157">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="16ba5-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




