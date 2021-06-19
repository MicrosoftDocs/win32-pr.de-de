---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageResolution-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394819"
---
# <a name="pageresolution"></a><span data-ttu-id="3d08e-105">Pageresolution</span><span class="sxs-lookup"><span data-stu-id="3d08e-105">PageResolution</span></span>

<span data-ttu-id="3d08e-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3d08e-106">This topic is not current.</span></span> <span data-ttu-id="3d08e-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3d08e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3d08e-108">Definiert die Seitenauflösung der Druckerausgabe durch einen qualitativen Wert, durch einen DPI-Wert (Dots per Inch, Punkte pro Zoll) oder durch beide Angaben.</span><span class="sxs-lookup"><span data-stu-id="3d08e-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="3d08e-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3d08e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3d08e-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3d08e-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3d08e-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3d08e-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3d08e-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3d08e-112">Element Information</span></span>



| <span data-ttu-id="3d08e-113">Name</span><span class="sxs-lookup"><span data-stu-id="3d08e-113">Name</span></span> | <span data-ttu-id="3d08e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3d08e-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3d08e-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3d08e-115">Element Type</span></span> <br/>   | <span data-ttu-id="3d08e-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="3d08e-116">Feature</span></span><br/> |
| <span data-ttu-id="3d08e-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3d08e-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3d08e-118">Seite</span><span class="sxs-lookup"><span data-stu-id="3d08e-118">Page</span></span><br/>    |
| <span data-ttu-id="3d08e-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d08e-119">Notes</span></span> <br/>          | <span data-ttu-id="3d08e-120">Keine</span><span class="sxs-lookup"><span data-stu-id="3d08e-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="3d08e-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3d08e-121">Structural Content</span></span>

<span data-ttu-id="3d08e-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3d08e-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3d08e-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3d08e-123">Structure Variables</span></span>

<span data-ttu-id="3d08e-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3d08e-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3d08e-125">Name</span><span class="sxs-lookup"><span data-stu-id="3d08e-125">Name</span></span>                                      | <span data-ttu-id="3d08e-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3d08e-126">Data type</span></span>          | <span data-ttu-id="3d08e-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="3d08e-127">Unit</span></span>                  | <span data-ttu-id="3d08e-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3d08e-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3d08e-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3d08e-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d08e-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3d08e-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="3d08e-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d08e-131">string</span></span><br/>  | <span data-ttu-id="3d08e-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3d08e-132">characters</span></span><br/> | <span data-ttu-id="3d08e-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3d08e-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3d08e-134">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3d08e-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3d08e-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3d08e-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="3d08e-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3d08e-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="3d08e-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d08e-137">string</span></span><br/>  | <span data-ttu-id="3d08e-138">–</span><span class="sxs-lookup"><span data-stu-id="3d08e-138">n/a</span></span><br/>        | <span data-ttu-id="3d08e-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3d08e-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3d08e-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3d08e-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="3d08e-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="3d08e-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="3d08e-142">integer</span><span class="sxs-lookup"><span data-stu-id="3d08e-142">integer</span></span><br/> | <span data-ttu-id="3d08e-143">DPI</span><span class="sxs-lookup"><span data-stu-id="3d08e-143">DPI</span></span><br/>        | <span data-ttu-id="3d08e-144">Größer 0</span><span class="sxs-lookup"><span data-stu-id="3d08e-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3d08e-145">Gibt die x-Komponente der Auflösung relativ zum PageImageableSize in DPI (relativ zur PageMediaSize- und Feedrichtung des Mediums) an.</span><span class="sxs-lookup"><span data-stu-id="3d08e-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="3d08e-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="3d08e-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="3d08e-147">integer</span><span class="sxs-lookup"><span data-stu-id="3d08e-147">integer</span></span><br/> | <span data-ttu-id="3d08e-148">DPI</span><span class="sxs-lookup"><span data-stu-id="3d08e-148">DPI</span></span><br/>        | <span data-ttu-id="3d08e-149">Größer 0</span><span class="sxs-lookup"><span data-stu-id="3d08e-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="3d08e-150">Gibt die y-Komponente der Auflösung relativ zum PageImageableSize in DPI (relativ zur PageMediaSize- und Feedrichtung des Mediums) an.</span><span class="sxs-lookup"><span data-stu-id="3d08e-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="3d08e-151">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="3d08e-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="3d08e-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d08e-152">string</span></span><br/>  | <span data-ttu-id="3d08e-153">–</span><span class="sxs-lookup"><span data-stu-id="3d08e-153">n/a</span></span><br/>        | <span data-ttu-id="3d08e-154">Default, Draft, High, Normal, Other.</span><span class="sxs-lookup"><span data-stu-id="3d08e-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="3d08e-155">Gibt eine Qualitätsbezeichnung für die Auflösung an.</span><span class="sxs-lookup"><span data-stu-id="3d08e-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3d08e-156">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3d08e-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3d08e-157">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3d08e-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3d08e-158">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3d08e-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3d08e-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d08e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d08e-160">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3d08e-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




