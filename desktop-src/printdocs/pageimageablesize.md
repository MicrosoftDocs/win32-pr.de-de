---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996107"
---
# <a name="pageimageablesize"></a><span data-ttu-id="22cfb-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="22cfb-104">PageImageableSize</span></span>

<span data-ttu-id="22cfb-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="22cfb-105">This topic is not current.</span></span> <span data-ttu-id="22cfb-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="22cfb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22cfb-107">Beschreibt den bildierten Zeichenbereich für Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="22cfb-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="22cfb-108">Dies wird basierend auf PageMediaSize und PageOrientation gemeldet.</span><span class="sxs-lookup"><span data-stu-id="22cfb-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="22cfb-109">Die folgenden Diagramme veranschaulichen die Verwendung von PageImageableSize-Variablen basierend auf PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="22cfb-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![Diagramm, das Seitenmessungen zeigt](images/local-1641910626-image.png)

-   [<span data-ttu-id="22cfb-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22cfb-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22cfb-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="22cfb-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="22cfb-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="22cfb-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="22cfb-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22cfb-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="22cfb-115">Name</span><span class="sxs-lookup"><span data-stu-id="22cfb-115">Name</span></span> | <span data-ttu-id="22cfb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="22cfb-116">Value</span></span> |
| <span data-ttu-id="22cfb-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="22cfb-117">Element Type</span></span><br/>    | <span data-ttu-id="22cfb-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22cfb-118">Property</span></span><br/> |
| <span data-ttu-id="22cfb-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="22cfb-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22cfb-120">Seite</span><span class="sxs-lookup"><span data-stu-id="22cfb-120">Page</span></span><br/>     |
| <span data-ttu-id="22cfb-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22cfb-121">Notes</span></span> <br/>          | <span data-ttu-id="22cfb-122">Keine</span><span class="sxs-lookup"><span data-stu-id="22cfb-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="22cfb-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="22cfb-123">Structural Content</span></span>

<span data-ttu-id="22cfb-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="22cfb-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="22cfb-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="22cfb-125">Structure Variables</span></span>

<span data-ttu-id="22cfb-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="22cfb-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22cfb-127">Name</span><span class="sxs-lookup"><span data-stu-id="22cfb-127">Name</span></span>                                    | <span data-ttu-id="22cfb-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="22cfb-128">Data type</span></span>          | <span data-ttu-id="22cfb-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="22cfb-129">Unit</span></span>               | <span data-ttu-id="22cfb-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="22cfb-130">Supported values</span></span>                       | <span data-ttu-id="22cfb-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="22cfb-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cfb-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="22cfb-133">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-133">integer</span></span><br/> | <span data-ttu-id="22cfb-134">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-134">microns</span></span><br/> | <span data-ttu-id="22cfb-135">Größer 0</span><span class="sxs-lookup"><span data-stu-id="22cfb-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="22cfb-136">Gibt die horizontale Dimension der Anwendungsmediengröße relativ zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="22cfb-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="22cfb-138">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-138">integer</span></span><br/> | <span data-ttu-id="22cfb-139">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-139">microns</span></span><br/> | <span data-ttu-id="22cfb-140">Größer 0</span><span class="sxs-lookup"><span data-stu-id="22cfb-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="22cfb-141">Gibt die vertikale Dimension der Mediengröße der Anwendung relativ zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="22cfb-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="22cfb-143">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-143">integer</span></span><br/> | <span data-ttu-id="22cfb-144">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-144">microns</span></span><br/> | <span data-ttu-id="22cfb-145">Größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="22cfb-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="22cfb-146">Gibt den horizontalen Ursprung des bildbaren Bereichs relativ zur Größe der Anwendungsmedien an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="22cfb-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="22cfb-148">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-148">integer</span></span><br/> | <span data-ttu-id="22cfb-149">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-149">microns</span></span><br/> | <span data-ttu-id="22cfb-150">Größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="22cfb-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="22cfb-151">Gibt den vertikalen Ursprung des bildbaren Bereichs relativ zur Größe der Anwendungsmedien an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="22cfb-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="22cfb-153">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-153">integer</span></span><br/> | <span data-ttu-id="22cfb-154">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-154">microns</span></span><br/> | <span data-ttu-id="22cfb-155">Größer 0</span><span class="sxs-lookup"><span data-stu-id="22cfb-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="22cfb-156">Gibt den horizontalen Abstand zwischen dem Ursprung und der Begrenzungsgrenze der Größe der Anwendungsmedien an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="22cfb-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="22cfb-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="22cfb-158">integer</span><span class="sxs-lookup"><span data-stu-id="22cfb-158">integer</span></span><br/> | <span data-ttu-id="22cfb-159">Mikron</span><span class="sxs-lookup"><span data-stu-id="22cfb-159">microns</span></span><br/> | <span data-ttu-id="22cfb-160">Größer 0</span><span class="sxs-lookup"><span data-stu-id="22cfb-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="22cfb-161">Gibt den vertikalen Abstand zwischen dem Ursprung und der Begrenzungsgrenze der Mediengröße der Canvasanwendung an.</span><span class="sxs-lookup"><span data-stu-id="22cfb-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="22cfb-162">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="22cfb-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="22cfb-163">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="22cfb-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="22cfb-164">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="22cfb-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="22cfb-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22cfb-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22cfb-166">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="22cfb-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




