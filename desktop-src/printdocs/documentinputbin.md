---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997767"
---
# <a name="documentinputbin"></a><span data-ttu-id="15c8d-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="15c8d-104">DocumentInputBin</span></span>

<span data-ttu-id="15c8d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="15c8d-105">This topic is not current.</span></span> <span data-ttu-id="15c8d-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="15c8d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15c8d-107">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="15c8d-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="15c8d-108">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="15c8d-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="15c8d-109">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15c8d-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="15c8d-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15c8d-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="15c8d-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="15c8d-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="15c8d-112">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="15c8d-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="15c8d-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15c8d-113">Element Information</span></span>



| <span data-ttu-id="15c8d-114">Name</span><span class="sxs-lookup"><span data-stu-id="15c8d-114">Name</span></span> | <span data-ttu-id="15c8d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="15c8d-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c8d-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="15c8d-116">Element Type</span></span> <br/>   | <span data-ttu-id="15c8d-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="15c8d-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="15c8d-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="15c8d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15c8d-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="15c8d-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="15c8d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15c8d-120">Notes</span></span> <br/>          | <span data-ttu-id="15c8d-121">Unterstützte, derzeit nicht installierte Bins sollten im PrintCapabilities-Dokument als eingeschränkt gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="15c8d-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="15c8d-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="15c8d-122">Structural Content</span></span>

<span data-ttu-id="15c8d-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="15c8d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="15c8d-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="15c8d-124">Structure Variables</span></span>

<span data-ttu-id="15c8d-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="15c8d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15c8d-126">Name</span><span class="sxs-lookup"><span data-stu-id="15c8d-126">Name</span></span>                                   | <span data-ttu-id="15c8d-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="15c8d-127">Data type</span></span>          | <span data-ttu-id="15c8d-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="15c8d-128">Unit</span></span>                  | <span data-ttu-id="15c8d-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="15c8d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="15c8d-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="15c8d-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15c8d-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="15c8d-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-132">string</span></span><br/>  | <span data-ttu-id="15c8d-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="15c8d-133">characters</span></span><br/> | <span data-ttu-id="15c8d-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="15c8d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="15c8d-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="15c8d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="15c8d-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="15c8d-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="15c8d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="15c8d-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-138">string</span></span><br/>  | <span data-ttu-id="15c8d-139">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-139">n/a</span></span><br/>        | <span data-ttu-id="15c8d-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="15c8d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="15c8d-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="15c8d-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="15c8d-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="15c8d-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-143">string</span></span><br/>  | <span data-ttu-id="15c8d-144">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-144">n/a</span></span><br/>        | <span data-ttu-id="15c8d-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="15c8d-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="15c8d-146">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="15c8d-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="15c8d-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="15c8d-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-148">string</span></span><br/>  | <span data-ttu-id="15c8d-149">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-149">n/a</span></span><br/>        | <span data-ttu-id="15c8d-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="15c8d-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="15c8d-151">Gibt den Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="15c8d-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="15c8d-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="15c8d-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-153">string</span></span><br/>  | <span data-ttu-id="15c8d-154">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-154">n/a</span></span><br/>        | <span data-ttu-id="15c8d-155">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="15c8d-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="15c8d-156">Gibt den Feedmechanismus des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="15c8d-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="15c8d-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="15c8d-158">integer</span><span class="sxs-lookup"><span data-stu-id="15c8d-158">integer</span></span><br/> | <span data-ttu-id="15c8d-159">Blätter</span><span class="sxs-lookup"><span data-stu-id="15c8d-159">sheets</span></span><br/>     | <span data-ttu-id="15c8d-160">Maximal zulässige ganzzahlige Einschränkung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="15c8d-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="15c8d-161">Gibt an, ob es sich bei dem Container um einen Container mit hoher Kapazität (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="15c8d-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="15c8d-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="15c8d-163">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-163">string</span></span><br/>  | <span data-ttu-id="15c8d-164">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-164">n/a</span></span><br/>        | <span data-ttu-id="15c8d-165">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="15c8d-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="15c8d-166">Gibt die Funktion zur automatischen Empfindlichkeit der Mediengröße des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="15c8d-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="15c8d-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="15c8d-168">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-168">string</span></span><br/>  | <span data-ttu-id="15c8d-169">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-169">n/a</span></span><br/>        | <span data-ttu-id="15c8d-170">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="15c8d-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="15c8d-171">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="15c8d-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="15c8d-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="15c8d-173">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-173">string</span></span><br/>  | <span data-ttu-id="15c8d-174">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-174">n/a</span></span><br/>        | <span data-ttu-id="15c8d-175">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="15c8d-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="15c8d-176">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="15c8d-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="15c8d-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="15c8d-178">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-178">string</span></span><br/>  | <span data-ttu-id="15c8d-179">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-179">n/a</span></span><br/>        | <span data-ttu-id="15c8d-180">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="15c8d-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="15c8d-181">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15c8d-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="15c8d-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="15c8d-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="15c8d-183">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15c8d-183">string</span></span><br/>  | <span data-ttu-id="15c8d-184">–</span><span class="sxs-lookup"><span data-stu-id="15c8d-184">n/a</span></span><br/>        | <span data-ttu-id="15c8d-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="15c8d-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="15c8d-186">Gibt an, ob das Medium zuerst einen langen Edge oder einen kurzen Rand einfährt.</span><span class="sxs-lookup"><span data-stu-id="15c8d-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="15c8d-187">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="15c8d-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="15c8d-188">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="15c8d-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="15c8d-189">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="15c8d-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="15c8d-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15c8d-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c8d-191">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="15c8d-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




