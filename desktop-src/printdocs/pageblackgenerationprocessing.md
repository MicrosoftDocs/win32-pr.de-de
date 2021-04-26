---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba727cfa1c11850b62a883b95ab78a6dfae50
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996257"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="8a733-104">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="8a733-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="8a733-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8a733-105">This topic is not current.</span></span> <span data-ttu-id="8a733-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8a733-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8a733-107">Gibt das Verhalten der schwarzen Generierung für CSPALTE-Trennungen an.</span><span class="sxs-lookup"><span data-stu-id="8a733-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="8a733-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8a733-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8a733-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8a733-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8a733-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8a733-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8a733-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8a733-111">Element Information</span></span>



| <span data-ttu-id="8a733-112">Name</span><span class="sxs-lookup"><span data-stu-id="8a733-112">Name</span></span> | <span data-ttu-id="8a733-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8a733-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8a733-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8a733-114">Element Type</span></span> <br/>   | <span data-ttu-id="8a733-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="8a733-115">Feature</span></span><br/> |
| <span data-ttu-id="8a733-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8a733-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8a733-117">Seite</span><span class="sxs-lookup"><span data-stu-id="8a733-117">Page</span></span><br/>    |
| <span data-ttu-id="8a733-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a733-118">Notes</span></span> <br/>          | <span data-ttu-id="8a733-119">Keine</span><span class="sxs-lookup"><span data-stu-id="8a733-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="8a733-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8a733-120">Structural Content</span></span>

<span data-ttu-id="8a733-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="8a733-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="8a733-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8a733-122">Structure Variables</span></span>

<span data-ttu-id="8a733-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8a733-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8a733-124">Name</span><span class="sxs-lookup"><span data-stu-id="8a733-124">Name</span></span>                               | <span data-ttu-id="8a733-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8a733-125">Data type</span></span>         | <span data-ttu-id="8a733-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="8a733-126">Unit</span></span>                  | <span data-ttu-id="8a733-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8a733-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8a733-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8a733-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8a733-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="8a733-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8a733-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8a733-130">string</span></span><br/> | <span data-ttu-id="8a733-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8a733-131">characters</span></span><br/> | <span data-ttu-id="8a733-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8a733-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8a733-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8a733-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8a733-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="8a733-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8a733-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8a733-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8a733-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8a733-136">string</span></span><br/> | <span data-ttu-id="8a733-137">–</span><span class="sxs-lookup"><span data-stu-id="8a733-137">n/a</span></span><br/>        | <span data-ttu-id="8a733-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="8a733-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8a733-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8a733-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8a733-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8a733-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8a733-141">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="8a733-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8a733-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8a733-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="8a733-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a733-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a733-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8a733-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




