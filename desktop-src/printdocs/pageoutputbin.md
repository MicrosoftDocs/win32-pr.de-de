---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: Pageoutputbin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219112"
---
# <a name="pageoutputbin"></a><span data-ttu-id="9e20f-104">Pageoutputbin</span><span class="sxs-lookup"><span data-stu-id="9e20f-104">PageOutputBin</span></span>

<span data-ttu-id="9e20f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9e20f-105">This topic is not current.</span></span> <span data-ttu-id="9e20f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9e20f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9e20f-107">Beschreibt die vollständige Liste der unterstützten Container für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="9e20f-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="9e20f-108">Ermöglicht die Angabe des Ausgabe-bin pro Seite.</span><span class="sxs-lookup"><span data-stu-id="9e20f-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="9e20f-109">Die Schlüsselwörter "joboutputbin", "documentoutputbin" und "pageoutputbin" schließen sich gegenseitig aus. nur eine sollte in einem PrintTicket-oder Druck Funktions Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e20f-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9e20f-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9e20f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9e20f-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9e20f-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9e20f-112">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9e20f-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9e20f-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9e20f-113">Element Information</span></span>



| <span data-ttu-id="9e20f-114">Name</span><span class="sxs-lookup"><span data-stu-id="9e20f-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9e20f-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9e20f-115">Element Type</span></span> <br/>   | <span data-ttu-id="9e20f-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="9e20f-116">Feature</span></span><br/> |
| <span data-ttu-id="9e20f-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="9e20f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9e20f-118">Seite</span><span class="sxs-lookup"><span data-stu-id="9e20f-118">Page</span></span><br/>    |
| <span data-ttu-id="9e20f-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9e20f-119">Notes</span></span> <br/>          | <span data-ttu-id="9e20f-120">Keine</span><span class="sxs-lookup"><span data-stu-id="9e20f-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9e20f-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9e20f-121">Structural Content</span></span>

<span data-ttu-id="9e20f-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9e20f-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="9e20f-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9e20f-123">Structure Variables</span></span>

<span data-ttu-id="9e20f-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9e20f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9e20f-125">Name</span><span class="sxs-lookup"><span data-stu-id="9e20f-125">Name</span></span>                                   | <span data-ttu-id="9e20f-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9e20f-126">Data type</span></span>          | <span data-ttu-id="9e20f-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="9e20f-127">Unit</span></span>                  | <span data-ttu-id="9e20f-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9e20f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9e20f-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9e20f-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9e20f-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="9e20f-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9e20f-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9e20f-131">string</span></span><br/>  | <span data-ttu-id="9e20f-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9e20f-132">characters</span></span><br/> | <span data-ttu-id="9e20f-133">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9e20f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9e20f-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9e20f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9e20f-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9e20f-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="9e20f-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9e20f-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9e20f-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9e20f-137">string</span></span><br/>  | <span data-ttu-id="9e20f-138">–</span><span class="sxs-lookup"><span data-stu-id="9e20f-138">n/a</span></span><br/>        | <span data-ttu-id="9e20f-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9e20f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9e20f-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9e20f-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9e20f-141">\_Bintypevalue\_</span><span class="sxs-lookup"><span data-stu-id="9e20f-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="9e20f-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9e20f-142">string</span></span><br/>  | <span data-ttu-id="9e20f-143">–</span><span class="sxs-lookup"><span data-stu-id="9e20f-143">n/a</span></span><br/>        | <span data-ttu-id="9e20f-144">Facedowntray, faceuptray, Mailbox, Sorter, Stack, Finisher keine.</span><span class="sxs-lookup"><span data-stu-id="9e20f-144">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="9e20f-145">Gibt den allgemeinen Typ der bin an.</span><span class="sxs-lookup"><span data-stu-id="9e20f-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="9e20f-146">\_Mediasheetcapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="9e20f-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="9e20f-147">integer</span><span class="sxs-lookup"><span data-stu-id="9e20f-147">integer</span></span><br/> | <span data-ttu-id="9e20f-148">Glas</span><span class="sxs-lookup"><span data-stu-id="9e20f-148">sheets</span></span><br/>     | <span data-ttu-id="9e20f-149">Größer 0</span><span class="sxs-lookup"><span data-stu-id="9e20f-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="9e20f-150">Gibt die Medien Kapazität in der Anzahl der Seiten (vollständig) des bin an.</span><span class="sxs-lookup"><span data-stu-id="9e20f-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9e20f-151">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9e20f-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9e20f-152">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9e20f-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9e20f-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9e20f-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="9e20f-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e20f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e20f-155">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9e20f-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




