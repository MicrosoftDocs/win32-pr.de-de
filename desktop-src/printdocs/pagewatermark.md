---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageWatermark-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b93eadfb3aeaa2c0be1de2cf5775bd1b5c88666
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396085"
---
# <a name="pagewatermark"></a><span data-ttu-id="ce2ff-105">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="ce2ff-105">PageWatermark</span></span>

<span data-ttu-id="ce2ff-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-106">This topic is not current.</span></span> <span data-ttu-id="ce2ff-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ce2ff-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce2ff-108">Beschreibt die Wasserzeicheneinstellung der Ausgabe und die Wasserzeichenmerkmale.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-108">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="ce2ff-109">Wasserzeichen gelten für die logische Seite, nicht für die physische Seite.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-109">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="ce2ff-110">Wenn DocumentDuplex beispielsweise aktiviert ist, wird auf jeder NUp-Seite auf jedem Blatt ein Wasserzeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-110">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="ce2ff-111">Wenn DocumentDuplex PagesPerSheet=2 ist, hat jedes Blatt 2 Wasserzeichen.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-111">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="ce2ff-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce2ff-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce2ff-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="ce2ff-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ce2ff-114">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="ce2ff-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce2ff-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce2ff-115">Element Information</span></span>



| <span data-ttu-id="ce2ff-116">Name</span><span class="sxs-lookup"><span data-stu-id="ce2ff-116">Name</span></span> | <span data-ttu-id="ce2ff-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ce2ff-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2ff-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ce2ff-118">Element Type</span></span> <br/>   | <span data-ttu-id="ce2ff-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="ce2ff-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ce2ff-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ce2ff-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce2ff-121">Seite</span><span class="sxs-lookup"><span data-stu-id="ce2ff-121">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="ce2ff-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce2ff-122">Notes</span></span> <br/>          | <span data-ttu-id="ce2ff-123">Koordinaten sind relativ zu PageImageableSize, wobei der Ursprung des Wasserzeichens relativ zum Ursprung von PageImageableSize ist.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-123">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ce2ff-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="ce2ff-124">Structural Content</span></span>

<span data-ttu-id="ce2ff-125">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ce2ff-125">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ce2ff-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="ce2ff-126">Structure Variables</span></span>

<span data-ttu-id="ce2ff-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce2ff-128">Name</span><span class="sxs-lookup"><span data-stu-id="ce2ff-128">Name</span></span>                               | <span data-ttu-id="ce2ff-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ce2ff-129">Data type</span></span>         | <span data-ttu-id="ce2ff-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="ce2ff-130">Unit</span></span>                  | <span data-ttu-id="ce2ff-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="ce2ff-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ce2ff-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ce2ff-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce2ff-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ce2ff-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ce2ff-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce2ff-134">string</span></span><br/> | <span data-ttu-id="ce2ff-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="ce2ff-135">characters</span></span><br/> | <span data-ttu-id="ce2ff-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ce2ff-137">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce2ff-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ce2ff-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ce2ff-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ce2ff-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce2ff-140">string</span></span><br/> | <span data-ttu-id="ce2ff-141">–</span><span class="sxs-lookup"><span data-stu-id="ce2ff-141">n/a</span></span><br/>        | <span data-ttu-id="ce2ff-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="ce2ff-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ce2ff-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce2ff-144">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="ce2ff-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce2ff-145">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="ce2ff-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ce2ff-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="ce2ff-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ce2ff-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce2ff-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce2ff-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ce2ff-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




