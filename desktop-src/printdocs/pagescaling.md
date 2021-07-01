---
description: Erfahren Sie mehr über das PageScaling-Element. Dieses Element beschreibt die Skalierungsmerkmale der Ausgabe.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: Pagescaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795332f38da331a9f16b614154bf0a9270e613de
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119035"
---
# <a name="pagescaling"></a><span data-ttu-id="c553f-104">Pagescaling</span><span class="sxs-lookup"><span data-stu-id="c553f-104">PageScaling</span></span>

<span data-ttu-id="c553f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c553f-105">This topic is not current.</span></span> <span data-ttu-id="c553f-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c553f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c553f-107">Beschreibt die Skalierungsmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c553f-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="c553f-108">Bestimmte Optionen dieses Features erfordern, dass der Consumer die Merkmale der "Anwendungsinhaltsdimensionen" bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="c553f-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="c553f-109">Wenn diese Merkmale nicht bestimmt werden können, sollte der Consumer standardmäßig die Identitätsoption verwenden.</span><span class="sxs-lookup"><span data-stu-id="c553f-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="c553f-110">Diese Merkmale sind:</span><span class="sxs-lookup"><span data-stu-id="c553f-110">These characteristics are:</span></span>



| <span data-ttu-id="c553f-111">Skalierungsmerkmal</span><span class="sxs-lookup"><span data-stu-id="c553f-111">Scaling characteristic</span></span>                         | <span data-ttu-id="c553f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c553f-112">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c553f-113">Größe der Anwendungsmedien</span><span class="sxs-lookup"><span data-stu-id="c553f-113">Application Media Size</span></span>   | <span data-ttu-id="c553f-114">Die Dimensionen der mediendefiniert durch das Anwendungslayout.</span><span class="sxs-lookup"><span data-stu-id="c553f-114">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="c553f-115">Die Größe der Anwendungsmedien entspricht möglicherweise einer vom Consumer unterstützten PageMediaSize-Größe.</span><span class="sxs-lookup"><span data-stu-id="c553f-115">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="c553f-116">Größe des Anwendungsinhalts</span><span class="sxs-lookup"><span data-stu-id="c553f-116">Application Content Size</span></span> | <span data-ttu-id="c553f-117">Die Dimensionen der mediendefiniert durch das Anwendungslayout.</span><span class="sxs-lookup"><span data-stu-id="c553f-117">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="c553f-118">Die Größe der Anwendungsmedien entspricht möglicherweise einer vom Consumer unterstützten PageMediaSize-Größe.</span><span class="sxs-lookup"><span data-stu-id="c553f-118">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="c553f-119">Bleed Size der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c553f-119">Application Bleed Size</span></span>   | <span data-ttu-id="c553f-120">Der Offset und der Umfang des Bereichs für die Anwendungsblessure, ein Überlauffeld, das von der Anwendung für die Registrierung und das Layout in Bezug auf die Größe der Anwendungsmedien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c553f-120">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="c553f-121">Der bereichlose Bereich ist größer oder gleich der Größe des Anwendungsmediums.</span><span class="sxs-lookup"><span data-stu-id="c553f-121">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="c553f-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c553f-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c553f-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c553f-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c553f-124">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="c553f-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c553f-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c553f-125">Element Information</span></span>



| <span data-ttu-id="c553f-126">Name</span><span class="sxs-lookup"><span data-stu-id="c553f-126">Name</span></span> | <span data-ttu-id="c553f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c553f-127">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c553f-128">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c553f-128">Element Type</span></span> <br/>   | <span data-ttu-id="c553f-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="c553f-129">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="c553f-130">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c553f-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c553f-131">Seite</span><span class="sxs-lookup"><span data-stu-id="c553f-131">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="c553f-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c553f-132">Notes</span></span> <br/>          | <span data-ttu-id="c553f-133">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="c553f-133">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="c553f-134">Koordinaten sind relativ zu PageImageableSize, wobei der Ursprung von relativ zum Ursprung von PageImageableSize ist.</span><span class="sxs-lookup"><span data-stu-id="c553f-134">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c553f-135">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c553f-135">Structural Content</span></span>

<span data-ttu-id="c553f-136">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="c553f-136">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c553f-137">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c553f-137">Structure Variables</span></span>

<span data-ttu-id="c553f-138">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c553f-138">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c553f-139">Name</span><span class="sxs-lookup"><span data-stu-id="c553f-139">Name</span></span>                               | <span data-ttu-id="c553f-140">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c553f-140">Data type</span></span>         | <span data-ttu-id="c553f-141">Einheit</span><span class="sxs-lookup"><span data-stu-id="c553f-141">Unit</span></span>                  | <span data-ttu-id="c553f-142">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c553f-142">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c553f-143">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c553f-143">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c553f-144">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c553f-144">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c553f-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c553f-145">string</span></span><br/> | <span data-ttu-id="c553f-146">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c553f-146">characters</span></span><br/> | <span data-ttu-id="c553f-147">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="c553f-147">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c553f-148">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c553f-148">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c553f-149">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c553f-149">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c553f-150">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c553f-150">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c553f-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c553f-151">string</span></span><br/> | <span data-ttu-id="c553f-152">–</span><span class="sxs-lookup"><span data-stu-id="c553f-152">n/a</span></span><br/>        | <span data-ttu-id="c553f-153">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c553f-153">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c553f-154">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c553f-154">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c553f-155">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="c553f-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c553f-156">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="c553f-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c553f-157">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c553f-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c553f-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c553f-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c553f-159">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c553f-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




