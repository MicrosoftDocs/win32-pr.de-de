---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageImageableSize-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395305"
---
# <a name="pageimageablesize"></a><span data-ttu-id="7ef40-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="7ef40-105">PageImageableSize</span></span>

<span data-ttu-id="7ef40-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7ef40-106">This topic is not current.</span></span> <span data-ttu-id="7ef40-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7ef40-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ef40-108">Beschreibt den bildierten Zeichenbereich für Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="7ef40-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="7ef40-109">Dies wird basierend auf PageMediaSize und PageOrientation gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7ef40-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="7ef40-110">Die folgenden Diagramme veranschaulichen die Verwendung von PageImageableSize-Variablen basierend auf PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="7ef40-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![Diagramm, das Seitenmessungen zeigt](images/local-1641910626-image.png)

-   [<span data-ttu-id="7ef40-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7ef40-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7ef40-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7ef40-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7ef40-114">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="7ef40-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7ef40-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7ef40-115">Element Information</span></span>

| <span data-ttu-id="7ef40-116">Name</span><span class="sxs-lookup"><span data-stu-id="7ef40-116">Name</span></span>                 | <span data-ttu-id="7ef40-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7ef40-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="7ef40-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7ef40-118">Element Type</span></span><br/>    | <span data-ttu-id="7ef40-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7ef40-119">Property</span></span><br/> |
| <span data-ttu-id="7ef40-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7ef40-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ef40-121">Seite</span><span class="sxs-lookup"><span data-stu-id="7ef40-121">Page</span></span><br/>     |
| <span data-ttu-id="7ef40-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ef40-122">Notes</span></span> <br/>          | <span data-ttu-id="7ef40-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7ef40-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="7ef40-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7ef40-124">Structural Content</span></span>

<span data-ttu-id="7ef40-125">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="7ef40-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7ef40-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="7ef40-126">Structure Variables</span></span>

<span data-ttu-id="7ef40-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7ef40-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ef40-128">Name</span><span class="sxs-lookup"><span data-stu-id="7ef40-128">Name</span></span>                                    | <span data-ttu-id="7ef40-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7ef40-129">Data type</span></span>          | <span data-ttu-id="7ef40-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="7ef40-130">Unit</span></span>               | <span data-ttu-id="7ef40-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="7ef40-131">Supported values</span></span>                       | <span data-ttu-id="7ef40-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7ef40-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef40-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="7ef40-134">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-134">integer</span></span><br/> | <span data-ttu-id="7ef40-135">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-135">microns</span></span><br/> | <span data-ttu-id="7ef40-136">Größer 0</span><span class="sxs-lookup"><span data-stu-id="7ef40-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="7ef40-137">Gibt die horizontale Dimension der Anwendungsmediengröße relativ zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="7ef40-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="7ef40-139">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-139">integer</span></span><br/> | <span data-ttu-id="7ef40-140">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-140">microns</span></span><br/> | <span data-ttu-id="7ef40-141">Größer 0</span><span class="sxs-lookup"><span data-stu-id="7ef40-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="7ef40-142">Gibt die vertikale Dimension der Anwendungsmediengröße relativ zur PageOrientation an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="7ef40-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="7ef40-144">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-144">integer</span></span><br/> | <span data-ttu-id="7ef40-145">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-145">microns</span></span><br/> | <span data-ttu-id="7ef40-146">Größer als oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="7ef40-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="7ef40-147">Gibt den horizontalen Ursprung des bildbaren Bereichs relativ zur Mediengröße der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="7ef40-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="7ef40-149">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-149">integer</span></span><br/> | <span data-ttu-id="7ef40-150">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-150">microns</span></span><br/> | <span data-ttu-id="7ef40-151">Größer als oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="7ef40-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="7ef40-152">Gibt den vertikalen Ursprung des bildbaren Bereichs relativ zur Mediengröße der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="7ef40-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="7ef40-154">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-154">integer</span></span><br/> | <span data-ttu-id="7ef40-155">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-155">microns</span></span><br/> | <span data-ttu-id="7ef40-156">Größer 0</span><span class="sxs-lookup"><span data-stu-id="7ef40-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="7ef40-157">Gibt den horizontalen Abstand zwischen dem Ursprung und dem Begrenzungsgrenzwert der Anwendungsmediengröße an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="7ef40-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="7ef40-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="7ef40-159">integer</span><span class="sxs-lookup"><span data-stu-id="7ef40-159">integer</span></span><br/> | <span data-ttu-id="7ef40-160">Mikron</span><span class="sxs-lookup"><span data-stu-id="7ef40-160">microns</span></span><br/> | <span data-ttu-id="7ef40-161">Größer 0</span><span class="sxs-lookup"><span data-stu-id="7ef40-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="7ef40-162">Gibt den vertikalen Abstand zwischen dem Ursprung und dem Begrenzungsgrenzwert der Mediengröße der Canvasanwendung an.</span><span class="sxs-lookup"><span data-stu-id="7ef40-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7ef40-163">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="7ef40-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7ef40-164">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="7ef40-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7ef40-165">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="7ef40-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7ef40-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ef40-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef40-167">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7ef40-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




