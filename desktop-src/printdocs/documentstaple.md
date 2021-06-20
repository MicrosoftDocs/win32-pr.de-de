---
description: Erfahren Sie mehr über das JobStapleAllDocuments-Element, das die Staplingmerkmale der Ausgabe beschreibt.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409133"
---
# <a name="documentstaple"></a><span data-ttu-id="e4797-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="e4797-103">DocumentStaple</span></span>

<span data-ttu-id="e4797-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e4797-104">This topic is not current.</span></span> <span data-ttu-id="e4797-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e4797-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e4797-106">Beschreibt die Staplingmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e4797-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="e4797-107">Jedes Dokument ist separat zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="e4797-107">Each document is stapled separately.</span></span> <span data-ttu-id="e4797-108">Die Schlüsselwörter JobStapleAllDocuments und DocumentStaple schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="e4797-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="e4797-109">Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e4797-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="e4797-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e4797-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e4797-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e4797-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e4797-112">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="e4797-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e4797-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e4797-113">Element Information</span></span>



| <span data-ttu-id="e4797-114">Name</span><span class="sxs-lookup"><span data-stu-id="e4797-114">Name</span></span> | <span data-ttu-id="e4797-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e4797-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e4797-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e4797-116">Element Type</span></span> <br/>   | <span data-ttu-id="e4797-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="e4797-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="e4797-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e4797-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e4797-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="e4797-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="e4797-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4797-120">Notes</span></span> <br/>          | <span data-ttu-id="e4797-121">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="e4797-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e4797-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e4797-122">Structural Content</span></span>

<span data-ttu-id="e4797-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="e4797-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="e4797-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e4797-124">Structure Variables</span></span>

<span data-ttu-id="e4797-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4797-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e4797-126">Name</span><span class="sxs-lookup"><span data-stu-id="e4797-126">Name</span></span>                               | <span data-ttu-id="e4797-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4797-127">Data type</span></span>          | <span data-ttu-id="e4797-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="e4797-128">Unit</span></span>                       | <span data-ttu-id="e4797-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e4797-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e4797-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e4797-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4797-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="e4797-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e4797-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4797-132">string</span></span><br/>  | <span data-ttu-id="e4797-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e4797-133">characters</span></span><br/>      | <span data-ttu-id="e4797-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="e4797-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e4797-135">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="e4797-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e4797-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="e4797-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e4797-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e4797-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e4797-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4797-138">string</span></span><br/>  | <span data-ttu-id="e4797-139">–</span><span class="sxs-lookup"><span data-stu-id="e4797-139">n/a</span></span><br/>             | <span data-ttu-id="e4797-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="e4797-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e4797-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e4797-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="e4797-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="e4797-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="e4797-143">integer</span><span class="sxs-lookup"><span data-stu-id="e4797-143">integer</span></span><br/> | <span data-ttu-id="e4797-144">Grad</span><span class="sxs-lookup"><span data-stu-id="e4797-144">degrees</span></span><br/>         | <span data-ttu-id="e4797-145">Größer 0</span><span class="sxs-lookup"><span data-stu-id="e4797-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e4797-146">Gibt den Klammerwinkel relativ zur X-Richtung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="e4797-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="e4797-147">Der Klammerwinkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="e4797-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="e4797-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="e4797-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="e4797-149">integer</span><span class="sxs-lookup"><span data-stu-id="e4797-149">integer</span></span><br/> | <span data-ttu-id="e4797-150">Medienblätter</span><span class="sxs-lookup"><span data-stu-id="e4797-150">sheets of media</span></span><br/> | <span data-ttu-id="e4797-151">Größer 0</span><span class="sxs-lookup"><span data-stu-id="e4797-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e4797-152">Gibt die Anzahl von Blättern an, die von der Staplingoption für den aktuell ausgewählten MediaType unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e4797-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e4797-153">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="e4797-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e4797-154">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="e4797-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e4797-155">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="e4797-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e4797-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4797-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4797-157">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e4797-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




