---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: Pagescaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32beceead1c0dc867a2bb7b24d476ef05bf8820
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997497"
---
# <a name="pagescaling"></a><span data-ttu-id="a1776-104">Pagescaling</span><span class="sxs-lookup"><span data-stu-id="a1776-104">PageScaling</span></span>

<span data-ttu-id="a1776-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a1776-105">This topic is not current.</span></span> <span data-ttu-id="a1776-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a1776-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1776-107">Beschreibt die Skalierungsmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a1776-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="a1776-108">Bestimmte Optionen dieses Features erfordern, dass der Consumer die Merkmale der "Anwendungsinhaltsdimensionen" bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="a1776-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="a1776-109">Wenn diese Merkmale nicht bestimmt werden können, sollte der Consumer standardmäßig die Identitätsoption verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1776-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="a1776-110">Dies sind die folgenden Merkmale:</span><span class="sxs-lookup"><span data-stu-id="a1776-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1776-111">Größe der Anwendungsmedien</span><span class="sxs-lookup"><span data-stu-id="a1776-111">Application Media Size</span></span>   | <span data-ttu-id="a1776-112">Die Vom Anwendungslayout definierten Mediendimensionen.</span><span class="sxs-lookup"><span data-stu-id="a1776-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a1776-113">Die Größe der Anwendungsmedien entspricht möglicherweise einer PageMediaSize, die vom Consumer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a1776-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a1776-114">Größe des Anwendungsinhalts</span><span class="sxs-lookup"><span data-stu-id="a1776-114">Application Content Size</span></span> | <span data-ttu-id="a1776-115">Die Vom Anwendungslayout definierten Mediendimensionen.</span><span class="sxs-lookup"><span data-stu-id="a1776-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a1776-116">Die Größe der Anwendungsmedien entspricht möglicherweise einer PageMediaSize, die vom Consumer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a1776-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a1776-117">Application Bleed Size</span><span class="sxs-lookup"><span data-stu-id="a1776-117">Application Bleed Size</span></span>   | <span data-ttu-id="a1776-118">Der Offset und der Umfang des Überlaufbereichs der Anwendung, ein Überlauffeld, das von der Anwendung für die Registrierung und das Layout in Bezug auf die Größe der Anwendungsmedien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1776-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="a1776-119">Der Überleerungsbereich ist größer oder gleich der Mediengröße der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a1776-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="a1776-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a1776-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a1776-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a1776-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a1776-122">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a1776-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a1776-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a1776-123">Element Information</span></span>



| <span data-ttu-id="a1776-124">Name</span><span class="sxs-lookup"><span data-stu-id="a1776-124">Name</span></span> | <span data-ttu-id="a1776-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a1776-125">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1776-126">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a1776-126">Element Type</span></span> <br/>   | <span data-ttu-id="a1776-127">Funktion</span><span class="sxs-lookup"><span data-stu-id="a1776-127">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="a1776-128">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a1776-128">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1776-129">Seite</span><span class="sxs-lookup"><span data-stu-id="a1776-129">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="a1776-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1776-130">Notes</span></span> <br/>          | <span data-ttu-id="a1776-131">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a1776-131">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="a1776-132">Koordinaten sind relativ zu PageImageableSize, wobei der Ursprung von relativ zum Ursprung von PageImageableSize ist.</span><span class="sxs-lookup"><span data-stu-id="a1776-132">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a1776-133">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a1776-133">Structural Content</span></span>

<span data-ttu-id="a1776-134">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a1776-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a1776-135">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a1776-135">Structure Variables</span></span>

<span data-ttu-id="a1776-136">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1776-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1776-137">Name</span><span class="sxs-lookup"><span data-stu-id="a1776-137">Name</span></span>                               | <span data-ttu-id="a1776-138">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a1776-138">Data type</span></span>         | <span data-ttu-id="a1776-139">Einheit</span><span class="sxs-lookup"><span data-stu-id="a1776-139">Unit</span></span>                  | <span data-ttu-id="a1776-140">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a1776-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a1776-141">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a1776-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1776-142">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a1776-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a1776-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a1776-143">string</span></span><br/> | <span data-ttu-id="a1776-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a1776-144">characters</span></span><br/> | <span data-ttu-id="a1776-145">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a1776-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a1776-146">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a1776-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a1776-147">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a1776-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a1776-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a1776-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a1776-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a1776-149">string</span></span><br/> | <span data-ttu-id="a1776-150">–</span><span class="sxs-lookup"><span data-stu-id="a1776-150">n/a</span></span><br/>        | <span data-ttu-id="a1776-151">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a1776-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a1776-152">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a1776-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a1776-153">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a1776-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a1776-154">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a1776-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a1776-155">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a1776-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a1776-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1776-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1776-157">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a1776-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




