---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106350608"
---
# <a name="pageresolution"></a><span data-ttu-id="3bf43-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="3bf43-104">PageResolution</span></span>

<span data-ttu-id="3bf43-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3bf43-105">This topic is not current.</span></span> <span data-ttu-id="3bf43-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3bf43-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3bf43-107">Definiert die Seitenauflösung der Druckerausgabe durch einen qualitativen Wert, durch einen DPI-Wert (Dots per Inch, Punkte pro Zoll) oder durch beide Angaben.</span><span class="sxs-lookup"><span data-stu-id="3bf43-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="3bf43-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3bf43-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3bf43-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3bf43-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3bf43-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3bf43-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3bf43-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3bf43-111">Element Information</span></span>



| <span data-ttu-id="3bf43-112">Name</span><span class="sxs-lookup"><span data-stu-id="3bf43-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="3bf43-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3bf43-113">Element Type</span></span> <br/>   | <span data-ttu-id="3bf43-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="3bf43-114">Feature</span></span><br/> |
| <span data-ttu-id="3bf43-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="3bf43-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3bf43-116">Seite</span><span class="sxs-lookup"><span data-stu-id="3bf43-116">Page</span></span><br/>    |
| <span data-ttu-id="3bf43-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3bf43-117">Notes</span></span> <br/>          | <span data-ttu-id="3bf43-118">Keine</span><span class="sxs-lookup"><span data-stu-id="3bf43-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="3bf43-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3bf43-119">Structural Content</span></span>

<span data-ttu-id="3bf43-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3bf43-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3bf43-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3bf43-121">Structure Variables</span></span>

<span data-ttu-id="3bf43-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3bf43-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3bf43-123">Name</span><span class="sxs-lookup"><span data-stu-id="3bf43-123">Name</span></span>                                      | <span data-ttu-id="3bf43-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3bf43-124">Data type</span></span>          | <span data-ttu-id="3bf43-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="3bf43-125">Unit</span></span>                  | <span data-ttu-id="3bf43-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3bf43-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3bf43-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3bf43-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf43-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="3bf43-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="3bf43-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3bf43-129">string</span></span><br/>  | <span data-ttu-id="3bf43-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3bf43-130">characters</span></span><br/> | <span data-ttu-id="3bf43-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3bf43-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3bf43-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3bf43-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3bf43-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3bf43-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="3bf43-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="3bf43-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="3bf43-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3bf43-135">string</span></span><br/>  | <span data-ttu-id="3bf43-136">–</span><span class="sxs-lookup"><span data-stu-id="3bf43-136">n/a</span></span><br/>        | <span data-ttu-id="3bf43-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3bf43-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3bf43-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3bf43-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="3bf43-139">\_Resolutionxvalue\_</span><span class="sxs-lookup"><span data-stu-id="3bf43-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="3bf43-140">integer</span><span class="sxs-lookup"><span data-stu-id="3bf43-140">integer</span></span><br/> | <span data-ttu-id="3bf43-141">DPI</span><span class="sxs-lookup"><span data-stu-id="3bf43-141">DPI</span></span><br/>        | <span data-ttu-id="3bf43-142">Größer 0</span><span class="sxs-lookup"><span data-stu-id="3bf43-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3bf43-143">Gibt die x-Komponente der Auflösung relativ zu PageImageableSize in dpi an (relativ zur PageMediaSize-und Feed-Richtung der Medien).</span><span class="sxs-lookup"><span data-stu-id="3bf43-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="3bf43-144">\_Resolutionyvalue\_</span><span class="sxs-lookup"><span data-stu-id="3bf43-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="3bf43-145">integer</span><span class="sxs-lookup"><span data-stu-id="3bf43-145">integer</span></span><br/> | <span data-ttu-id="3bf43-146">DPI</span><span class="sxs-lookup"><span data-stu-id="3bf43-146">DPI</span></span><br/>        | <span data-ttu-id="3bf43-147">Größer 0</span><span class="sxs-lookup"><span data-stu-id="3bf43-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3bf43-148">Gibt die y-Komponente der Auflösung relativ zu PageImageableSize in dpi an (relativ zur PageMediaSize-und Feed-Richtung der Medien).</span><span class="sxs-lookup"><span data-stu-id="3bf43-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="3bf43-149">\_Wert von "qualitativeresolutionvalue"\_</span><span class="sxs-lookup"><span data-stu-id="3bf43-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="3bf43-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3bf43-150">string</span></span><br/>  | <span data-ttu-id="3bf43-151">–</span><span class="sxs-lookup"><span data-stu-id="3bf43-151">n/a</span></span><br/>        | <span data-ttu-id="3bf43-152">Standard, Entwurf, hoch, normal, andere.</span><span class="sxs-lookup"><span data-stu-id="3bf43-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="3bf43-153">Gibt eine Qualitätsbezeichnung für die Auflösung an.</span><span class="sxs-lookup"><span data-stu-id="3bf43-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3bf43-154">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3bf43-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3bf43-155">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3bf43-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3bf43-156">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3bf43-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3bf43-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3bf43-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bf43-158">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="3bf43-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




