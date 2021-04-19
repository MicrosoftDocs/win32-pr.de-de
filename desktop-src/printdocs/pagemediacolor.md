---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: Pagemediacolor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc6d39d3b189edbd2bd51803f1bb517fedd3edf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106361784"
---
# <a name="pagemediacolor"></a><span data-ttu-id="b0bf9-104">Pagemediacolor</span><span class="sxs-lookup"><span data-stu-id="b0bf9-104">PageMediaColor</span></span>

<span data-ttu-id="b0bf9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-105">This topic is not current.</span></span> <span data-ttu-id="b0bf9-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b0bf9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b0bf9-107">Beschreibt die Optionen für Medien Farben und die Merkmale der einzelnen Optionen.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="b0bf9-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b0bf9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b0bf9-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b0bf9-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b0bf9-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b0bf9-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b0bf9-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b0bf9-111">Element Information</span></span>



| <span data-ttu-id="b0bf9-112">Name</span><span class="sxs-lookup"><span data-stu-id="b0bf9-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="b0bf9-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b0bf9-113">Element Type</span></span> <br/>   | <span data-ttu-id="b0bf9-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="b0bf9-114">Feature</span></span><br/> |
| <span data-ttu-id="b0bf9-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="b0bf9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b0bf9-116">Seite</span><span class="sxs-lookup"><span data-stu-id="b0bf9-116">Page</span></span><br/>    |
| <span data-ttu-id="b0bf9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0bf9-117">Notes</span></span> <br/>          | <span data-ttu-id="b0bf9-118">Keine</span><span class="sxs-lookup"><span data-stu-id="b0bf9-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b0bf9-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b0bf9-119">Structural Content</span></span>

<span data-ttu-id="b0bf9-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="b0bf9-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b0bf9-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="b0bf9-121">Structure Variables</span></span>

<span data-ttu-id="b0bf9-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b0bf9-123">Name</span><span class="sxs-lookup"><span data-stu-id="b0bf9-123">Name</span></span>                               | <span data-ttu-id="b0bf9-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b0bf9-124">Data type</span></span>         | <span data-ttu-id="b0bf9-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="b0bf9-125">Unit</span></span>                  | <span data-ttu-id="b0bf9-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="b0bf9-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b0bf9-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b0bf9-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b0bf9-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="b0bf9-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b0bf9-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b0bf9-129">string</span></span><br/> | <span data-ttu-id="b0bf9-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b0bf9-130">characters</span></span><br/> | <span data-ttu-id="b0bf9-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b0bf9-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b0bf9-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b0bf9-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="b0bf9-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b0bf9-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b0bf9-135">string</span></span><br/> | <span data-ttu-id="b0bf9-136">–</span><span class="sxs-lookup"><span data-stu-id="b0bf9-136">n/a</span></span><br/>        | <span data-ttu-id="b0bf9-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="b0bf9-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b0bf9-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="b0bf9-139">\_Mediacolorsrgbvalue\_</span><span class="sxs-lookup"><span data-stu-id="b0bf9-139">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="b0bf9-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b0bf9-140">string</span></span><br/> | <span data-ttu-id="b0bf9-141">sRGB-Farbe</span><span class="sxs-lookup"><span data-stu-id="b0bf9-141">sRGB Color</span></span><br/> | <span data-ttu-id="b0bf9-142">\#AARRGGBB, wobei A, R, G, B hexadezimale Ziffern darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-142">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="b0bf9-143">Definiert die sRGB-Farbe für das physische Medien Blatt.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-143">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b0bf9-144">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b0bf9-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b0bf9-145">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-145">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="b0bf9-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="b0bf9-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b0bf9-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0bf9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0bf9-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b0bf9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
