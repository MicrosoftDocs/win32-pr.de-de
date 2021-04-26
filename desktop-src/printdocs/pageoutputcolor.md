---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4791ca4a53b8bdcc43a32c5c7aa5a1e38bbe1e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998047"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="4cfe0-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="4cfe0-104">PageOutputColor</span></span>

<span data-ttu-id="4cfe0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-105">This topic is not current.</span></span> <span data-ttu-id="4cfe0-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4cfe0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4cfe0-107">Beschreibt die Merkmale der Farbeinstellungen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="4cfe0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4cfe0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4cfe0-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="4cfe0-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4cfe0-110">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="4cfe0-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4cfe0-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4cfe0-111">Element Information</span></span>



| <span data-ttu-id="4cfe0-112">Name</span><span class="sxs-lookup"><span data-stu-id="4cfe0-112">Name</span></span> | <span data-ttu-id="4cfe0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4cfe0-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="4cfe0-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4cfe0-114">Element Type</span></span> <br/>   | <span data-ttu-id="4cfe0-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="4cfe0-115">Feature</span></span><br/> |
| <span data-ttu-id="4cfe0-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4cfe0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4cfe0-117">Seite</span><span class="sxs-lookup"><span data-stu-id="4cfe0-117">Page</span></span><br/>    |
| <span data-ttu-id="4cfe0-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cfe0-118">Notes</span></span> <br/>          | <span data-ttu-id="4cfe0-119">Keine</span><span class="sxs-lookup"><span data-stu-id="4cfe0-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="4cfe0-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="4cfe0-120">Structural Content</span></span>

<span data-ttu-id="4cfe0-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4cfe0-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4cfe0-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4cfe0-122">Structure Variables</span></span>

<span data-ttu-id="4cfe0-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4cfe0-124">Name</span><span class="sxs-lookup"><span data-stu-id="4cfe0-124">Name</span></span>                                   | <span data-ttu-id="4cfe0-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4cfe0-125">Data type</span></span>          | <span data-ttu-id="4cfe0-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="4cfe0-126">Unit</span></span>                      | <span data-ttu-id="4cfe0-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4cfe0-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4cfe0-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4cfe0-128">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfe0-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="4cfe0-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="4cfe0-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4cfe0-130">string</span></span><br/>  | <span data-ttu-id="4cfe0-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4cfe0-131">characters</span></span><br/>     | <span data-ttu-id="4cfe0-132">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4cfe0-133">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4cfe0-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-134">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="4cfe0-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4cfe0-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="4cfe0-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4cfe0-136">string</span></span><br/>  | <span data-ttu-id="4cfe0-137">–</span><span class="sxs-lookup"><span data-stu-id="4cfe0-137">n/a</span></span><br/>            | <span data-ttu-id="4cfe0-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4cfe0-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4cfe0-139">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="4cfe0-140">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="4cfe0-140">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="4cfe0-141">integer</span><span class="sxs-lookup"><span data-stu-id="4cfe0-141">integer</span></span><br/> | <span data-ttu-id="4cfe0-142">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="4cfe0-142">bits per pixel</span></span><br/> | <span data-ttu-id="4cfe0-143">Größer als 0, kleiner als der maximale Wert für die Geräteunterstützung.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-143">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="4cfe0-144">Numerischer Wert, der die Anzahl der Bits pro Pixel der vom Drucker unterstützten Farbdaten angibt.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-144">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="4cfe0-145">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="4cfe0-145">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="4cfe0-146">integer</span><span class="sxs-lookup"><span data-stu-id="4cfe0-146">integer</span></span><br/> | <span data-ttu-id="4cfe0-147">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="4cfe0-147">bits per pixel</span></span><br/> | <span data-ttu-id="4cfe0-148">Größer als 0, kleiner als der maximale Wert für die Geräteunterstützung.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-148">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="4cfe0-149">Numerischer Wert, der die Anzahl der Bits pro Pixel angibt, die der Kerntreiber für seinen Bitmaprenderingpuffer verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-149">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4cfe0-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4cfe0-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4cfe0-151">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4cfe0-152">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4cfe0-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4cfe0-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4cfe0-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cfe0-154">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4cfe0-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




