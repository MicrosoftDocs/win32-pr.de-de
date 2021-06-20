---
description: Erfahren Sie mehr über das PageBlackGenerationProcessing-Element, das das Schwarzgenerierungsverhalten für CMYK-Trennungen angibt.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408513"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="3f868-103">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="3f868-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="3f868-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3f868-104">This topic is not current.</span></span> <span data-ttu-id="3f868-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3f868-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f868-106">Gibt das Schwarzgenerierungsverhalten für CMYK-Trennungen an.</span><span class="sxs-lookup"><span data-stu-id="3f868-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="3f868-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3f868-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3f868-108">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3f868-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3f868-109">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3f868-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3f868-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3f868-110">Element Information</span></span>



| <span data-ttu-id="3f868-111">Name</span><span class="sxs-lookup"><span data-stu-id="3f868-111">Name</span></span> | <span data-ttu-id="3f868-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3f868-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3f868-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3f868-113">Element Type</span></span> <br/>   | <span data-ttu-id="3f868-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="3f868-114">Feature</span></span><br/> |
| <span data-ttu-id="3f868-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3f868-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3f868-116">Seite</span><span class="sxs-lookup"><span data-stu-id="3f868-116">Page</span></span><br/>    |
| <span data-ttu-id="3f868-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f868-117">Notes</span></span> <br/>          | <span data-ttu-id="3f868-118">Keine</span><span class="sxs-lookup"><span data-stu-id="3f868-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="3f868-119">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3f868-119">Structural Content</span></span>

<span data-ttu-id="3f868-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3f868-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3f868-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3f868-121">Structure Variables</span></span>

<span data-ttu-id="3f868-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f868-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3f868-123">Name</span><span class="sxs-lookup"><span data-stu-id="3f868-123">Name</span></span>                               | <span data-ttu-id="3f868-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3f868-124">Data type</span></span>         | <span data-ttu-id="3f868-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="3f868-125">Unit</span></span>                  | <span data-ttu-id="3f868-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3f868-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3f868-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3f868-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3f868-128">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3f868-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3f868-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f868-129">string</span></span><br/> | <span data-ttu-id="3f868-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3f868-130">characters</span></span><br/> | <span data-ttu-id="3f868-131">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3f868-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3f868-132">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3f868-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3f868-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3f868-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3f868-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3f868-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3f868-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f868-135">string</span></span><br/> | <span data-ttu-id="3f868-136">–</span><span class="sxs-lookup"><span data-stu-id="3f868-136">n/a</span></span><br/>        | <span data-ttu-id="3f868-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3f868-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3f868-138">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3f868-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3f868-139">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3f868-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3f868-140">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3f868-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3f868-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3f868-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3f868-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f868-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f868-143">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3f868-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




