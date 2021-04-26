---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74e75653f7c6cbc6a586b80b3e8217286ce7c36
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993767"
---
# <a name="pageinputbin"></a><span data-ttu-id="14396-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="14396-104">PageInputBin</span></span>

<span data-ttu-id="14396-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="14396-105">This topic is not current.</span></span> <span data-ttu-id="14396-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="14396-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="14396-107">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="14396-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="14396-108">Ermöglicht die Angabe des Eingabebehälters pro Seite.</span><span class="sxs-lookup"><span data-stu-id="14396-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="14396-109">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="14396-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="14396-110">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14396-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="14396-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="14396-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="14396-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="14396-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="14396-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="14396-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="14396-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="14396-114">Element Information</span></span>



| <span data-ttu-id="14396-115">Name</span><span class="sxs-lookup"><span data-stu-id="14396-115">Name</span></span> | <span data-ttu-id="14396-116">Wert</span><span class="sxs-lookup"><span data-stu-id="14396-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="14396-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="14396-117">Element Type</span></span> <br/>   | <span data-ttu-id="14396-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="14396-118">Feature</span></span><br/> |
| <span data-ttu-id="14396-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="14396-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="14396-120">Seite</span><span class="sxs-lookup"><span data-stu-id="14396-120">Page</span></span><br/>    |
| <span data-ttu-id="14396-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14396-121">Notes</span></span> <br/>          | <span data-ttu-id="14396-122">Keine</span><span class="sxs-lookup"><span data-stu-id="14396-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="14396-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="14396-123">Structural Content</span></span>

<span data-ttu-id="14396-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="14396-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="14396-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="14396-125">Structure Variables</span></span>

<span data-ttu-id="14396-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="14396-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="14396-127">Name</span><span class="sxs-lookup"><span data-stu-id="14396-127">Name</span></span>                                   | <span data-ttu-id="14396-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="14396-128">Data type</span></span>          | <span data-ttu-id="14396-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="14396-129">Unit</span></span>                  | <span data-ttu-id="14396-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="14396-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="14396-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="14396-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14396-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="14396-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="14396-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-133">string</span></span><br/>  | <span data-ttu-id="14396-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="14396-134">characters</span></span><br/> | <span data-ttu-id="14396-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="14396-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="14396-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="14396-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="14396-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="14396-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="14396-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="14396-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-139">string</span></span><br/>  | <span data-ttu-id="14396-140">–</span><span class="sxs-lookup"><span data-stu-id="14396-140">n/a</span></span><br/>        | <span data-ttu-id="14396-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="14396-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="14396-142">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="14396-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="14396-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="14396-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-144">string</span></span><br/>  | <span data-ttu-id="14396-145">–</span><span class="sxs-lookup"><span data-stu-id="14396-145">n/a</span></span><br/>        | <span data-ttu-id="14396-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="14396-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="14396-147">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="14396-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="14396-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="14396-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-149">string</span></span><br/>  | <span data-ttu-id="14396-150">–</span><span class="sxs-lookup"><span data-stu-id="14396-150">n/a</span></span><br/>        | <span data-ttu-id="14396-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="14396-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="14396-152">Gibt den Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="14396-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="14396-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="14396-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-154">string</span></span><br/>  | <span data-ttu-id="14396-155">–</span><span class="sxs-lookup"><span data-stu-id="14396-155">n/a</span></span><br/>        | <span data-ttu-id="14396-156">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="14396-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="14396-157">Gibt den Feedmechanismus des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="14396-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="14396-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="14396-159">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-159">string</span></span><br/>  | <span data-ttu-id="14396-160">–</span><span class="sxs-lookup"><span data-stu-id="14396-160">n/a</span></span><br/>        | <span data-ttu-id="14396-161">Hoch, Standard.</span><span class="sxs-lookup"><span data-stu-id="14396-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="14396-162">Gibt an, ob es sich bei dem Container um einen Container mit hoher Kapazität (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="14396-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="14396-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="14396-164">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-164">string</span></span><br/>  | <span data-ttu-id="14396-165">–</span><span class="sxs-lookup"><span data-stu-id="14396-165">n/a</span></span><br/>        | <span data-ttu-id="14396-166">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="14396-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="14396-167">Gibt die Funktion zur automatischen Empfindlichkeit der Mediengröße des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="14396-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="14396-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="14396-169">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-169">string</span></span><br/>  | <span data-ttu-id="14396-170">–</span><span class="sxs-lookup"><span data-stu-id="14396-170">n/a</span></span><br/>        | <span data-ttu-id="14396-171">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="14396-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="14396-172">Gibt die Funktion für den automatischen Sinn des Medientyps des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="14396-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="14396-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="14396-174">integer</span><span class="sxs-lookup"><span data-stu-id="14396-174">integer</span></span><br/> | <span data-ttu-id="14396-175">Blätter</span><span class="sxs-lookup"><span data-stu-id="14396-175">sheets</span></span><br/>     | <span data-ttu-id="14396-176">Maximale ganzzahlige Einschränkung, die vom Gerät zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="14396-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="14396-177">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="14396-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="14396-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="14396-179">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-179">string</span></span><br/>  | <span data-ttu-id="14396-180">–</span><span class="sxs-lookup"><span data-stu-id="14396-180">n/a</span></span><br/>        | <span data-ttu-id="14396-181">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="14396-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="14396-182">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="14396-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="14396-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="14396-184">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-184">string</span></span><br/>  | <span data-ttu-id="14396-185">–</span><span class="sxs-lookup"><span data-stu-id="14396-185">n/a</span></span><br/>        | <span data-ttu-id="14396-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="14396-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="14396-187">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="14396-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="14396-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="14396-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="14396-189">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14396-189">string</span></span><br/>  | <span data-ttu-id="14396-190">–</span><span class="sxs-lookup"><span data-stu-id="14396-190">n/a</span></span><br/>        | <span data-ttu-id="14396-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="14396-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="14396-192">Gibt an, ob das Medium zuerst einen langen Edge oder einen kurzen Rand einfährt.</span><span class="sxs-lookup"><span data-stu-id="14396-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="14396-193">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="14396-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="14396-194">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="14396-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="14396-195">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="14396-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="14396-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14396-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14396-197">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="14396-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




