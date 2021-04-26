---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338a72baecc62d22ac63ef50d8ce8967c7fd534a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997037"
---
# <a name="documentstaple"></a><span data-ttu-id="0b110-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="0b110-104">DocumentStaple</span></span>

<span data-ttu-id="0b110-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0b110-105">This topic is not current.</span></span> <span data-ttu-id="0b110-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0b110-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0b110-107">Beschreibt die Hefteigenschaften der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0b110-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="0b110-108">Jedes Dokument wird separat geheftet.</span><span class="sxs-lookup"><span data-stu-id="0b110-108">Each document is stapled separately.</span></span> <span data-ttu-id="0b110-109">Die Schlüsselwörter JobStapleAllDocuments und DocumentStaple schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="0b110-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="0b110-110">Der Treiber muss die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0b110-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="0b110-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b110-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0b110-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0b110-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0b110-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0b110-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0b110-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b110-114">Element Information</span></span>



| <span data-ttu-id="0b110-115">Name</span><span class="sxs-lookup"><span data-stu-id="0b110-115">Name</span></span> | <span data-ttu-id="0b110-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0b110-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0b110-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0b110-117">Element Type</span></span> <br/>   | <span data-ttu-id="0b110-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="0b110-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="0b110-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0b110-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0b110-120">Dokument</span><span class="sxs-lookup"><span data-stu-id="0b110-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="0b110-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b110-121">Notes</span></span> <br/>          | <span data-ttu-id="0b110-122">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="0b110-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0b110-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0b110-123">Structural Content</span></span>

<span data-ttu-id="0b110-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="0b110-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0b110-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0b110-125">Structure Variables</span></span>

<span data-ttu-id="0b110-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0b110-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0b110-127">Name</span><span class="sxs-lookup"><span data-stu-id="0b110-127">Name</span></span>                               | <span data-ttu-id="0b110-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0b110-128">Data type</span></span>          | <span data-ttu-id="0b110-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="0b110-129">Unit</span></span>                       | <span data-ttu-id="0b110-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0b110-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0b110-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0b110-131">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b110-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="0b110-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0b110-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b110-133">string</span></span><br/>  | <span data-ttu-id="0b110-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0b110-134">characters</span></span><br/>      | <span data-ttu-id="0b110-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="0b110-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0b110-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="0b110-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0b110-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="0b110-137">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="0b110-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0b110-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0b110-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b110-139">string</span></span><br/>  | <span data-ttu-id="0b110-140">–</span><span class="sxs-lookup"><span data-stu-id="0b110-140">n/a</span></span><br/>             | <span data-ttu-id="0b110-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="0b110-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0b110-142">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0b110-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="0b110-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="0b110-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="0b110-144">integer</span><span class="sxs-lookup"><span data-stu-id="0b110-144">integer</span></span><br/> | <span data-ttu-id="0b110-145">Grad</span><span class="sxs-lookup"><span data-stu-id="0b110-145">degrees</span></span><br/>         | <span data-ttu-id="0b110-146">Größer 0</span><span class="sxs-lookup"><span data-stu-id="0b110-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0b110-147">Gibt den Klammerwinkel relativ zur X-Richtung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="0b110-147">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="0b110-148">Der Klammerwinkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="0b110-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="0b110-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="0b110-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="0b110-150">integer</span><span class="sxs-lookup"><span data-stu-id="0b110-150">integer</span></span><br/> | <span data-ttu-id="0b110-151">Medienblätter</span><span class="sxs-lookup"><span data-stu-id="0b110-151">sheets of media</span></span><br/> | <span data-ttu-id="0b110-152">Größer 0</span><span class="sxs-lookup"><span data-stu-id="0b110-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0b110-153">Gibt die Anzahl von Blättern an, die von der Staplingoption für den aktuell ausgewählten MediaType unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0b110-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0b110-154">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="0b110-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0b110-155">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="0b110-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0b110-156">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="0b110-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0b110-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b110-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b110-158">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0b110-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




