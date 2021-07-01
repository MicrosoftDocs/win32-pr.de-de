---
description: Erfahren Sie mehr über das Property-Element in Dokumenten und beim Drucken. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Eigenschaft (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120295"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="05777-105">Eigenschaft (Dokumente und Drucken)</span><span class="sxs-lookup"><span data-stu-id="05777-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="05777-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="05777-106">This topic is not current.</span></span> <span data-ttu-id="05777-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="05777-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="05777-108">Ein Property-Element deklariert ein Gerät, eine Auftragsformatierung oder eine andere relevante Eigenschaft, deren Name durch das Name-Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05777-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="05777-109">Ein Value-Element wird verwendet, um der Eigenschaft einen Wert zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="05777-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="05777-110">Eine Eigenschaft kann komplex sein und möglicherweise mehrere Untereigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="05777-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="05777-111">Untereigenschaften werden auch durch Property-Elemente dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05777-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="05777-112">Elementtag</span><span class="sxs-lookup"><span data-stu-id="05777-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="05777-113">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="05777-113">XML Attributes</span></span>

<span data-ttu-id="05777-114">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.</span><span class="sxs-lookup"><span data-stu-id="05777-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="05777-115">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="05777-115">XML Attribute</span></span>   | <span data-ttu-id="05777-116">Details</span><span class="sxs-lookup"><span data-stu-id="05777-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05777-117">name</span><span class="sxs-lookup"><span data-stu-id="05777-117">name</span></span><br/> | <span data-ttu-id="05777-118">Enthält das Namensattribut der Eigenschaft, bei der es sich entweder um eine Standardeigenschaft oder eine privat definierte Eigenschaft handelt.</span><span class="sxs-lookup"><span data-stu-id="05777-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="05777-119">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="05777-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="05777-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="05777-120">Element Information</span></span>

<span data-ttu-id="05777-121">In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="05777-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="05777-122">Category</span><span class="sxs-lookup"><span data-stu-id="05777-122">Category</span></span>                   | <span data-ttu-id="05777-123">Details</span><span class="sxs-lookup"><span data-stu-id="05777-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05777-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05777-124">Parent elements</span></span><br/> | <span data-ttu-id="05777-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="05777-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="05777-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="05777-126">Feature</span></span><br/> <span data-ttu-id="05777-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="05777-127">PrintTicket</span></span><br/> <span data-ttu-id="05777-128">Option</span><span class="sxs-lookup"><span data-stu-id="05777-128">Option</span></span><br/> <span data-ttu-id="05777-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="05777-129">ParameterDef</span></span><br/> <span data-ttu-id="05777-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05777-130">Property</span></span><br/> <span data-ttu-id="05777-131">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="05777-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="05777-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05777-132">Child elements</span></span><br/>  | <span data-ttu-id="05777-133">Das System weist der Reihenfolge der Elemente keine Bedeutung zu.</span><span class="sxs-lookup"><span data-stu-id="05777-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="05777-134">Wenn Clients sich dafür entscheiden, eine gewisse Bedeutung in der Reihenfolge der Elemente zuzuordnen, können sie dies auch tun.</span><span class="sxs-lookup"><span data-stu-id="05777-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="05777-135">*Eigenschaftswert* (mindestens ein *Wert)* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="05777-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="05777-136">oder</span><span class="sxs-lookup"><span data-stu-id="05777-136">or</span></span> <br/> <span data-ttu-id="05777-137">*Eigenschaftswert* (null oder mehr) (mindestens ein *Wert)*</span><span class="sxs-lookup"><span data-stu-id="05777-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="05777-138">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="05777-138">This element</span></span><br/>    | <span data-ttu-id="05777-139">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="05777-139">No character data is permitted.</span></span><br/> <span data-ttu-id="05777-140">Doppelte untergeordnete Value-Elemente, die gleichgeordnete Elemente sind, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="05777-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="05777-141">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="05777-141">Configuration Dependencies</span></span>

<span data-ttu-id="05777-142">Eine Eigenschaft kann Konfigurationsabhängigkeiten aufweisen, es sei denn, sie wird in einem ParameterDef-Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="05777-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="05777-143">Elementverwendung</span><span class="sxs-lookup"><span data-stu-id="05777-143">Element Usage</span></span>

<span data-ttu-id="05777-144">Zusätzlich zum Erscheinen in Feature- und Optionselementen können Eigenschaftselemente auf der Stammebene der jeweiligen zugrunde liegenden Technologien angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05777-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="05777-145">Das Druckschema definiert einen Satz von Eigenschaftselementen, die verwendet werden können, um ein Gerät auf portable Weise zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="05777-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="05777-146">Wenn diese Eigenschaften jedoch nicht ihren Anforderungen als PrintCapabilities-Anbieter entsprechen (in der Regel weil das unterstützte Gerät neue Aspekte aufweist, die vom Druckschema nicht erwartet werden), können Sie Ihre eigenen privaten Property-Elemente einführen.</span><span class="sxs-lookup"><span data-stu-id="05777-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="05777-147">Sie können die von einer öffentlichen Eigenschaft bereitgestellten Informationen erweitern oder erweitern, indem Sie eine oder mehrere private Untereigenschaften als Elementinhalt der öffentlichen Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05777-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="05777-148">Eigenschaftselemente werden mithilfe eines XML-Elementtags <Property> definiert.</span><span class="sxs-lookup"><span data-stu-id="05777-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="05777-149">Jeder Eigenschaft wird anhand ihres Namensattributs ein Name zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="05777-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="05777-150">Der Name muss ein XML-QName sein und der Namespacekonvention entsprechen.</span><span class="sxs-lookup"><span data-stu-id="05777-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="05777-151">Weitere Informationen finden Sie unter [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="05777-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="05777-152">Das Eigenschaftsnamenattribut und seine Position innerhalb der Hierarchie übergeordneter Property-Elemente (wenn es sich um eine Untereigenschaft handelt) identifizieren die Eigenschaft eindeutig im PrintCapabilities-Dokument oder printTicket.</span><span class="sxs-lookup"><span data-stu-id="05777-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="05777-153">Eine Eigenschaft kann ein oder mehrere Value-Elemente oder mindestens ein untergeordnetes Property-Element (als Untereigenschaften bezeichnet) oder eine Kombination aus beiden enthalten.</span><span class="sxs-lookup"><span data-stu-id="05777-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="05777-154">Untereigenschaften sind nützlich, wenn die Eigenschaft selbst aus mehreren Komponenten besteht.</span><span class="sxs-lookup"><span data-stu-id="05777-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="05777-155">Beispielsweise kann eine "ConsumableColor"-Eigenschaft über die Komponenten "C", "M" und "Y" verfügen.</span><span class="sxs-lookup"><span data-stu-id="05777-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="05777-156">Beispiel</span><span class="sxs-lookup"><span data-stu-id="05777-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="05777-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05777-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05777-158">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="05777-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




