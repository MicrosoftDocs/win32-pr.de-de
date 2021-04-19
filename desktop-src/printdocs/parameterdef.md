---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350599"
---
# <a name="parameterdef"></a><span data-ttu-id="16b24-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="16b24-104">ParameterDef</span></span>

<span data-ttu-id="16b24-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="16b24-105">This topic is not current.</span></span> <span data-ttu-id="16b24-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16b24-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16b24-107">Ein ParameterDef-Element definiert die gültigen Merkmale von Parameter Eingaben.</span><span class="sxs-lookup"><span data-stu-id="16b24-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="16b24-108">Der Wert wird mithilfe eines parameterinit-Elements eingegeben.</span><span class="sxs-lookup"><span data-stu-id="16b24-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="16b24-109">Elementtag</span><span class="sxs-lookup"><span data-stu-id="16b24-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="16b24-110">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="16b24-110">XML Attributes</span></span>

<span data-ttu-id="16b24-111">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="16b24-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="16b24-112">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="16b24-112">XML Attribute</span></span>   | <span data-ttu-id="16b24-113">Details</span><span class="sxs-lookup"><span data-stu-id="16b24-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b24-114">name</span><span class="sxs-lookup"><span data-stu-id="16b24-114">name</span></span><br/> | <span data-ttu-id="16b24-115">Definiert einen eindeutigen Namen für den Parameter im Kontext des aktuellen Dokuments.</span><span class="sxs-lookup"><span data-stu-id="16b24-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="16b24-116">Doppelte ParameterDef-namens Attribute renderdas printfunktionalitäten-Dokument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="16b24-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="16b24-117">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="16b24-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="16b24-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="16b24-118">Element Information</span></span>

<span data-ttu-id="16b24-119">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="16b24-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16b24-120">Category</span><span class="sxs-lookup"><span data-stu-id="16b24-120">Category</span></span></th>
<th><span data-ttu-id="16b24-121">Details</span><span class="sxs-lookup"><span data-stu-id="16b24-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16b24-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16b24-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="16b24-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="16b24-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16b24-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16b24-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="16b24-125">Eigenschaft (ein oder mehrere Elemente)</span><span class="sxs-lookup"><span data-stu-id="16b24-125">Property (one or more)</span></span><br/> <span data-ttu-id="16b24-126">Die folgenden Standard Eigenschafts Elemente müssen als Inhalt eines ParameterDef-Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16b24-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="16b24-127">DataType</span><span class="sxs-lookup"><span data-stu-id="16b24-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="16b24-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="16b24-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="16b24-129">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="16b24-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="16b24-130">MaxLength oder MaxValue</span><span class="sxs-lookup"><span data-stu-id="16b24-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="16b24-131">MinLength oder MinValue</span><span class="sxs-lookup"><span data-stu-id="16b24-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="16b24-132">Mehr</span><span class="sxs-lookup"><span data-stu-id="16b24-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="16b24-133">UnitType</span><span class="sxs-lookup"><span data-stu-id="16b24-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16b24-134">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="16b24-134">This element</span></span><br/></td>
<td><span data-ttu-id="16b24-135">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="16b24-135">No character data is permitted.</span></span><br/> <span data-ttu-id="16b24-136">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="16b24-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="16b24-137">\*Erforderlich, wenn DataType Integer oder Decimal ist.</span><span class="sxs-lookup"><span data-stu-id="16b24-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="16b24-138">Optional, wenn DataType eine Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="16b24-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="16b24-139">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="16b24-139">Configuration Dependencies</span></span>

<span data-ttu-id="16b24-140">Ein ParameterDef und der zugehörige Inhalt einer beliebigen Schachtelungs Ebene verfügen möglicherweise nicht über Konfigurations Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="16b24-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="16b24-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="16b24-141">Example</span></span>

<span data-ttu-id="16b24-142">Im folgenden Beispiel werden alle erforderlichen Eigenschaften Elemente für diesen Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16b24-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="16b24-143">Das Beispiel in [parameterinit](parameterinit.md) veranschaulicht, wie dieser Parameter initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="16b24-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="16b24-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16b24-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b24-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="16b24-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




