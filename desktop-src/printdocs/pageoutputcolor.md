---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219111"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="54e41-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="54e41-104">PageOutputColor</span></span>

<span data-ttu-id="54e41-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="54e41-105">This topic is not current.</span></span> <span data-ttu-id="54e41-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54e41-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54e41-107">Beschreibt die Merkmale der Farbeinstellungen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="54e41-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="54e41-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54e41-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54e41-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="54e41-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="54e41-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="54e41-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="54e41-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54e41-111">Element Information</span></span>



| <span data-ttu-id="54e41-112">Name</span><span class="sxs-lookup"><span data-stu-id="54e41-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="54e41-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="54e41-113">Element Type</span></span> <br/>   | <span data-ttu-id="54e41-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="54e41-114">Feature</span></span><br/> |
| <span data-ttu-id="54e41-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="54e41-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54e41-116">Seite</span><span class="sxs-lookup"><span data-stu-id="54e41-116">Page</span></span><br/>    |
| <span data-ttu-id="54e41-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54e41-117">Notes</span></span> <br/>          | <span data-ttu-id="54e41-118">Keine</span><span class="sxs-lookup"><span data-stu-id="54e41-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="54e41-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="54e41-119">Structural Content</span></span>

<span data-ttu-id="54e41-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="54e41-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="54e41-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="54e41-121">Structure Variables</span></span>

<span data-ttu-id="54e41-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="54e41-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54e41-123">Name</span><span class="sxs-lookup"><span data-stu-id="54e41-123">Name</span></span>                                   | <span data-ttu-id="54e41-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="54e41-124">Data type</span></span>          | <span data-ttu-id="54e41-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="54e41-125">Unit</span></span>                      | <span data-ttu-id="54e41-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="54e41-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="54e41-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="54e41-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e41-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="54e41-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="54e41-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="54e41-129">string</span></span><br/>  | <span data-ttu-id="54e41-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="54e41-130">characters</span></span><br/>     | <span data-ttu-id="54e41-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="54e41-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="54e41-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="54e41-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="54e41-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="54e41-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="54e41-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="54e41-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="54e41-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="54e41-135">string</span></span><br/>  | <span data-ttu-id="54e41-136">–</span><span class="sxs-lookup"><span data-stu-id="54e41-136">n/a</span></span><br/>            | <span data-ttu-id="54e41-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="54e41-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="54e41-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="54e41-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="54e41-139">\_Devicebitsperpixelvalue\_</span><span class="sxs-lookup"><span data-stu-id="54e41-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="54e41-140">integer</span><span class="sxs-lookup"><span data-stu-id="54e41-140">integer</span></span><br/> | <span data-ttu-id="54e41-141">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="54e41-141">bits per pixel</span></span><br/> | <span data-ttu-id="54e41-142">Größer als 0 (null), kleiner als der maximal zulässige Geräte Unterstützungs Wert.</span><span class="sxs-lookup"><span data-stu-id="54e41-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="54e41-143">Numerischer Wert, der die Anzahl der Bits pro Pixel von Farbdaten angibt, die vom Drucker unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="54e41-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="54e41-144">\_Driverbitsperpixelvalue\_</span><span class="sxs-lookup"><span data-stu-id="54e41-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="54e41-145">integer</span><span class="sxs-lookup"><span data-stu-id="54e41-145">integer</span></span><br/> | <span data-ttu-id="54e41-146">Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="54e41-146">bits per pixel</span></span><br/> | <span data-ttu-id="54e41-147">Größer als 0 (null), kleiner als der maximal zulässige Geräte Unterstützungs Wert.</span><span class="sxs-lookup"><span data-stu-id="54e41-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="54e41-148">Numerischer Wert, der die Anzahl der Bits pro Pixel angibt, die der Kern Treiber für den bitmaprenderpuffer verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="54e41-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="54e41-149">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="54e41-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="54e41-150">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="54e41-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="54e41-151">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="54e41-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="54e41-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54e41-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e41-153">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="54e41-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




