---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9abf6184c3164e0e5a1492911e15794ea7e1d948
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993907"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="0f5ad-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="0f5ad-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="0f5ad-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-105">This topic is not current.</span></span> <span data-ttu-id="0f5ad-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0f5ad-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f5ad-107">Beschreibt die Staplingmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="0f5ad-108">Alle Dokumente im Auftrag sind zusammengeheftet.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="0f5ad-109">Die Schlüsselwörter JobStapleAllDocuments und DocumentStaple schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="0f5ad-110">Es liegt an dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="0f5ad-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0f5ad-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0f5ad-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="0f5ad-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0f5ad-113">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="0f5ad-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0f5ad-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0f5ad-114">Element Information</span></span>



| <span data-ttu-id="0f5ad-115">Name</span><span class="sxs-lookup"><span data-stu-id="0f5ad-115">Name</span></span> | <span data-ttu-id="0f5ad-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0f5ad-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ad-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0f5ad-117">Element Type</span></span> <br/>   | <span data-ttu-id="0f5ad-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="0f5ad-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="0f5ad-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0f5ad-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0f5ad-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0f5ad-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="0f5ad-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f5ad-121">Notes</span></span> <br/>          | <span data-ttu-id="0f5ad-122">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-122">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0f5ad-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="0f5ad-123">Structural Content</span></span>

<span data-ttu-id="0f5ad-124">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="0f5ad-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="0f5ad-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0f5ad-125">Structure Variables</span></span>

<span data-ttu-id="0f5ad-126">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0f5ad-127">Name</span><span class="sxs-lookup"><span data-stu-id="0f5ad-127">Name</span></span>                               | <span data-ttu-id="0f5ad-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0f5ad-128">Data type</span></span>          | <span data-ttu-id="0f5ad-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="0f5ad-129">Unit</span></span>                       | <span data-ttu-id="0f5ad-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0f5ad-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0f5ad-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0f5ad-131">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ad-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="0f5ad-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0f5ad-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0f5ad-133">string</span></span><br/>  | <span data-ttu-id="0f5ad-134">Zeichen</span><span class="sxs-lookup"><span data-stu-id="0f5ad-134">Characters</span></span><br/>      | <span data-ttu-id="0f5ad-135">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0f5ad-136">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0f5ad-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-137">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="0f5ad-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5ad-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0f5ad-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0f5ad-139">string</span></span><br/>  | <span data-ttu-id="0f5ad-140">–</span><span class="sxs-lookup"><span data-stu-id="0f5ad-140">n/a</span></span><br/>             | <span data-ttu-id="0f5ad-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="0f5ad-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0f5ad-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="0f5ad-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5ad-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="0f5ad-144">integer</span><span class="sxs-lookup"><span data-stu-id="0f5ad-144">integer</span></span><br/> | <span data-ttu-id="0f5ad-145">Grad</span><span class="sxs-lookup"><span data-stu-id="0f5ad-145">degrees</span></span><br/>         | <span data-ttu-id="0f5ad-146">Größer 0</span><span class="sxs-lookup"><span data-stu-id="0f5ad-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0f5ad-147">Gibt den Klammerwinkel relativ zur Breite von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-147">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="0f5ad-148">Der Winkel der Klammer wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="0f5ad-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5ad-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="0f5ad-150">integer</span><span class="sxs-lookup"><span data-stu-id="0f5ad-150">integer</span></span><br/> | <span data-ttu-id="0f5ad-151">Medienblätter</span><span class="sxs-lookup"><span data-stu-id="0f5ad-151">sheets of media</span></span><br/> | <span data-ttu-id="0f5ad-152">Größer 0</span><span class="sxs-lookup"><span data-stu-id="0f5ad-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0f5ad-153">Gibt die Anzahl der Blätter an, die von der Heftoption für den aktuell ausgewählten MediaType unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0f5ad-154">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0f5ad-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0f5ad-155">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0f5ad-156">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="0f5ad-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
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

## <a name="related-topics"></a><span data-ttu-id="0f5ad-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f5ad-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ad-158">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0f5ad-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




