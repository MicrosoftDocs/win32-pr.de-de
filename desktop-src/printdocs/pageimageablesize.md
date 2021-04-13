---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104560731"
---
# <a name="pageimageablesize"></a><span data-ttu-id="63b82-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="63b82-104">PageImageableSize</span></span>

<span data-ttu-id="63b82-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="63b82-105">This topic is not current.</span></span> <span data-ttu-id="63b82-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63b82-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63b82-107">Beschreibt das Abbild Canvas für Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="63b82-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="63b82-108">Dies wird auf der Grundlage von PageMediaSize und PageOrientation gemeldet.</span><span class="sxs-lookup"><span data-stu-id="63b82-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="63b82-109">Die folgenden Diagramme veranschaulichen die Verwendung der PageImageableSize-Variablen auf der Grundlage von PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="63b82-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![ein Diagramm, das Seiten Messungen anzeigt](images/local-1641910626-image.png)

-   [<span data-ttu-id="63b82-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="63b82-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63b82-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="63b82-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="63b82-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="63b82-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="63b82-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="63b82-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="63b82-115">Name</span><span class="sxs-lookup"><span data-stu-id="63b82-115">Name</span></span>                       |                     |
| <span data-ttu-id="63b82-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="63b82-116">Element Type</span></span><br/>    | <span data-ttu-id="63b82-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63b82-117">Property</span></span><br/> |
| <span data-ttu-id="63b82-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="63b82-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63b82-119">Seite</span><span class="sxs-lookup"><span data-stu-id="63b82-119">Page</span></span><br/>     |
| <span data-ttu-id="63b82-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63b82-120">Notes</span></span> <br/>          | <span data-ttu-id="63b82-121">Keine</span><span class="sxs-lookup"><span data-stu-id="63b82-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="63b82-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="63b82-122">Structural Content</span></span>

<span data-ttu-id="63b82-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="63b82-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="63b82-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="63b82-124">Structure Variables</span></span>

<span data-ttu-id="63b82-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="63b82-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63b82-126">Name</span><span class="sxs-lookup"><span data-stu-id="63b82-126">Name</span></span>                                    | <span data-ttu-id="63b82-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="63b82-127">Data type</span></span>          | <span data-ttu-id="63b82-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="63b82-128">Unit</span></span>               | <span data-ttu-id="63b82-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="63b82-129">Supported values</span></span>                       | <span data-ttu-id="63b82-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="63b82-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b82-131">\_Imageablesizewidthvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="63b82-132">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-132">integer</span></span><br/> | <span data-ttu-id="63b82-133">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-133">microns</span></span><br/> | <span data-ttu-id="63b82-134">Größer 0</span><span class="sxs-lookup"><span data-stu-id="63b82-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="63b82-135">Gibt die horizontale Dimension der Anwendungs Mediengröße in Relation zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="63b82-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="63b82-136">\_Imageablesizeheightvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="63b82-137">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-137">integer</span></span><br/> | <span data-ttu-id="63b82-138">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-138">microns</span></span><br/> | <span data-ttu-id="63b82-139">Größer 0</span><span class="sxs-lookup"><span data-stu-id="63b82-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="63b82-140">Gibt die vertikale Dimension der Anwendungs Mediengröße in Relation zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="63b82-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="63b82-141">\_Originwidthvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="63b82-142">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-142">integer</span></span><br/> | <span data-ttu-id="63b82-143">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-143">microns</span></span><br/> | <span data-ttu-id="63b82-144">Größer oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="63b82-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="63b82-145">Gibt den horizontalen Ursprung des Druck Bereichs in Bezug auf die Größe des Anwendungs Mediums an.</span><span class="sxs-lookup"><span data-stu-id="63b82-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="63b82-146">\_Originheightvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="63b82-147">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-147">integer</span></span><br/> | <span data-ttu-id="63b82-148">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-148">microns</span></span><br/> | <span data-ttu-id="63b82-149">Größer oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="63b82-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="63b82-150">Gibt den vertikalen Ursprung des Druck Bereichs in Bezug auf die Größe des Anwendungs Mediums an.</span><span class="sxs-lookup"><span data-stu-id="63b82-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="63b82-151">\_Extentwidthvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="63b82-152">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-152">integer</span></span><br/> | <span data-ttu-id="63b82-153">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-153">microns</span></span><br/> | <span data-ttu-id="63b82-154">Größer 0</span><span class="sxs-lookup"><span data-stu-id="63b82-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="63b82-155">Gibt den horizontalen Abstand zwischen dem Ursprung und dem Begrenzungs Grenzwert der Größe der Anwendungs Medien an.</span><span class="sxs-lookup"><span data-stu-id="63b82-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="63b82-156">\_Extentheightvalue\_</span><span class="sxs-lookup"><span data-stu-id="63b82-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="63b82-157">integer</span><span class="sxs-lookup"><span data-stu-id="63b82-157">integer</span></span><br/> | <span data-ttu-id="63b82-158">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="63b82-158">microns</span></span><br/> | <span data-ttu-id="63b82-159">Größer 0</span><span class="sxs-lookup"><span data-stu-id="63b82-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="63b82-160">Gibt den vertikalen Abstand zwischen dem Ursprung und dem Begrenzungs Grenzwert der Mediengröße der Canvas-Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="63b82-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="63b82-161">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="63b82-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="63b82-162">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="63b82-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="63b82-163">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="63b82-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="63b82-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63b82-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63b82-165">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="63b82-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




