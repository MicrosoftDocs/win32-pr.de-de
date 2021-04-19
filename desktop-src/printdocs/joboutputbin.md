---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: Joboutputbin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43fcf4aaf389769625e2289a438d7d5c2be0b83
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106366571"
---
# <a name="joboutputbin"></a><span data-ttu-id="300cb-104">Joboutputbin</span><span class="sxs-lookup"><span data-stu-id="300cb-104">JobOutputBin</span></span>

<span data-ttu-id="300cb-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="300cb-105">This topic is not current.</span></span> <span data-ttu-id="300cb-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="300cb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="300cb-107">Beschreibt den installierten Ausgabe Korb in einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="300cb-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="300cb-108">Die Schlüsselwörter "joboutputbin", "documentoutputbin" und "pageoutputbin" schließen sich gegenseitig aus. nur eine sollte in einem PrintTicket-oder Druck Funktions Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="300cb-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="300cb-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="300cb-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="300cb-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="300cb-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="300cb-111">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="300cb-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="300cb-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="300cb-112">Element Information</span></span>



| <span data-ttu-id="300cb-113">Name</span><span class="sxs-lookup"><span data-stu-id="300cb-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="300cb-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="300cb-114">Element Type</span></span> <br/>   | <span data-ttu-id="300cb-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="300cb-115">Feature</span></span><br/> |
| <span data-ttu-id="300cb-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="300cb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="300cb-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="300cb-117">Job</span></span><br/>     |
| <span data-ttu-id="300cb-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="300cb-118">Notes</span></span> <br/>          | <span data-ttu-id="300cb-119">Keine</span><span class="sxs-lookup"><span data-stu-id="300cb-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="300cb-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="300cb-120">Structural Content</span></span>

<span data-ttu-id="300cb-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="300cb-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="300cb-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="300cb-122">Structure Variables</span></span>

<span data-ttu-id="300cb-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="300cb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="300cb-124">Name</span><span class="sxs-lookup"><span data-stu-id="300cb-124">Name</span></span>                                   | <span data-ttu-id="300cb-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="300cb-125">Data type</span></span>          | <span data-ttu-id="300cb-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="300cb-126">Unit</span></span>                  | <span data-ttu-id="300cb-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="300cb-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="300cb-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="300cb-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="300cb-129">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="300cb-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="300cb-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="300cb-130">string</span></span><br/>  | <span data-ttu-id="300cb-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="300cb-131">characters</span></span><br/> | <span data-ttu-id="300cb-132">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="300cb-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="300cb-133">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="300cb-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="300cb-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="300cb-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="300cb-135">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="300cb-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="300cb-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="300cb-136">string</span></span><br/>  | <span data-ttu-id="300cb-137">–</span><span class="sxs-lookup"><span data-stu-id="300cb-137">n/a</span></span><br/>        | <span data-ttu-id="300cb-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="300cb-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="300cb-139">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="300cb-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="300cb-140">\_Bintypevalue\_</span><span class="sxs-lookup"><span data-stu-id="300cb-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="300cb-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="300cb-141">string</span></span><br/>  | <span data-ttu-id="300cb-142">–</span><span class="sxs-lookup"><span data-stu-id="300cb-142">n/a</span></span><br/>        | <span data-ttu-id="300cb-143">Mailbox, Sorter, Stack, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="300cb-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="300cb-144">Gibt den allgemeinen Typ der bin an.</span><span class="sxs-lookup"><span data-stu-id="300cb-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="300cb-145">\_Mediasheetcapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="300cb-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="300cb-146">integer</span><span class="sxs-lookup"><span data-stu-id="300cb-146">integer</span></span><br/> | <span data-ttu-id="300cb-147">Glas</span><span class="sxs-lookup"><span data-stu-id="300cb-147">sheets</span></span><br/>     | <span data-ttu-id="300cb-148">Die maximale ganzzahlige Einschränkung ist vom Gerät zugelassen.</span><span class="sxs-lookup"><span data-stu-id="300cb-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="300cb-149">Gibt die Medien Kapazität in der Anzahl der Seiten (vollständig) des bin an.</span><span class="sxs-lookup"><span data-stu-id="300cb-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="300cb-150">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="300cb-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="300cb-151">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="300cb-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="300cb-152">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="300cb-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="300cb-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="300cb-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="300cb-154">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="300cb-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




