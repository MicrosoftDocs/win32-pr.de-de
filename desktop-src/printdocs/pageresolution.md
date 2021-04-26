---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e44a7ff73c03929d3dfc8bc9f7c31c878ad039c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993717"
---
# <a name="pageresolution"></a><span data-ttu-id="06b2a-104">Pageresolution</span><span class="sxs-lookup"><span data-stu-id="06b2a-104">PageResolution</span></span>

<span data-ttu-id="06b2a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="06b2a-105">This topic is not current.</span></span> <span data-ttu-id="06b2a-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="06b2a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06b2a-107">Definiert die Seitenauflösung der Druckerausgabe durch einen qualitativen Wert, durch einen DPI-Wert (Dots per Inch, Punkte pro Zoll) oder durch beide Angaben.</span><span class="sxs-lookup"><span data-stu-id="06b2a-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="06b2a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="06b2a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06b2a-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="06b2a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="06b2a-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="06b2a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="06b2a-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="06b2a-111">Element Information</span></span>



| <span data-ttu-id="06b2a-112">Name</span><span class="sxs-lookup"><span data-stu-id="06b2a-112">Name</span></span> | <span data-ttu-id="06b2a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="06b2a-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="06b2a-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="06b2a-114">Element Type</span></span> <br/>   | <span data-ttu-id="06b2a-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="06b2a-115">Feature</span></span><br/> |
| <span data-ttu-id="06b2a-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="06b2a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06b2a-117">Seite</span><span class="sxs-lookup"><span data-stu-id="06b2a-117">Page</span></span><br/>    |
| <span data-ttu-id="06b2a-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06b2a-118">Notes</span></span> <br/>          | <span data-ttu-id="06b2a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="06b2a-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="06b2a-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="06b2a-120">Structural Content</span></span>

<span data-ttu-id="06b2a-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="06b2a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="06b2a-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="06b2a-122">Structure Variables</span></span>

<span data-ttu-id="06b2a-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="06b2a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06b2a-124">Name</span><span class="sxs-lookup"><span data-stu-id="06b2a-124">Name</span></span>                                      | <span data-ttu-id="06b2a-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="06b2a-125">Data type</span></span>          | <span data-ttu-id="06b2a-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="06b2a-126">Unit</span></span>                  | <span data-ttu-id="06b2a-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="06b2a-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="06b2a-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="06b2a-128">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b2a-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="06b2a-129">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="06b2a-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="06b2a-130">string</span></span><br/>  | <span data-ttu-id="06b2a-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="06b2a-131">characters</span></span><br/> | <span data-ttu-id="06b2a-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="06b2a-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="06b2a-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="06b2a-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="06b2a-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="06b2a-134">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="06b2a-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="06b2a-135">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="06b2a-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="06b2a-136">string</span></span><br/>  | <span data-ttu-id="06b2a-137">–</span><span class="sxs-lookup"><span data-stu-id="06b2a-137">n/a</span></span><br/>        | <span data-ttu-id="06b2a-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="06b2a-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="06b2a-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="06b2a-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="06b2a-140">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="06b2a-140">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="06b2a-141">integer</span><span class="sxs-lookup"><span data-stu-id="06b2a-141">integer</span></span><br/> | <span data-ttu-id="06b2a-142">DPI</span><span class="sxs-lookup"><span data-stu-id="06b2a-142">DPI</span></span><br/>        | <span data-ttu-id="06b2a-143">Größer 0</span><span class="sxs-lookup"><span data-stu-id="06b2a-143">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="06b2a-144">Gibt die x-Komponente der Auflösung relativ zu PageImageableSize in DPI an (relativ zur PageMediaSize und Feedrichtung des Mediums).</span><span class="sxs-lookup"><span data-stu-id="06b2a-144">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="06b2a-145">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="06b2a-145">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="06b2a-146">integer</span><span class="sxs-lookup"><span data-stu-id="06b2a-146">integer</span></span><br/> | <span data-ttu-id="06b2a-147">DPI</span><span class="sxs-lookup"><span data-stu-id="06b2a-147">DPI</span></span><br/>        | <span data-ttu-id="06b2a-148">Größer 0</span><span class="sxs-lookup"><span data-stu-id="06b2a-148">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="06b2a-149">Gibt die y-Komponente der Auflösung relativ zu PageImageableSize in DPI (relativ zur PageMediaSize- und Feedrichtung des Mediums) an.</span><span class="sxs-lookup"><span data-stu-id="06b2a-149">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="06b2a-150">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="06b2a-150">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="06b2a-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="06b2a-151">string</span></span><br/>  | <span data-ttu-id="06b2a-152">–</span><span class="sxs-lookup"><span data-stu-id="06b2a-152">n/a</span></span><br/>        | <span data-ttu-id="06b2a-153">Default, Draft, High, Normal, Other.</span><span class="sxs-lookup"><span data-stu-id="06b2a-153">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="06b2a-154">Gibt eine Qualitätsbezeichnung für die Auflösung an.</span><span class="sxs-lookup"><span data-stu-id="06b2a-154">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="06b2a-155">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="06b2a-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="06b2a-156">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="06b2a-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="06b2a-157">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="06b2a-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="06b2a-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06b2a-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b2a-159">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="06b2a-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




