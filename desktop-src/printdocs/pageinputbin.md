---
description: Abrufen von Informationen über das vom Benutzer konfigurierbare PageInputBin-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549168"
---
# <a name="pageinputbin"></a><span data-ttu-id="9a2af-105">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="9a2af-105">PageInputBin</span></span>

<span data-ttu-id="9a2af-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9a2af-106">This topic is not current.</span></span> <span data-ttu-id="9a2af-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="9a2af-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9a2af-108">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="9a2af-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="9a2af-109">Ermöglicht die Angabe des Eingabecontainers pro Seite.</span><span class="sxs-lookup"><span data-stu-id="9a2af-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="9a2af-110">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="9a2af-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="9a2af-111">Beide sollten nicht gleichzeitig in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a2af-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9a2af-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9a2af-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9a2af-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="9a2af-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9a2af-114">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="9a2af-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9a2af-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9a2af-115">Element Information</span></span>



| <span data-ttu-id="9a2af-116">Name</span><span class="sxs-lookup"><span data-stu-id="9a2af-116">Name</span></span> | <span data-ttu-id="9a2af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9a2af-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9a2af-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9a2af-118">Element Type</span></span> <br/>   | <span data-ttu-id="9a2af-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="9a2af-119">Feature</span></span><br/> |
| <span data-ttu-id="9a2af-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="9a2af-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9a2af-121">Seite</span><span class="sxs-lookup"><span data-stu-id="9a2af-121">Page</span></span><br/>    |
| <span data-ttu-id="9a2af-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a2af-122">Notes</span></span> <br/>          | <span data-ttu-id="9a2af-123">Keine</span><span class="sxs-lookup"><span data-stu-id="9a2af-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9a2af-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="9a2af-124">Structural Content</span></span>

<span data-ttu-id="9a2af-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9a2af-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="9a2af-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9a2af-126">Structure Variables</span></span>

<span data-ttu-id="9a2af-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9a2af-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9a2af-128">Name</span><span class="sxs-lookup"><span data-stu-id="9a2af-128">Name</span></span>                                   | <span data-ttu-id="9a2af-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9a2af-129">Data type</span></span>          | <span data-ttu-id="9a2af-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="9a2af-130">Unit</span></span>                  | <span data-ttu-id="9a2af-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9a2af-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9a2af-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9a2af-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2af-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9a2af-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-134">string</span></span><br/>  | <span data-ttu-id="9a2af-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9a2af-135">characters</span></span><br/> | <span data-ttu-id="9a2af-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9a2af-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9a2af-137">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9a2af-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9a2af-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9a2af-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="9a2af-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9a2af-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-140">string</span></span><br/>  | <span data-ttu-id="9a2af-141">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-141">n/a</span></span><br/>        | <span data-ttu-id="9a2af-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9a2af-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9a2af-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2af-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9a2af-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="9a2af-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-145">string</span></span><br/>  | <span data-ttu-id="9a2af-146">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-146">n/a</span></span><br/>        | <span data-ttu-id="9a2af-147">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9a2af-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9a2af-148">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2af-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9a2af-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="9a2af-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-150">string</span></span><br/>  | <span data-ttu-id="9a2af-151">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-151">n/a</span></span><br/>        | <span data-ttu-id="9a2af-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="9a2af-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="9a2af-153">Gibt den Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="9a2af-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="9a2af-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-155">string</span></span><br/>  | <span data-ttu-id="9a2af-156">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-156">n/a</span></span><br/>        | <span data-ttu-id="9a2af-157">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="9a2af-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="9a2af-158">Gibt den Feedmechanismus des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="9a2af-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="9a2af-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-160">string</span></span><br/>  | <span data-ttu-id="9a2af-161">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-161">n/a</span></span><br/>        | <span data-ttu-id="9a2af-162">Hoch, Standard.</span><span class="sxs-lookup"><span data-stu-id="9a2af-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="9a2af-163">Gibt an, ob es sich bei dem Container um einen Container mit hoher Kapazität (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="9a2af-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="9a2af-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9a2af-165">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-165">string</span></span><br/>  | <span data-ttu-id="9a2af-166">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-166">n/a</span></span><br/>        | <span data-ttu-id="9a2af-167">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="9a2af-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9a2af-168">Gibt die Funktion zur automatischen Empfindlichkeit des Geräts für die Mediengröße an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="9a2af-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9a2af-170">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-170">string</span></span><br/>  | <span data-ttu-id="9a2af-171">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-171">n/a</span></span><br/>        | <span data-ttu-id="9a2af-172">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="9a2af-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9a2af-173">Gibt die Funktion für den automatischen Sinn des Medientyps des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="9a2af-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="9a2af-175">integer</span><span class="sxs-lookup"><span data-stu-id="9a2af-175">integer</span></span><br/> | <span data-ttu-id="9a2af-176">Blätter</span><span class="sxs-lookup"><span data-stu-id="9a2af-176">sheets</span></span><br/>     | <span data-ttu-id="9a2af-177">Maximal zulässige ganzzahlige Einschränkung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9a2af-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="9a2af-178">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="9a2af-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="9a2af-180">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-180">string</span></span><br/>  | <span data-ttu-id="9a2af-181">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-181">n/a</span></span><br/>        | <span data-ttu-id="9a2af-182">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="9a2af-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="9a2af-183">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="9a2af-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="9a2af-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="9a2af-185">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-185">string</span></span><br/>  | <span data-ttu-id="9a2af-186">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-186">n/a</span></span><br/>        | <span data-ttu-id="9a2af-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="9a2af-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9a2af-188">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a2af-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="9a2af-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a2af-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="9a2af-190">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9a2af-190">string</span></span><br/>  | <span data-ttu-id="9a2af-191">n/v</span><span class="sxs-lookup"><span data-stu-id="9a2af-191">n/a</span></span><br/>        | <span data-ttu-id="9a2af-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="9a2af-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="9a2af-193">Gibt an, ob dem Medium zuerst der lange Rand oder zuerst der kurze Rand zugeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2af-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9a2af-194">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="9a2af-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9a2af-195">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9a2af-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9a2af-196">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9a2af-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="9a2af-197">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a2af-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a2af-198">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="9a2af-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




