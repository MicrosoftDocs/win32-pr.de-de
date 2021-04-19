---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41af04cc5657360fcc8d4b15812e9c2dd6b9fb06
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106363063"
---
# <a name="pagescaling"></a><span data-ttu-id="985d7-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="985d7-104">PageScaling</span></span>

<span data-ttu-id="985d7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="985d7-105">This topic is not current.</span></span> <span data-ttu-id="985d7-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="985d7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="985d7-107">Beschreibt die Skalierungs Merkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="985d7-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="985d7-108">Bestimmte Optionen dieses Features erfordern, dass der Consumer die Merkmale der "Anwendungs Inhalts Dimensionen" bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="985d7-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="985d7-109">Wenn keine Möglichkeit besteht, diese Merkmale zu ermitteln, sollte der Consumer standardmäßig die Identitäts Option festlegen.</span><span class="sxs-lookup"><span data-stu-id="985d7-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="985d7-110">Folgende Merkmale sind zu finden:</span><span class="sxs-lookup"><span data-stu-id="985d7-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985d7-111">Größe des Anwendungs Mediums</span><span class="sxs-lookup"><span data-stu-id="985d7-111">Application Media Size</span></span>   | <span data-ttu-id="985d7-112">Die Dimensionen des Mediums, das vom Anwendungs Layout definiert wird.</span><span class="sxs-lookup"><span data-stu-id="985d7-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="985d7-113">Die Größe der Anwendungs Medien entspricht möglicherweise einer vom Consumer unterstützten PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="985d7-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="985d7-114">Anwendungs Inhalts Größe</span><span class="sxs-lookup"><span data-stu-id="985d7-114">Application Content Size</span></span> | <span data-ttu-id="985d7-115">Die Dimensionen des Mediums, das vom Anwendungs Layout definiert wird.</span><span class="sxs-lookup"><span data-stu-id="985d7-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="985d7-116">Die Größe der Anwendungs Medien entspricht möglicherweise einer vom Consumer unterstützten PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="985d7-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="985d7-117">Größe der APP-Größe</span><span class="sxs-lookup"><span data-stu-id="985d7-117">Application Bleed Size</span></span>   | <span data-ttu-id="985d7-118">Der Offset und der Umfang des Bereichs der Anwendungs bluten, ein Überlauf Feld, das von der Anwendung für die Registrierung und das Layout verwendet wird, in Bezug auf die Größe des Anwendungs Mediums.</span><span class="sxs-lookup"><span data-stu-id="985d7-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="985d7-119">Der geblendende Bereich ist groß oder gleich der Größe des Anwendungs Mediums.</span><span class="sxs-lookup"><span data-stu-id="985d7-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="985d7-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="985d7-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="985d7-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="985d7-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="985d7-122">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="985d7-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="985d7-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="985d7-123">Element Information</span></span>



| <span data-ttu-id="985d7-124">Name</span><span class="sxs-lookup"><span data-stu-id="985d7-124">Name</span></span>                       |                                                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985d7-125">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="985d7-125">Element Type</span></span> <br/>   | <span data-ttu-id="985d7-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="985d7-126">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="985d7-127">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="985d7-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="985d7-128">Seite</span><span class="sxs-lookup"><span data-stu-id="985d7-128">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="985d7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="985d7-129">Notes</span></span> <br/>          | <span data-ttu-id="985d7-130">"Top", "Bottom", "Left" und "Right" sind relativ zu "PageImageableSize".</span><span class="sxs-lookup"><span data-stu-id="985d7-130">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="985d7-131">Die Koordinaten sind relativ zu PageImageableSize, wobei der Ursprung von relativ zum Ursprung von PageImageableSize ist.</span><span class="sxs-lookup"><span data-stu-id="985d7-131">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="985d7-132">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="985d7-132">Structural Content</span></span>

<span data-ttu-id="985d7-133">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="985d7-133">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="985d7-134">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="985d7-134">Structure Variables</span></span>

<span data-ttu-id="985d7-135">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="985d7-135">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="985d7-136">Name</span><span class="sxs-lookup"><span data-stu-id="985d7-136">Name</span></span>                               | <span data-ttu-id="985d7-137">Datentyp</span><span class="sxs-lookup"><span data-stu-id="985d7-137">Data type</span></span>         | <span data-ttu-id="985d7-138">Einheit</span><span class="sxs-lookup"><span data-stu-id="985d7-138">Unit</span></span>                  | <span data-ttu-id="985d7-139">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="985d7-139">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="985d7-140">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="985d7-140">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="985d7-141">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="985d7-141">\_OptionName\_</span></span><br/>          | <span data-ttu-id="985d7-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="985d7-142">string</span></span><br/> | <span data-ttu-id="985d7-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="985d7-143">characters</span></span><br/> | <span data-ttu-id="985d7-144">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="985d7-144">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="985d7-145">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="985d7-145">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="985d7-146">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="985d7-146">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="985d7-147">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="985d7-147">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="985d7-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="985d7-148">string</span></span><br/> | <span data-ttu-id="985d7-149">–</span><span class="sxs-lookup"><span data-stu-id="985d7-149">n/a</span></span><br/>        | <span data-ttu-id="985d7-150">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="985d7-150">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="985d7-151">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="985d7-151">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="985d7-152">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="985d7-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="985d7-153">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="985d7-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="985d7-154">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="985d7-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="985d7-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="985d7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="985d7-156">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="985d7-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




