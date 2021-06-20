---
description: Erfahren Sie mehr über das DocumentInputBin-Element, das den installierten Eingabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät beschreibt.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452e2f94b3e75a2b0555610db26d69e2a2f7548b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409303"
---
# <a name="documentinputbin"></a><span data-ttu-id="bbda5-103">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="bbda5-103">DocumentInputBin</span></span>

<span data-ttu-id="bbda5-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="bbda5-104">This topic is not current.</span></span> <span data-ttu-id="bbda5-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="bbda5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbda5-106">Beschreibt den installierten Eingabebehälter in einem Gerät oder die vollständige Liste der unterstützten Behälter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="bbda5-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="bbda5-107">Die Schlüsselwörter JobInputBin, DocumentInputBin und PageInputBin schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="bbda5-107">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="bbda5-108">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bbda5-108">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="bbda5-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bbda5-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="bbda5-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bbda5-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="bbda5-111">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="bbda5-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bbda5-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bbda5-112">Element Information</span></span>



| <span data-ttu-id="bbda5-113">Name</span><span class="sxs-lookup"><span data-stu-id="bbda5-113">Name</span></span> | <span data-ttu-id="bbda5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bbda5-114">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbda5-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="bbda5-115">Element Type</span></span> <br/>   | <span data-ttu-id="bbda5-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="bbda5-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="bbda5-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="bbda5-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bbda5-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="bbda5-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="bbda5-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbda5-119">Notes</span></span> <br/>          | <span data-ttu-id="bbda5-120">Unterstützte, derzeit nicht installierte Bins sollten im PrintCapabilities-Dokument als eingeschränkt gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bbda5-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bbda5-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bbda5-121">Structural Content</span></span>

<span data-ttu-id="bbda5-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="bbda5-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="bbda5-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="bbda5-123">Structure Variables</span></span>

<span data-ttu-id="bbda5-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbda5-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bbda5-125">Name</span><span class="sxs-lookup"><span data-stu-id="bbda5-125">Name</span></span>                                   | <span data-ttu-id="bbda5-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bbda5-126">Data type</span></span>          | <span data-ttu-id="bbda5-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="bbda5-127">Unit</span></span>                  | <span data-ttu-id="bbda5-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="bbda5-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bbda5-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bbda5-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bbda5-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="bbda5-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-131">string</span></span><br/>  | <span data-ttu-id="bbda5-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="bbda5-132">characters</span></span><br/> | <span data-ttu-id="bbda5-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bbda5-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bbda5-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="bbda5-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bbda5-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="bbda5-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="bbda5-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="bbda5-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-137">string</span></span><br/>  | <span data-ttu-id="bbda5-138">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-138">n/a</span></span><br/>        | <span data-ttu-id="bbda5-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="bbda5-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bbda5-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bbda5-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="bbda5-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="bbda5-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-142">string</span></span><br/>  | <span data-ttu-id="bbda5-143">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-143">n/a</span></span><br/>        | <span data-ttu-id="bbda5-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="bbda5-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bbda5-145">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bbda5-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="bbda5-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="bbda5-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-147">string</span></span><br/>  | <span data-ttu-id="bbda5-148">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-148">n/a</span></span><br/>        | <span data-ttu-id="bbda5-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="bbda5-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="bbda5-150">Gibt den Typ des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="bbda5-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="bbda5-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="bbda5-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-152">string</span></span><br/>  | <span data-ttu-id="bbda5-153">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-153">n/a</span></span><br/>        | <span data-ttu-id="bbda5-154">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="bbda5-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="bbda5-155">Gibt den Feedmechanismus des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="bbda5-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="bbda5-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="bbda5-157">integer</span><span class="sxs-lookup"><span data-stu-id="bbda5-157">integer</span></span><br/> | <span data-ttu-id="bbda5-158">Blätter</span><span class="sxs-lookup"><span data-stu-id="bbda5-158">sheets</span></span><br/>     | <span data-ttu-id="bbda5-159">Maximale ganzzahlige Einschränkung, die vom Gerät zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="bbda5-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="bbda5-160">Gibt an, ob es sich bei der Behälter um einen Hochkapazitätsbehälter (qualitativ) handelt.</span><span class="sxs-lookup"><span data-stu-id="bbda5-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="bbda5-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="bbda5-162">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-162">string</span></span><br/>  | <span data-ttu-id="bbda5-163">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-163">n/a</span></span><br/>        | <span data-ttu-id="bbda5-164">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="bbda5-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bbda5-165">Gibt die Funktion der automatischen Mediengröße für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="bbda5-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="bbda5-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="bbda5-167">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-167">string</span></span><br/>  | <span data-ttu-id="bbda5-168">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-168">n/a</span></span><br/>        | <span data-ttu-id="bbda5-169">Unterstützt, Keine.</span><span class="sxs-lookup"><span data-stu-id="bbda5-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bbda5-170">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="bbda5-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="bbda5-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="bbda5-172">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-172">string</span></span><br/>  | <span data-ttu-id="bbda5-173">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-173">n/a</span></span><br/>        | <span data-ttu-id="bbda5-174">Gerade, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="bbda5-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="bbda5-175">Gibt die Merkmale des Medienpfads an.</span><span class="sxs-lookup"><span data-stu-id="bbda5-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="bbda5-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="bbda5-177">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-177">string</span></span><br/>  | <span data-ttu-id="bbda5-178">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-178">n/a</span></span><br/>        | <span data-ttu-id="bbda5-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="bbda5-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bbda5-180">Gibt an, ob Medien nach oben oder nach unten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bbda5-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="bbda5-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="bbda5-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="bbda5-182">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbda5-182">string</span></span><br/>  | <span data-ttu-id="bbda5-183">–</span><span class="sxs-lookup"><span data-stu-id="bbda5-183">n/a</span></span><br/>        | <span data-ttu-id="bbda5-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="bbda5-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="bbda5-185">Gibt an, ob medien zuerst lange Kanten oder kurze Kanten gespeist werden.</span><span class="sxs-lookup"><span data-stu-id="bbda5-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bbda5-186">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bbda5-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bbda5-187">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="bbda5-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bbda5-188">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="bbda5-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bbda5-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbda5-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbda5-190">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="bbda5-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




