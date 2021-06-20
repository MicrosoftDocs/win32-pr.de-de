---
description: Erfahren Sie mehr über das JobStapleAllDocuments-Element, das die Staplingmerkmale der Auftragsausgabe beschreibt.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9598f09181a225bf10d097b8c2aedaf19373a1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408643"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="75d05-103">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="75d05-103">JobStapleAllDocuments</span></span>

<span data-ttu-id="75d05-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="75d05-104">This topic is not current.</span></span> <span data-ttu-id="75d05-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="75d05-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75d05-106">Beschreibt die Staplingmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="75d05-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="75d05-107">Alle Dokumente im Auftrag sind zusammen zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="75d05-107">All documents in the job are stapled together.</span></span> <span data-ttu-id="75d05-108">Die Schlüsselwörter JobStapleAllDocuments und DocumentStaple schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="75d05-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="75d05-109">Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="75d05-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="75d05-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="75d05-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75d05-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="75d05-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75d05-112">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="75d05-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75d05-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="75d05-113">Element Information</span></span>



| <span data-ttu-id="75d05-114">Name</span><span class="sxs-lookup"><span data-stu-id="75d05-114">Name</span></span> | <span data-ttu-id="75d05-115">Wert</span><span class="sxs-lookup"><span data-stu-id="75d05-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="75d05-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="75d05-116">Element Type</span></span> <br/>   | <span data-ttu-id="75d05-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="75d05-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="75d05-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="75d05-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75d05-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="75d05-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="75d05-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75d05-120">Notes</span></span> <br/>          | <span data-ttu-id="75d05-121">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="75d05-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="75d05-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="75d05-122">Structural Content</span></span>

<span data-ttu-id="75d05-123">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="75d05-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="75d05-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="75d05-124">Structure Variables</span></span>

<span data-ttu-id="75d05-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75d05-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75d05-126">Name</span><span class="sxs-lookup"><span data-stu-id="75d05-126">Name</span></span>                               | <span data-ttu-id="75d05-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="75d05-127">Data type</span></span>          | <span data-ttu-id="75d05-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="75d05-128">Unit</span></span>                       | <span data-ttu-id="75d05-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="75d05-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75d05-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="75d05-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d05-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="75d05-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="75d05-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="75d05-132">string</span></span><br/>  | <span data-ttu-id="75d05-133">Zeichen</span><span class="sxs-lookup"><span data-stu-id="75d05-133">Characters</span></span><br/>      | <span data-ttu-id="75d05-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="75d05-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75d05-135">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="75d05-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75d05-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="75d05-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="75d05-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75d05-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="75d05-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="75d05-138">string</span></span><br/>  | <span data-ttu-id="75d05-139">–</span><span class="sxs-lookup"><span data-stu-id="75d05-139">n/a</span></span><br/>             | <span data-ttu-id="75d05-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="75d05-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75d05-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="75d05-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="75d05-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="75d05-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="75d05-143">integer</span><span class="sxs-lookup"><span data-stu-id="75d05-143">integer</span></span><br/> | <span data-ttu-id="75d05-144">Grad</span><span class="sxs-lookup"><span data-stu-id="75d05-144">degrees</span></span><br/>         | <span data-ttu-id="75d05-145">Größer 0</span><span class="sxs-lookup"><span data-stu-id="75d05-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75d05-146">Gibt den Klammerwinkel relativ zur Breite von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="75d05-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="75d05-147">Der Klammerwinkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="75d05-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="75d05-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="75d05-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="75d05-149">integer</span><span class="sxs-lookup"><span data-stu-id="75d05-149">integer</span></span><br/> | <span data-ttu-id="75d05-150">Medienblätter</span><span class="sxs-lookup"><span data-stu-id="75d05-150">sheets of media</span></span><br/> | <span data-ttu-id="75d05-151">Größer 0</span><span class="sxs-lookup"><span data-stu-id="75d05-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75d05-152">Gibt die Anzahl von Blättern an, die von der Staplingoption für den aktuell ausgewählten MediaType unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="75d05-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75d05-153">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="75d05-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75d05-154">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="75d05-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75d05-155">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="75d05-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="75d05-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75d05-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d05-157">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="75d05-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




