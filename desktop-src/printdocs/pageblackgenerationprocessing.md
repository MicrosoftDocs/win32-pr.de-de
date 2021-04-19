---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: "\"Pgeblackgenerationprocessing\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6019cd2e4d73e1869f0a71795923509566afebd0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357175"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="2e074-104">"Pgeblackgenerationprocessing"</span><span class="sxs-lookup"><span data-stu-id="2e074-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="2e074-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2e074-105">This topic is not current.</span></span> <span data-ttu-id="2e074-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e074-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e074-107">Gibt das Verhalten der schwarzen Generierung für CMYK-Trennzeichen an.</span><span class="sxs-lookup"><span data-stu-id="2e074-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="2e074-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2e074-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e074-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2e074-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2e074-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2e074-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2e074-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2e074-111">Element Information</span></span>



| <span data-ttu-id="2e074-112">Name</span><span class="sxs-lookup"><span data-stu-id="2e074-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2e074-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2e074-113">Element Type</span></span> <br/>   | <span data-ttu-id="2e074-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="2e074-114">Feature</span></span><br/> |
| <span data-ttu-id="2e074-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="2e074-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e074-116">Seite</span><span class="sxs-lookup"><span data-stu-id="2e074-116">Page</span></span><br/>    |
| <span data-ttu-id="2e074-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e074-117">Notes</span></span> <br/>          | <span data-ttu-id="2e074-118">Keine</span><span class="sxs-lookup"><span data-stu-id="2e074-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="2e074-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2e074-119">Structural Content</span></span>

<span data-ttu-id="2e074-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="2e074-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2e074-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="2e074-121">Structure Variables</span></span>

<span data-ttu-id="2e074-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2e074-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e074-123">Name</span><span class="sxs-lookup"><span data-stu-id="2e074-123">Name</span></span>                               | <span data-ttu-id="2e074-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2e074-124">Data type</span></span>         | <span data-ttu-id="2e074-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="2e074-125">Unit</span></span>                  | <span data-ttu-id="2e074-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="2e074-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2e074-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2e074-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2e074-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="2e074-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2e074-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e074-129">string</span></span><br/> | <span data-ttu-id="2e074-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="2e074-130">characters</span></span><br/> | <span data-ttu-id="2e074-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="2e074-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2e074-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="2e074-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2e074-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="2e074-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2e074-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="2e074-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2e074-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e074-135">string</span></span><br/> | <span data-ttu-id="2e074-136">–</span><span class="sxs-lookup"><span data-stu-id="2e074-136">n/a</span></span><br/>        | <span data-ttu-id="2e074-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="2e074-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2e074-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2e074-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2e074-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2e074-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2e074-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="2e074-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2e074-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="2e074-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2e074-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e074-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e074-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="2e074-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




