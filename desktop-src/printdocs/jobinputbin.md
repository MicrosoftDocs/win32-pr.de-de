---
description: Erfahren Sie mehr über das JobInputBin-Element, das den installierten Eingabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät beschreibt.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929df4cb4871e5a8d2ebacfe533b5da3ad9babf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408893"
---
# <a name="jobinputbin"></a><span data-ttu-id="cc654-103">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="cc654-103">JobInputBin</span></span>

<span data-ttu-id="cc654-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="cc654-104">This topic is not current.</span></span> <span data-ttu-id="cc654-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="cc654-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc654-106">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="cc654-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="cc654-107">Ermöglicht die Angabe des Eingabebehälters pro Auftrag.</span><span class="sxs-lookup"><span data-stu-id="cc654-107">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="cc654-108">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="cc654-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="cc654-109">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc654-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="cc654-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cc654-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc654-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="cc654-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cc654-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="cc654-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cc654-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cc654-113">Element Information</span></span>



| <span data-ttu-id="cc654-114">Name</span><span class="sxs-lookup"><span data-stu-id="cc654-114">Name</span></span> | <span data-ttu-id="cc654-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cc654-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="cc654-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="cc654-116">Element Type</span></span> <br/>   | <span data-ttu-id="cc654-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="cc654-117">Feature</span></span><br/> |
| <span data-ttu-id="cc654-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="cc654-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc654-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="cc654-119">Job</span></span><br/>     |
| <span data-ttu-id="cc654-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc654-120">Notes</span></span> <br/>          | <span data-ttu-id="cc654-121">Keine</span><span class="sxs-lookup"><span data-stu-id="cc654-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="cc654-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="cc654-122">Structural Content</span></span>

<span data-ttu-id="cc654-123">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc654-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="cc654-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="cc654-124">Structure Variables</span></span>

<span data-ttu-id="cc654-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cc654-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc654-126">Name</span><span class="sxs-lookup"><span data-stu-id="cc654-126">Name</span></span>                                   | <span data-ttu-id="cc654-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cc654-127">Data type</span></span>          | <span data-ttu-id="cc654-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="cc654-128">Unit</span></span>                  | <span data-ttu-id="cc654-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="cc654-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cc654-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cc654-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc654-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="cc654-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="cc654-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-132">string</span></span><br/>  | <span data-ttu-id="cc654-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="cc654-133">characters</span></span><br/> | <span data-ttu-id="cc654-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="cc654-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cc654-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="cc654-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cc654-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="cc654-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="cc654-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="cc654-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-138">string</span></span><br/>  | <span data-ttu-id="cc654-139">–</span><span class="sxs-lookup"><span data-stu-id="cc654-139">n/a</span></span><br/>        | <span data-ttu-id="cc654-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="cc654-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cc654-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="cc654-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="cc654-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="cc654-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-143">string</span></span><br/>  | <span data-ttu-id="cc654-144">–</span><span class="sxs-lookup"><span data-stu-id="cc654-144">n/a</span></span><br/>        | <span data-ttu-id="cc654-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="cc654-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cc654-146">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="cc654-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="cc654-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="cc654-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-148">string</span></span><br/>  | <span data-ttu-id="cc654-149">–</span><span class="sxs-lookup"><span data-stu-id="cc654-149">n/a</span></span><br/>        | <span data-ttu-id="cc654-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="cc654-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="cc654-151">Gibt den Typ des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="cc654-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="cc654-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="cc654-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-153">string</span></span><br/>  | <span data-ttu-id="cc654-154">–</span><span class="sxs-lookup"><span data-stu-id="cc654-154">n/a</span></span><br/>        | <span data-ttu-id="cc654-155">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="cc654-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="cc654-156">Gibt den Feedmechanismus des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="cc654-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="cc654-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="cc654-158">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-158">string</span></span><br/>  | <span data-ttu-id="cc654-159">–</span><span class="sxs-lookup"><span data-stu-id="cc654-159">n/a</span></span><br/>        | <span data-ttu-id="cc654-160">Hoch, Standard.</span><span class="sxs-lookup"><span data-stu-id="cc654-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="cc654-161">Gibt an, ob es sich bei der Behälter um einen Hochkapazitätsbehälter (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="cc654-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="cc654-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="cc654-163">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-163">string</span></span><br/>  | <span data-ttu-id="cc654-164">–</span><span class="sxs-lookup"><span data-stu-id="cc654-164">n/a</span></span><br/>        | <span data-ttu-id="cc654-165">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="cc654-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cc654-166">Gibt die Funktion zur automatischen Nutzung der Mediengröße des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="cc654-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="cc654-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="cc654-168">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-168">string</span></span><br/>  | <span data-ttu-id="cc654-169">–</span><span class="sxs-lookup"><span data-stu-id="cc654-169">n/a</span></span><br/>        | <span data-ttu-id="cc654-170">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="cc654-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cc654-171">Gibt die Funktion für den automatischen Medientypsendung des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="cc654-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="cc654-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="cc654-173">integer</span><span class="sxs-lookup"><span data-stu-id="cc654-173">integer</span></span><br/> | <span data-ttu-id="cc654-174">Blätter</span><span class="sxs-lookup"><span data-stu-id="cc654-174">sheets</span></span><br/>     | <span data-ttu-id="cc654-175">Maximale ganzzahlige Einschränkung, die vom Gerät zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="cc654-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="cc654-176">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="cc654-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="cc654-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="cc654-178">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-178">string</span></span><br/>  | <span data-ttu-id="cc654-179">–</span><span class="sxs-lookup"><span data-stu-id="cc654-179">n/a</span></span><br/>        | <span data-ttu-id="cc654-180">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="cc654-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="cc654-181">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="cc654-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="cc654-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="cc654-183">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-183">string</span></span><br/>  | <span data-ttu-id="cc654-184">–</span><span class="sxs-lookup"><span data-stu-id="cc654-184">n/a</span></span><br/>        | <span data-ttu-id="cc654-185">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="cc654-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cc654-186">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc654-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="cc654-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="cc654-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="cc654-188">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc654-188">string</span></span><br/>  | <span data-ttu-id="cc654-189">–</span><span class="sxs-lookup"><span data-stu-id="cc654-189">n/a</span></span><br/>        | <span data-ttu-id="cc654-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="cc654-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="cc654-191">Gibt an, ob medien zuerst lange Kanten oder kurze Kanten gespeist werden.</span><span class="sxs-lookup"><span data-stu-id="cc654-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cc654-192">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="cc654-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cc654-193">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="cc654-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cc654-194">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="cc654-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="cc654-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc654-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc654-196">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="cc654-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




