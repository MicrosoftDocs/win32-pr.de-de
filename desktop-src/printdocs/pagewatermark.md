---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: Einfügemarke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106351865"
---
# <a name="pagewatermark"></a><span data-ttu-id="25d95-104">Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="25d95-104">PageWatermark</span></span>

<span data-ttu-id="25d95-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="25d95-105">This topic is not current.</span></span> <span data-ttu-id="25d95-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="25d95-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="25d95-107">Beschreibt die Wasserzeichen Einstellung der Ausgabe-und Wasserzeichen Merkmale.</span><span class="sxs-lookup"><span data-stu-id="25d95-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="25d95-108">Wasserzeichen gelten für die logische Seite, nicht für die physische Seite.</span><span class="sxs-lookup"><span data-stu-id="25d95-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="25d95-109">Wenn z. b. DocumentDuplex aktiviert ist, wird auf jeder NUP-Seite jedes Blatts ein Wasserzeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25d95-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="25d95-110">Wenn DocumentDuplex, PagesPerSheet = 2, enthält jedes Blatt zwei Wasserzeichen.</span><span class="sxs-lookup"><span data-stu-id="25d95-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="25d95-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="25d95-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="25d95-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="25d95-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="25d95-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="25d95-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="25d95-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="25d95-114">Element Information</span></span>



| <span data-ttu-id="25d95-115">Name</span><span class="sxs-lookup"><span data-stu-id="25d95-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25d95-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="25d95-116">Element Type</span></span> <br/>   | <span data-ttu-id="25d95-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="25d95-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="25d95-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="25d95-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="25d95-119">Seite</span><span class="sxs-lookup"><span data-stu-id="25d95-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="25d95-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="25d95-120">Notes</span></span> <br/>          | <span data-ttu-id="25d95-121">Die Koordinaten sind relativ zu PageImageableSize, wobei der Ursprung des Wasserzeichens relativ zum Ursprung von PageImageableSize ist.</span><span class="sxs-lookup"><span data-stu-id="25d95-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="25d95-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="25d95-122">Structural Content</span></span>

<span data-ttu-id="25d95-123">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25d95-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="25d95-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="25d95-124">Structure Variables</span></span>

<span data-ttu-id="25d95-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="25d95-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="25d95-126">Name</span><span class="sxs-lookup"><span data-stu-id="25d95-126">Name</span></span>                               | <span data-ttu-id="25d95-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25d95-127">Data type</span></span>         | <span data-ttu-id="25d95-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="25d95-128">Unit</span></span>                  | <span data-ttu-id="25d95-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="25d95-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="25d95-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="25d95-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="25d95-131">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="25d95-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="25d95-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="25d95-132">string</span></span><br/> | <span data-ttu-id="25d95-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="25d95-133">characters</span></span><br/> | <span data-ttu-id="25d95-134">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="25d95-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="25d95-135">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="25d95-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="25d95-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="25d95-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="25d95-137">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="25d95-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="25d95-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="25d95-138">string</span></span><br/> | <span data-ttu-id="25d95-139">–</span><span class="sxs-lookup"><span data-stu-id="25d95-139">n/a</span></span><br/>        | <span data-ttu-id="25d95-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="25d95-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="25d95-141">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="25d95-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="25d95-142">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="25d95-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="25d95-143">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="25d95-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="25d95-144">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="25d95-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="25d95-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25d95-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25d95-146">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="25d95-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




