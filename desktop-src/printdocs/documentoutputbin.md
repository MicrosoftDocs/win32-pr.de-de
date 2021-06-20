---
description: Erfahren Sie mehr über DocumentOutputBin, das die vollständige Liste der unterstützten Container für das Gerät beschreibt und die Angabe des Ausgabebehälters pro Dokument ermöglicht.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409243"
---
# <a name="documentoutputbin"></a><span data-ttu-id="ce221-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="ce221-103">DocumentOutputBin</span></span>

<span data-ttu-id="ce221-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ce221-104">This topic is not current.</span></span> <span data-ttu-id="ce221-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ce221-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce221-106">Beschreibt die vollständige Liste der unterstützten Container für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="ce221-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="ce221-107">Ermöglicht die Angabe des Ausgabebehälters pro Dokument.</span><span class="sxs-lookup"><span data-stu-id="ce221-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="ce221-108">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce221-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="ce221-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce221-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="ce221-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="ce221-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="ce221-111">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="ce221-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce221-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce221-112">Element Information</span></span>



| <span data-ttu-id="ce221-113">Name</span><span class="sxs-lookup"><span data-stu-id="ce221-113">Name</span></span> | <span data-ttu-id="ce221-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ce221-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="ce221-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ce221-115">Element Type</span></span> <br/>   | <span data-ttu-id="ce221-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="ce221-116">Feature</span></span><br/>  |
| <span data-ttu-id="ce221-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ce221-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce221-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="ce221-118">Document</span></span><br/> |
| <span data-ttu-id="ce221-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce221-119">Notes</span></span> <br/>          | <span data-ttu-id="ce221-120">Keine</span><span class="sxs-lookup"><span data-stu-id="ce221-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ce221-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="ce221-121">Structural Content</span></span>

<span data-ttu-id="ce221-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="ce221-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ce221-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="ce221-123">Structure Variables</span></span>

<span data-ttu-id="ce221-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce221-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce221-125">Name</span><span class="sxs-lookup"><span data-stu-id="ce221-125">Name</span></span>                                   | <span data-ttu-id="ce221-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ce221-126">Data type</span></span>          | <span data-ttu-id="ce221-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="ce221-127">Unit</span></span>                  | <span data-ttu-id="ce221-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="ce221-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="ce221-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ce221-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce221-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ce221-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="ce221-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce221-131">string</span></span><br/>  | <span data-ttu-id="ce221-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="ce221-132">characters</span></span><br/> | <span data-ttu-id="ce221-133">Gültiger vollqualifizierte Name gemäß Definition von https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="ce221-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="ce221-134">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="ce221-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce221-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="ce221-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="ce221-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ce221-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="ce221-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce221-137">string</span></span><br/>  | <span data-ttu-id="ce221-138">–</span><span class="sxs-lookup"><span data-stu-id="ce221-138">n/a</span></span><br/>        | <span data-ttu-id="ce221-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="ce221-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="ce221-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ce221-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="ce221-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="ce221-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="ce221-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce221-142">string</span></span><br/>  | <span data-ttu-id="ce221-143">–</span><span class="sxs-lookup"><span data-stu-id="ce221-143">n/a</span></span><br/>        | <span data-ttu-id="ce221-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="ce221-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="ce221-145">Gibt den allgemeinen Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="ce221-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="ce221-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="ce221-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="ce221-147">integer</span><span class="sxs-lookup"><span data-stu-id="ce221-147">integer</span></span><br/> | <span data-ttu-id="ce221-148">Blätter</span><span class="sxs-lookup"><span data-stu-id="ce221-148">sheets</span></span><br/>     | <span data-ttu-id="ce221-149">Größer 0</span><span class="sxs-lookup"><span data-stu-id="ce221-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="ce221-150">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="ce221-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce221-151">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="ce221-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce221-152">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="ce221-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ce221-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="ce221-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ce221-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce221-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce221-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ce221-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




