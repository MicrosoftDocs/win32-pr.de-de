---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 29d7ae65-9dd3-4a29-8e5e-79708638a3bb
title: PageMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8312554d8616ed31ea99cd0cc011b2b549d915f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106355745"
---
# <a name="pagemediatype"></a><span data-ttu-id="620be-104">PageMediaType</span><span class="sxs-lookup"><span data-stu-id="620be-104">PageMediaType</span></span>

<span data-ttu-id="620be-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="620be-105">This topic is not current.</span></span> <span data-ttu-id="620be-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="620be-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="620be-107">Beschreibt die MediaType-Optionen und die Merkmale der einzelnen Optionen.</span><span class="sxs-lookup"><span data-stu-id="620be-107">Describes the MediaType options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="620be-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="620be-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="620be-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="620be-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="620be-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="620be-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="620be-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="620be-111">Element Information</span></span>



| <span data-ttu-id="620be-112">Name</span><span class="sxs-lookup"><span data-stu-id="620be-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="620be-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="620be-113">Element Type</span></span> <br/>   | <span data-ttu-id="620be-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="620be-114">Feature</span></span><br/> |
| <span data-ttu-id="620be-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="620be-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="620be-116">Seite</span><span class="sxs-lookup"><span data-stu-id="620be-116">Page</span></span><br/>    |
| <span data-ttu-id="620be-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="620be-117">Notes</span></span> <br/>          | <span data-ttu-id="620be-118">Keine</span><span class="sxs-lookup"><span data-stu-id="620be-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="620be-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="620be-119">Structural Content</span></span>

<span data-ttu-id="620be-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="620be-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">_BackCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">_FrontCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_MaterialValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">_PrePrintedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">_PrePunchedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">_RecycledValue_</psf:Value>
    </psf:ScoredProperty>     
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_WeightValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="620be-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="620be-121">Structure Variables</span></span>

<span data-ttu-id="620be-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="620be-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="620be-123">Name</span><span class="sxs-lookup"><span data-stu-id="620be-123">Name</span></span>                               | <span data-ttu-id="620be-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="620be-124">Data type</span></span>          | <span data-ttu-id="620be-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="620be-125">Unit</span></span>                              | <span data-ttu-id="620be-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="620be-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="620be-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="620be-127">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="620be-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="620be-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="620be-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-129">string</span></span><br/>  | <span data-ttu-id="620be-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="620be-130">characters</span></span><br/>             | <span data-ttu-id="620be-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="620be-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="620be-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="620be-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="620be-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="620be-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="620be-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="620be-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-135">string</span></span><br/>  | <span data-ttu-id="620be-136">–</span><span class="sxs-lookup"><span data-stu-id="620be-136">n/a</span></span><br/>                    | <span data-ttu-id="620be-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="620be-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="620be-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="620be-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="620be-139">\_Backcoatingvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-139">\_BackCoatingValue\_</span></span><br/>    | <span data-ttu-id="620be-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-140">string</span></span><br/>  | <span data-ttu-id="620be-141">–</span><span class="sxs-lookup"><span data-stu-id="620be-141">n/a</span></span><br/>                    | <span data-ttu-id="620be-142">Hochglanz, HighGloss, Matt, None, Satin, Semigloss.</span><span class="sxs-lookup"><span data-stu-id="620be-142">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="620be-143">Gibt die Beschichtung der Rückseite des Mediums an.</span><span class="sxs-lookup"><span data-stu-id="620be-143">Specifies the coating of the back side of the media.</span></span><br/>              |
| <span data-ttu-id="620be-144">\_Frontcoatingvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-144">\_FrontCoatingValue\_</span></span><br/>   | <span data-ttu-id="620be-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-145">string</span></span><br/>  | <span data-ttu-id="620be-146">–</span><span class="sxs-lookup"><span data-stu-id="620be-146">n/a</span></span><br/>                    | <span data-ttu-id="620be-147">Hochglanz, HighGloss, Matt, None, Satin, Semigloss.</span><span class="sxs-lookup"><span data-stu-id="620be-147">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="620be-148">Gibt die Beschichtung der Vorderseite des Mediums an.</span><span class="sxs-lookup"><span data-stu-id="620be-148">Specifies the coating of the front side of the media.</span></span><br/>             |
| <span data-ttu-id="620be-149">\_Materialvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-149">\_MaterialValue\_</span></span><br/>       | <span data-ttu-id="620be-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-150">string</span></span><br/>  | <span data-ttu-id="620be-151">–</span><span class="sxs-lookup"><span data-stu-id="620be-151">n/a</span></span><br/>                    | <span data-ttu-id="620be-152">Aluminium, Display, dryfilm, Paper, Polyester, Transparenz, wetfilm.</span><span class="sxs-lookup"><span data-stu-id="620be-152">Aluminum, Display, DryFilm, Paper, Polyester, Transparency, WetFilm.</span></span><br/>                                                                                                       | <span data-ttu-id="620be-153">Gibt das Material an, aus dem die Medien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="620be-153">Specifies the material the media is made out of.</span></span><br/>                  |
| <span data-ttu-id="620be-154">\_Preprintedvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-154">\_PrePrintedValue\_</span></span><br/>     | <span data-ttu-id="620be-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-155">string</span></span><br/>  | <span data-ttu-id="620be-156">–</span><span class="sxs-lookup"><span data-stu-id="620be-156">n/a</span></span><br/>                    | <span data-ttu-id="620be-157">Keine, vorgedruckt, Briefkopf.</span><span class="sxs-lookup"><span data-stu-id="620be-157">None, PrePrinted, Letterhead.</span></span><br/>                                                                                                                                              | <span data-ttu-id="620be-158">Gibt Merkmale der vorab gedruckten Medien an.</span><span class="sxs-lookup"><span data-stu-id="620be-158">Specifies media preprinted characteristics.</span></span><br/>                       |
| <span data-ttu-id="620be-159">\_Prepunchedvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-159">\_PrePunchedValue\_</span></span><br/>     | <span data-ttu-id="620be-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-160">string</span></span><br/>  | <span data-ttu-id="620be-161">–</span><span class="sxs-lookup"><span data-stu-id="620be-161">n/a</span></span><br/>                    | <span data-ttu-id="620be-162">None, vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="620be-162">None, PrePunched.</span></span><br/>                                                                                                                                                          | <span data-ttu-id="620be-163">Gibt die vorgefertigte Medien Merkmale an.</span><span class="sxs-lookup"><span data-stu-id="620be-163">Specifies media prepunched characteristics.</span></span><br/>                       |
| <span data-ttu-id="620be-164">\_Recycledvalue\_</span><span class="sxs-lookup"><span data-stu-id="620be-164">\_RecycledValue\_</span></span><br/>       | <span data-ttu-id="620be-165">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="620be-165">string</span></span><br/>  | <span data-ttu-id="620be-166">–</span><span class="sxs-lookup"><span data-stu-id="620be-166">n/a</span></span><br/>                    | <span data-ttu-id="620be-167">None, Standard.</span><span class="sxs-lookup"><span data-stu-id="620be-167">None, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="620be-168">Gibt die wiederverwendeten Medien Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="620be-168">Specifies media recycled characteristics.</span></span><br/>                         |
| <span data-ttu-id="620be-169">\_Gewiweightwert\_</span><span class="sxs-lookup"><span data-stu-id="620be-169">\_WeightValue\_</span></span><br/>         | <span data-ttu-id="620be-170">integer</span><span class="sxs-lookup"><span data-stu-id="620be-170">integer</span></span><br/> | <span data-ttu-id="620be-171">grams pro Quadratmeter</span><span class="sxs-lookup"><span data-stu-id="620be-171">grams per square meter</span></span><br/> | <span data-ttu-id="620be-172">Größer 0</span><span class="sxs-lookup"><span data-stu-id="620be-172">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="620be-173">Gibt Medien Gewichtungs Merkmale an.</span><span class="sxs-lookup"><span data-stu-id="620be-173">Specifies media weight characteristics.</span></span><br/>                           |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="620be-174">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="620be-174">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="620be-175">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="620be-175">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="620be-176">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="620be-176">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies Media would be Automatically selected. -->
  <psf:Option name="psk:AutoSelect"/>
  <!-- Specifies archival quality media. -->
  <psf:Option name="psk:Archival">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty back printing film media. -->
  <psf:Option name="psk:BackPrintFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard bond media. -->
  <psf:Option name="psk:Bond">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard card stock media. -->
  <psf:Option name="psk:CardStock">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies continuous feed media. -->
  <psf:Option name="psk:Continous">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard envelope media. -->
  <psf:Option name="psk:EnvelopePlain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies windowed envelope media. -->
  <psf:Option name="psk:EnvelopeWindow">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies fabric media. -->
  <psf:Option name="psk:Fabric">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Polyester</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty high resolution media. -->
  <psf:Option name="psk:HighResolution">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies label media. -->
  <psf:Option name="psk:Label">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies attached multi-part forms media. -->
  <psf:Option name="psk:MultiLayerForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies separate multi-part forms media. -->
  <psf:Option name="psk:MultiPartForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard photographic media. -->
  <psf:Option name="psk:Photographic">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies film photographic media. -->
  <psf:Option name="psk:PhotographicFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies glossy photographic media. -->
  <psf:Option name="psk:PhotographicGlossy">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Glossy</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies high gloss photographic media. -->
  <psf:Option name="psk:PhotographicHighGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">HighGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies matte photographic media. -->
  <psf:Option name="psk:PhotographicMatte">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Matte</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies satin photographic media. -->
  <psf:Option name="psk:PhotographicSatin">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Satin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies semi-gloss photographic media. -->
  <psf:Option name="psk:PhotographicSemiGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">SemiGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard paper media. -->
  <psf:Option name="psk:Plain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in continuous form. -->
  <psf:Option name="psk:Screen">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in paged form. -->
  <psf:Option name="psk:ScreenPaged">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty stationery media. -->
  <psf:Option name="psk:Stationery">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">Letterhead</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is not pre-cut (single tabs). -->
  <psf:Option name="psk:TabStockFull">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is pre-cut (multiple tabs). -->
  <psf:Option name="psk:TabStockPreCut">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies transparency media. -->
  <psf:Option name="psk:Transparency">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Transparency</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty T-shirt transfer media. -->
  <psf:Option name="psk:TShirtTransfer">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies unknown or unlisted media. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="620be-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="620be-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="620be-178">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="620be-178">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
