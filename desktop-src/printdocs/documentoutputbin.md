---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: Documentoutputbin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444ca63fee0b76f17909b1aa08e65cd468537dee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219095"
---
# <a name="documentoutputbin"></a><span data-ttu-id="095b9-104">Documentoutputbin</span><span class="sxs-lookup"><span data-stu-id="095b9-104">DocumentOutputBin</span></span>

<span data-ttu-id="095b9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="095b9-105">This topic is not current.</span></span> <span data-ttu-id="095b9-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="095b9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="095b9-107">Beschreibt die vollständige Liste der unterstützten Container für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="095b9-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="095b9-108">Ermöglicht die Angabe des Ausgabe bin pro Dokument.</span><span class="sxs-lookup"><span data-stu-id="095b9-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="095b9-109">Die Schlüsselwörter "joboutputbin", "documentoutputbin" und "pageoutputbin" schließen sich gegenseitig aus. nur eine sollte in einem PrintTicket-oder Druck Funktions Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="095b9-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="095b9-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="095b9-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="095b9-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="095b9-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="095b9-112">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="095b9-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="095b9-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="095b9-113">Element Information</span></span>



| <span data-ttu-id="095b9-114">Name</span><span class="sxs-lookup"><span data-stu-id="095b9-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="095b9-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="095b9-115">Element Type</span></span> <br/>   | <span data-ttu-id="095b9-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="095b9-116">Feature</span></span><br/>  |
| <span data-ttu-id="095b9-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="095b9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="095b9-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="095b9-118">Document</span></span><br/> |
| <span data-ttu-id="095b9-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="095b9-119">Notes</span></span> <br/>          | <span data-ttu-id="095b9-120">Keine</span><span class="sxs-lookup"><span data-stu-id="095b9-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="095b9-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="095b9-121">Structural Content</span></span>

<span data-ttu-id="095b9-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="095b9-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="095b9-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="095b9-123">Structure Variables</span></span>

<span data-ttu-id="095b9-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="095b9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="095b9-125">Name</span><span class="sxs-lookup"><span data-stu-id="095b9-125">Name</span></span>                                   | <span data-ttu-id="095b9-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="095b9-126">Data type</span></span>          | <span data-ttu-id="095b9-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="095b9-127">Unit</span></span>                  | <span data-ttu-id="095b9-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="095b9-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="095b9-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="095b9-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="095b9-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="095b9-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="095b9-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="095b9-131">string</span></span><br/>  | <span data-ttu-id="095b9-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="095b9-132">characters</span></span><br/> | <span data-ttu-id="095b9-133">Gültiger voll qualifizierter Name, wie durch definiert https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="095b9-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="095b9-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="095b9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="095b9-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="095b9-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="095b9-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="095b9-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="095b9-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="095b9-137">string</span></span><br/>  | <span data-ttu-id="095b9-138">–</span><span class="sxs-lookup"><span data-stu-id="095b9-138">n/a</span></span><br/>        | <span data-ttu-id="095b9-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="095b9-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="095b9-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="095b9-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="095b9-141">\_Bintypevalue\_</span><span class="sxs-lookup"><span data-stu-id="095b9-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="095b9-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="095b9-142">string</span></span><br/>  | <span data-ttu-id="095b9-143">–</span><span class="sxs-lookup"><span data-stu-id="095b9-143">n/a</span></span><br/>        | <span data-ttu-id="095b9-144">Mailbox, Sorter, Stack, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="095b9-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="095b9-145">Gibt den allgemeinen Typ der bin an.</span><span class="sxs-lookup"><span data-stu-id="095b9-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="095b9-146">\_Mediasheetcapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="095b9-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="095b9-147">integer</span><span class="sxs-lookup"><span data-stu-id="095b9-147">integer</span></span><br/> | <span data-ttu-id="095b9-148">Glas</span><span class="sxs-lookup"><span data-stu-id="095b9-148">sheets</span></span><br/>     | <span data-ttu-id="095b9-149">Größer 0</span><span class="sxs-lookup"><span data-stu-id="095b9-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="095b9-150">Gibt die Medien Kapazität in der Anzahl der Seiten (vollständig) des bin an.</span><span class="sxs-lookup"><span data-stu-id="095b9-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="095b9-151">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="095b9-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="095b9-152">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="095b9-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="095b9-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="095b9-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="095b9-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="095b9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="095b9-155">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="095b9-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




