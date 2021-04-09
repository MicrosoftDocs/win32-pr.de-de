---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: Paginput bin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c8d84b099fb11aa97dea6f242f08acdd532105
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869664"
---
# <a name="pageinputbin"></a><span data-ttu-id="2b762-104">Paginput bin</span><span class="sxs-lookup"><span data-stu-id="2b762-104">PageInputBin</span></span>

<span data-ttu-id="2b762-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2b762-105">This topic is not current.</span></span> <span data-ttu-id="2b762-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2b762-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2b762-107">Beschreibt den installierten Eingabe Korb in einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="2b762-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="2b762-108">Ermöglicht die Angabe des Eingabe-bin pro Seite.</span><span class="sxs-lookup"><span data-stu-id="2b762-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="2b762-109">Die Schlüsselwörter "JobInputBin", "DocumentInputBin" und "PageInputBin" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="2b762-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="2b762-110">Beide sollten nicht gleichzeitig in einem PrintTicket-oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b762-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="2b762-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2b762-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2b762-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2b762-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2b762-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2b762-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2b762-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2b762-114">Element Information</span></span>



| <span data-ttu-id="2b762-115">Name</span><span class="sxs-lookup"><span data-stu-id="2b762-115">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2b762-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2b762-116">Element Type</span></span> <br/>   | <span data-ttu-id="2b762-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="2b762-117">Feature</span></span><br/> |
| <span data-ttu-id="2b762-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="2b762-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2b762-119">Seite</span><span class="sxs-lookup"><span data-stu-id="2b762-119">Page</span></span><br/>    |
| <span data-ttu-id="2b762-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b762-120">Notes</span></span> <br/>          | <span data-ttu-id="2b762-121">Keine</span><span class="sxs-lookup"><span data-stu-id="2b762-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2b762-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2b762-122">Structural Content</span></span>

<span data-ttu-id="2b762-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="2b762-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2b762-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="2b762-124">Structure Variables</span></span>

<span data-ttu-id="2b762-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2b762-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2b762-126">Name</span><span class="sxs-lookup"><span data-stu-id="2b762-126">Name</span></span>                                   | <span data-ttu-id="2b762-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2b762-127">Data type</span></span>          | <span data-ttu-id="2b762-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="2b762-128">Unit</span></span>                  | <span data-ttu-id="2b762-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="2b762-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2b762-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2b762-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b762-131">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="2b762-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="2b762-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-132">string</span></span><br/>  | <span data-ttu-id="2b762-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="2b762-133">characters</span></span><br/> | <span data-ttu-id="2b762-134">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="2b762-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2b762-135">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="2b762-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2b762-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="2b762-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="2b762-137">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="2b762-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-138">string</span></span><br/>  | <span data-ttu-id="2b762-139">–</span><span class="sxs-lookup"><span data-stu-id="2b762-139">n/a</span></span><br/>        | <span data-ttu-id="2b762-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="2b762-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2b762-141">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2b762-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2b762-142">\_Envelopeoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="2b762-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-143">string</span></span><br/>  | <span data-ttu-id="2b762-144">–</span><span class="sxs-lookup"><span data-stu-id="2b762-144">n/a</span></span><br/>        | <span data-ttu-id="2b762-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="2b762-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2b762-146">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2b762-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2b762-147">\_Bintypevalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="2b762-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-148">string</span></span><br/>  | <span data-ttu-id="2b762-149">–</span><span class="sxs-lookup"><span data-stu-id="2b762-149">n/a</span></span><br/>        | <span data-ttu-id="2b762-150">Continuousfeed, Sheetfeed.</span><span class="sxs-lookup"><span data-stu-id="2b762-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="2b762-151">Gibt den Typ der bin an.</span><span class="sxs-lookup"><span data-stu-id="2b762-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="2b762-152">\_Feedtypevalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="2b762-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-153">string</span></span><br/>  | <span data-ttu-id="2b762-154">–</span><span class="sxs-lookup"><span data-stu-id="2b762-154">n/a</span></span><br/>        | <span data-ttu-id="2b762-155">Automatisch, manuell.</span><span class="sxs-lookup"><span data-stu-id="2b762-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="2b762-156">Gibt den Feed-Mechanismus der bin an.</span><span class="sxs-lookup"><span data-stu-id="2b762-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="2b762-157">\_Mediacapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="2b762-158">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-158">string</span></span><br/>  | <span data-ttu-id="2b762-159">–</span><span class="sxs-lookup"><span data-stu-id="2b762-159">n/a</span></span><br/>        | <span data-ttu-id="2b762-160">Hoch, Standard.</span><span class="sxs-lookup"><span data-stu-id="2b762-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="2b762-161">Gibt an, ob der bin ein hoher Kapazitäts-bin (qualitativ) ist.</span><span class="sxs-lookup"><span data-stu-id="2b762-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="2b762-162">\_Mediasizeautosenendvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2b762-163">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-163">string</span></span><br/>  | <span data-ttu-id="2b762-164">–</span><span class="sxs-lookup"><span data-stu-id="2b762-164">n/a</span></span><br/>        | <span data-ttu-id="2b762-165">Unterstützt, keine.</span><span class="sxs-lookup"><span data-stu-id="2b762-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2b762-166">Gibt die Mediengröße für die automatische Sense-Funktion des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="2b762-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="2b762-167">\_Mediatypeer autosensvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2b762-168">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-168">string</span></span><br/>  | <span data-ttu-id="2b762-169">–</span><span class="sxs-lookup"><span data-stu-id="2b762-169">n/a</span></span><br/>        | <span data-ttu-id="2b762-170">Unterstützt, keine.</span><span class="sxs-lookup"><span data-stu-id="2b762-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2b762-171">Gibt die Auto-Sense-Funktion des Medientyps des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="2b762-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="2b762-172">\_Mediasheetcapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="2b762-173">integer</span><span class="sxs-lookup"><span data-stu-id="2b762-173">integer</span></span><br/> | <span data-ttu-id="2b762-174">Glas</span><span class="sxs-lookup"><span data-stu-id="2b762-174">sheets</span></span><br/>     | <span data-ttu-id="2b762-175">Die maximale ganzzahlige Einschränkung ist vom Gerät zugelassen.</span><span class="sxs-lookup"><span data-stu-id="2b762-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="2b762-176">Gibt die Medien Kapazität in der Anzahl der Seiten (vollständig) des bin an.</span><span class="sxs-lookup"><span data-stu-id="2b762-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="2b762-177">\_Mediapathvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="2b762-178">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-178">string</span></span><br/>  | <span data-ttu-id="2b762-179">–</span><span class="sxs-lookup"><span data-stu-id="2b762-179">n/a</span></span><br/>        | <span data-ttu-id="2b762-180">Direkt, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="2b762-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="2b762-181">Gibt die Merkmale des Medien Pfads an.</span><span class="sxs-lookup"><span data-stu-id="2b762-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="2b762-182">\_Feedwert\_</span><span class="sxs-lookup"><span data-stu-id="2b762-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="2b762-183">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-183">string</span></span><br/>  | <span data-ttu-id="2b762-184">–</span><span class="sxs-lookup"><span data-stu-id="2b762-184">n/a</span></span><br/>        | <span data-ttu-id="2b762-185">FaceUp, Facedown</span><span class="sxs-lookup"><span data-stu-id="2b762-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2b762-186">Gibt an, ob Medien gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b762-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="2b762-187">\_Feeddirectionvalue\_</span><span class="sxs-lookup"><span data-stu-id="2b762-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="2b762-188">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b762-188">string</span></span><br/>  | <span data-ttu-id="2b762-189">–</span><span class="sxs-lookup"><span data-stu-id="2b762-189">n/a</span></span><br/>        | <span data-ttu-id="2b762-190">Longedgefirst, shortedgefirst</span><span class="sxs-lookup"><span data-stu-id="2b762-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="2b762-191">Gibt an, ob die Medien zuerst den langen Edge-oder kurzen Edge-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2b762-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2b762-192">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2b762-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2b762-193">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="2b762-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2b762-194">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="2b762-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2b762-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b762-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b762-196">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="2b762-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




