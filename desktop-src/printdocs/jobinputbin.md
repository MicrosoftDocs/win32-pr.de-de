---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f87782d6cf9aae5c34d36603f025e803f47db3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998097"
---
# <a name="jobinputbin"></a><span data-ttu-id="a15bc-104">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="a15bc-104">JobInputBin</span></span>

<span data-ttu-id="a15bc-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a15bc-105">This topic is not current.</span></span> <span data-ttu-id="a15bc-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a15bc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a15bc-107">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="a15bc-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="a15bc-108">Ermöglicht die Angabe des Eingabebehälters pro Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a15bc-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="a15bc-109">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="a15bc-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="a15bc-110">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a15bc-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a15bc-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a15bc-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a15bc-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a15bc-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a15bc-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a15bc-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a15bc-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a15bc-114">Element Information</span></span>



| <span data-ttu-id="a15bc-115">Name</span><span class="sxs-lookup"><span data-stu-id="a15bc-115">Name</span></span> | <span data-ttu-id="a15bc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a15bc-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a15bc-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a15bc-117">Element Type</span></span> <br/>   | <span data-ttu-id="a15bc-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="a15bc-118">Feature</span></span><br/> |
| <span data-ttu-id="a15bc-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a15bc-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a15bc-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a15bc-120">Job</span></span><br/>     |
| <span data-ttu-id="a15bc-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a15bc-121">Notes</span></span> <br/>          | <span data-ttu-id="a15bc-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a15bc-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a15bc-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a15bc-123">Structural Content</span></span>

<span data-ttu-id="a15bc-124">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a15bc-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a15bc-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a15bc-125">Structure Variables</span></span>

<span data-ttu-id="a15bc-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a15bc-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a15bc-127">Name</span><span class="sxs-lookup"><span data-stu-id="a15bc-127">Name</span></span>                                   | <span data-ttu-id="a15bc-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a15bc-128">Data type</span></span>          | <span data-ttu-id="a15bc-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="a15bc-129">Unit</span></span>                  | <span data-ttu-id="a15bc-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a15bc-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a15bc-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a15bc-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a15bc-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="a15bc-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-133">string</span></span><br/>  | <span data-ttu-id="a15bc-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a15bc-134">characters</span></span><br/> | <span data-ttu-id="a15bc-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a15bc-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a15bc-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a15bc-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a15bc-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a15bc-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="a15bc-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="a15bc-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-139">string</span></span><br/>  | <span data-ttu-id="a15bc-140">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-140">n/a</span></span><br/>        | <span data-ttu-id="a15bc-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a15bc-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a15bc-142">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a15bc-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a15bc-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="a15bc-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-144">string</span></span><br/>  | <span data-ttu-id="a15bc-145">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-145">n/a</span></span><br/>        | <span data-ttu-id="a15bc-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a15bc-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a15bc-147">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a15bc-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a15bc-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="a15bc-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-149">string</span></span><br/>  | <span data-ttu-id="a15bc-150">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-150">n/a</span></span><br/>        | <span data-ttu-id="a15bc-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="a15bc-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="a15bc-152">Gibt den Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="a15bc-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="a15bc-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-154">string</span></span><br/>  | <span data-ttu-id="a15bc-155">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-155">n/a</span></span><br/>        | <span data-ttu-id="a15bc-156">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="a15bc-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="a15bc-157">Gibt den Feedmechanismus des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="a15bc-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="a15bc-159">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-159">string</span></span><br/>  | <span data-ttu-id="a15bc-160">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-160">n/a</span></span><br/>        | <span data-ttu-id="a15bc-161">Hoch, Standard.</span><span class="sxs-lookup"><span data-stu-id="a15bc-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a15bc-162">Gibt an, ob es sich bei dem Container um einen Container mit hoher Kapazität (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="a15bc-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="a15bc-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a15bc-164">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-164">string</span></span><br/>  | <span data-ttu-id="a15bc-165">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-165">n/a</span></span><br/>        | <span data-ttu-id="a15bc-166">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="a15bc-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a15bc-167">Gibt die Funktion zur automatischen Empfindlichkeit der Mediengröße des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="a15bc-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a15bc-169">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-169">string</span></span><br/>  | <span data-ttu-id="a15bc-170">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-170">n/a</span></span><br/>        | <span data-ttu-id="a15bc-171">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="a15bc-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a15bc-172">Gibt die Funktion für den automatischen Sinn des Medientyps des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="a15bc-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="a15bc-174">integer</span><span class="sxs-lookup"><span data-stu-id="a15bc-174">integer</span></span><br/> | <span data-ttu-id="a15bc-175">Blätter</span><span class="sxs-lookup"><span data-stu-id="a15bc-175">sheets</span></span><br/>     | <span data-ttu-id="a15bc-176">Maximal zulässige ganzzahlige Einschränkung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a15bc-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="a15bc-177">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="a15bc-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="a15bc-179">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-179">string</span></span><br/>  | <span data-ttu-id="a15bc-180">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-180">n/a</span></span><br/>        | <span data-ttu-id="a15bc-181">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="a15bc-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="a15bc-182">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="a15bc-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="a15bc-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="a15bc-184">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-184">string</span></span><br/>  | <span data-ttu-id="a15bc-185">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-185">n/a</span></span><br/>        | <span data-ttu-id="a15bc-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="a15bc-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a15bc-187">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a15bc-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="a15bc-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="a15bc-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="a15bc-189">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a15bc-189">string</span></span><br/>  | <span data-ttu-id="a15bc-190">–</span><span class="sxs-lookup"><span data-stu-id="a15bc-190">n/a</span></span><br/>        | <span data-ttu-id="a15bc-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="a15bc-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="a15bc-192">Gibt an, ob dem Medium zuerst der lange Rand oder zuerst der kurze Rand zugeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a15bc-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a15bc-193">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a15bc-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a15bc-194">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a15bc-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a15bc-195">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a15bc-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a15bc-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a15bc-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a15bc-197">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a15bc-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




