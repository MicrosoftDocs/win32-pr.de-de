---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357177"
---
# <a name="documentinputbin"></a><span data-ttu-id="18f6f-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="18f6f-104">DocumentInputBin</span></span>

<span data-ttu-id="18f6f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="18f6f-105">This topic is not current.</span></span> <span data-ttu-id="18f6f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="18f6f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="18f6f-107">Beschreibt den installierten Eingabe Korb in einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="18f6f-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="18f6f-108">Die Schlüsselwörter "JobInputBin", "DocumentInputBin" und "PageInputBin" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="18f6f-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="18f6f-109">Beide sollten nicht gleichzeitig in einem PrintTicket-oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="18f6f-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="18f6f-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="18f6f-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="18f6f-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="18f6f-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="18f6f-112">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="18f6f-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="18f6f-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="18f6f-113">Element Information</span></span>



| <span data-ttu-id="18f6f-114">Name</span><span class="sxs-lookup"><span data-stu-id="18f6f-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f6f-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="18f6f-115">Element Type</span></span> <br/>   | <span data-ttu-id="18f6f-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="18f6f-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="18f6f-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="18f6f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="18f6f-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="18f6f-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="18f6f-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="18f6f-119">Notes</span></span> <br/>          | <span data-ttu-id="18f6f-120">Unterstützte Behälter, die derzeit nicht installiert sind, sollten im printfunktionalitäten-Dokument als eingeschränkt gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="18f6f-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="18f6f-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="18f6f-121">Structural Content</span></span>

<span data-ttu-id="18f6f-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="18f6f-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="18f6f-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="18f6f-123">Structure Variables</span></span>

<span data-ttu-id="18f6f-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="18f6f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="18f6f-125">Name</span><span class="sxs-lookup"><span data-stu-id="18f6f-125">Name</span></span>                                   | <span data-ttu-id="18f6f-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="18f6f-126">Data type</span></span>          | <span data-ttu-id="18f6f-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="18f6f-127">Unit</span></span>                  | <span data-ttu-id="18f6f-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="18f6f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="18f6f-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="18f6f-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18f6f-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="18f6f-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-131">string</span></span><br/>  | <span data-ttu-id="18f6f-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="18f6f-132">characters</span></span><br/> | <span data-ttu-id="18f6f-133">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="18f6f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="18f6f-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="18f6f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="18f6f-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="18f6f-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="18f6f-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="18f6f-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-137">string</span></span><br/>  | <span data-ttu-id="18f6f-138">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-138">n/a</span></span><br/>        | <span data-ttu-id="18f6f-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="18f6f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="18f6f-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="18f6f-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="18f6f-141">\_Envelopeoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="18f6f-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-142">string</span></span><br/>  | <span data-ttu-id="18f6f-143">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-143">n/a</span></span><br/>        | <span data-ttu-id="18f6f-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="18f6f-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="18f6f-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="18f6f-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="18f6f-146">\_Bintypevalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="18f6f-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-147">string</span></span><br/>  | <span data-ttu-id="18f6f-148">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-148">n/a</span></span><br/>        | <span data-ttu-id="18f6f-149">Continuousfeed, Sheetfeed.</span><span class="sxs-lookup"><span data-stu-id="18f6f-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="18f6f-150">Gibt den Typ der bin an.</span><span class="sxs-lookup"><span data-stu-id="18f6f-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="18f6f-151">\_Feedtypevalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="18f6f-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-152">string</span></span><br/>  | <span data-ttu-id="18f6f-153">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-153">n/a</span></span><br/>        | <span data-ttu-id="18f6f-154">Automatisch, manuell.</span><span class="sxs-lookup"><span data-stu-id="18f6f-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="18f6f-155">Gibt den Feed-Mechanismus der bin an.</span><span class="sxs-lookup"><span data-stu-id="18f6f-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="18f6f-156">\_Mediacapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="18f6f-157">integer</span><span class="sxs-lookup"><span data-stu-id="18f6f-157">integer</span></span><br/> | <span data-ttu-id="18f6f-158">Glas</span><span class="sxs-lookup"><span data-stu-id="18f6f-158">sheets</span></span><br/>     | <span data-ttu-id="18f6f-159">Die maximale ganzzahlige Einschränkung ist vom Gerät zugelassen.</span><span class="sxs-lookup"><span data-stu-id="18f6f-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="18f6f-160">Gibt an, ob der bin ein hoher Kapazitäts-bin (qualitativ) ist.</span><span class="sxs-lookup"><span data-stu-id="18f6f-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="18f6f-161">\_Mediasizeautosenendvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="18f6f-162">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-162">string</span></span><br/>  | <span data-ttu-id="18f6f-163">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-163">n/a</span></span><br/>        | <span data-ttu-id="18f6f-164">Unterstützt, keine.</span><span class="sxs-lookup"><span data-stu-id="18f6f-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="18f6f-165">Gibt die Mediengröße für die automatische Sense-Funktion des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="18f6f-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="18f6f-166">\_Mediatypeer autosensvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="18f6f-167">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-167">string</span></span><br/>  | <span data-ttu-id="18f6f-168">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-168">n/a</span></span><br/>        | <span data-ttu-id="18f6f-169">Unterstützt, keine.</span><span class="sxs-lookup"><span data-stu-id="18f6f-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="18f6f-170">Gibt die Medien Kapazität in der Anzahl der Seiten (vollständig) des bin an.</span><span class="sxs-lookup"><span data-stu-id="18f6f-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="18f6f-171">\_Mediapathvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="18f6f-172">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-172">string</span></span><br/>  | <span data-ttu-id="18f6f-173">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-173">n/a</span></span><br/>        | <span data-ttu-id="18f6f-174">Direkt, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="18f6f-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="18f6f-175">Gibt die Merkmale des Medien Pfads an.</span><span class="sxs-lookup"><span data-stu-id="18f6f-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="18f6f-176">\_Feedwert\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="18f6f-177">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-177">string</span></span><br/>  | <span data-ttu-id="18f6f-178">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-178">n/a</span></span><br/>        | <span data-ttu-id="18f6f-179">FaceUp, Facedown</span><span class="sxs-lookup"><span data-stu-id="18f6f-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="18f6f-180">Gibt an, ob Medien gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="18f6f-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="18f6f-181">\_Feeddirectionvalue\_</span><span class="sxs-lookup"><span data-stu-id="18f6f-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="18f6f-182">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18f6f-182">string</span></span><br/>  | <span data-ttu-id="18f6f-183">–</span><span class="sxs-lookup"><span data-stu-id="18f6f-183">n/a</span></span><br/>        | <span data-ttu-id="18f6f-184">Longedgefirst, shortedgefirst</span><span class="sxs-lookup"><span data-stu-id="18f6f-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="18f6f-185">Gibt an, ob die Medien zuerst den langen Edge-oder kurzen Edge-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18f6f-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="18f6f-186">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="18f6f-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="18f6f-187">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="18f6f-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="18f6f-188">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="18f6f-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="18f6f-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18f6f-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18f6f-190">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="18f6f-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




