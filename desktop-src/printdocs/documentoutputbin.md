---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997137"
---
# <a name="documentoutputbin"></a><span data-ttu-id="de327-104">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="de327-104">DocumentOutputBin</span></span>

<span data-ttu-id="de327-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="de327-105">This topic is not current.</span></span> <span data-ttu-id="de327-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="de327-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="de327-107">Beschreibt die vollständige Liste der unterstützten Behälter für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="de327-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="de327-108">Ermöglicht die Angabe des Ausgabebehälters pro Dokument.</span><span class="sxs-lookup"><span data-stu-id="de327-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="de327-109">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de327-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="de327-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="de327-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="de327-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="de327-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="de327-112">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="de327-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="de327-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="de327-113">Element Information</span></span>



| <span data-ttu-id="de327-114">Name</span><span class="sxs-lookup"><span data-stu-id="de327-114">Name</span></span> | <span data-ttu-id="de327-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de327-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="de327-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="de327-116">Element Type</span></span> <br/>   | <span data-ttu-id="de327-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="de327-117">Feature</span></span><br/>  |
| <span data-ttu-id="de327-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="de327-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="de327-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="de327-119">Document</span></span><br/> |
| <span data-ttu-id="de327-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de327-120">Notes</span></span> <br/>          | <span data-ttu-id="de327-121">Keine</span><span class="sxs-lookup"><span data-stu-id="de327-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="de327-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="de327-122">Structural Content</span></span>

<span data-ttu-id="de327-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="de327-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="de327-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="de327-124">Structure Variables</span></span>

<span data-ttu-id="de327-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="de327-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="de327-126">Name</span><span class="sxs-lookup"><span data-stu-id="de327-126">Name</span></span>                                   | <span data-ttu-id="de327-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de327-127">Data type</span></span>          | <span data-ttu-id="de327-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="de327-128">Unit</span></span>                  | <span data-ttu-id="de327-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="de327-129">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="de327-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="de327-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de327-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="de327-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="de327-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="de327-132">string</span></span><br/>  | <span data-ttu-id="de327-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="de327-133">characters</span></span><br/> | <span data-ttu-id="de327-134">Gültiger vollqualifizierter Name, wie durch https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname definiert.</span><span class="sxs-lookup"><span data-stu-id="de327-134">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="de327-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="de327-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="de327-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="de327-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="de327-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="de327-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="de327-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="de327-138">string</span></span><br/>  | <span data-ttu-id="de327-139">–</span><span class="sxs-lookup"><span data-stu-id="de327-139">n/a</span></span><br/>        | <span data-ttu-id="de327-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="de327-140">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="de327-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="de327-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="de327-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="de327-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="de327-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="de327-143">string</span></span><br/>  | <span data-ttu-id="de327-144">–</span><span class="sxs-lookup"><span data-stu-id="de327-144">n/a</span></span><br/>        | <span data-ttu-id="de327-145">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="de327-145">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="de327-146">Gibt den allgemeinen Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="de327-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="de327-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="de327-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="de327-148">integer</span><span class="sxs-lookup"><span data-stu-id="de327-148">integer</span></span><br/> | <span data-ttu-id="de327-149">Blätter</span><span class="sxs-lookup"><span data-stu-id="de327-149">sheets</span></span><br/>     | <span data-ttu-id="de327-150">Größer 0</span><span class="sxs-lookup"><span data-stu-id="de327-150">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="de327-151">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="de327-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="de327-152">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="de327-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="de327-153">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="de327-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="de327-154">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="de327-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="de327-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de327-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de327-156">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="de327-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




