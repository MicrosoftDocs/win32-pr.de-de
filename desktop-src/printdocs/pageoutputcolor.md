---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageOutputColor-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548988"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="68368-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="68368-105">PageOutputColor</span></span>

<span data-ttu-id="68368-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="68368-106">This topic is not current.</span></span> <span data-ttu-id="68368-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="68368-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="68368-108">Beschreibt die Merkmale der Farbeinstellungen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="68368-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="68368-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="68368-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="68368-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="68368-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="68368-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="68368-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="68368-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="68368-112">Element Information</span></span>



| <span data-ttu-id="68368-113">Name</span><span class="sxs-lookup"><span data-stu-id="68368-113">Name</span></span> | <span data-ttu-id="68368-114">Wert</span><span class="sxs-lookup"><span data-stu-id="68368-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="68368-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="68368-115">Element Type</span></span> <br/>   | <span data-ttu-id="68368-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="68368-116">Feature</span></span><br/> |
| <span data-ttu-id="68368-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="68368-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="68368-118">Seite</span><span class="sxs-lookup"><span data-stu-id="68368-118">Page</span></span><br/>    |
| <span data-ttu-id="68368-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68368-119">Notes</span></span> <br/>          | <span data-ttu-id="68368-120">Keine</span><span class="sxs-lookup"><span data-stu-id="68368-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="68368-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="68368-121">Structural Content</span></span>

<span data-ttu-id="68368-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="68368-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="68368-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="68368-123">Structure Variables</span></span>

<span data-ttu-id="68368-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="68368-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="68368-125">Name</span><span class="sxs-lookup"><span data-stu-id="68368-125">Name</span></span>                                   | <span data-ttu-id="68368-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="68368-126">Data type</span></span>          | <span data-ttu-id="68368-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="68368-127">Unit</span></span>                      | <span data-ttu-id="68368-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="68368-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="68368-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="68368-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68368-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="68368-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="68368-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="68368-131">string</span></span><br/>  | <span data-ttu-id="68368-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="68368-132">characters</span></span><br/>     | <span data-ttu-id="68368-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="68368-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="68368-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="68368-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="68368-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="68368-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="68368-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="68368-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="68368-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="68368-137">string</span></span><br/>  | <span data-ttu-id="68368-138">n/v</span><span class="sxs-lookup"><span data-stu-id="68368-138">n/a</span></span><br/>            | <span data-ttu-id="68368-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="68368-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="68368-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="68368-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="68368-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="68368-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="68368-142">integer</span><span class="sxs-lookup"><span data-stu-id="68368-142">integer</span></span><br/> | <span data-ttu-id="68368-143">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="68368-143">bits per pixel</span></span><br/> | <span data-ttu-id="68368-144">Größer als 0, kleiner als der maximale Geräteunterstützungswert.</span><span class="sxs-lookup"><span data-stu-id="68368-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="68368-145">Numerischer Wert, der die Anzahl der vom Drucker unterstützten Farbdaten pro Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="68368-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="68368-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="68368-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="68368-147">integer</span><span class="sxs-lookup"><span data-stu-id="68368-147">integer</span></span><br/> | <span data-ttu-id="68368-148">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="68368-148">bits per pixel</span></span><br/> | <span data-ttu-id="68368-149">Größer als 0, kleiner als der maximale Geräteunterstützungswert.</span><span class="sxs-lookup"><span data-stu-id="68368-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="68368-150">Numerischer Wert, der die Anzahl der Bits pro Pixel angibt, die der Kerntreiber für seinen Bitmaprenderingpuffer verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="68368-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="68368-151">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="68368-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="68368-152">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="68368-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="68368-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="68368-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="68368-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68368-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68368-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="68368-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




