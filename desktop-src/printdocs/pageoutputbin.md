---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557a742604f6e643e8812493049b7f2b118e262c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997527"
---
# <a name="pageoutputbin"></a><span data-ttu-id="c4e2c-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="c4e2c-104">PageOutputBin</span></span>

<span data-ttu-id="c4e2c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-105">This topic is not current.</span></span> <span data-ttu-id="c4e2c-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c4e2c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4e2c-107">Beschreibt die vollständige Liste der unterstützten Container für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="c4e2c-108">Ermöglicht die Angabe des Ausgabebehälters pro Seite.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="c4e2c-109">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="c4e2c-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c4e2c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4e2c-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c4e2c-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c4e2c-112">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="c4e2c-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c4e2c-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c4e2c-113">Element Information</span></span>



| <span data-ttu-id="c4e2c-114">Name</span><span class="sxs-lookup"><span data-stu-id="c4e2c-114">Name</span></span> | <span data-ttu-id="c4e2c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c4e2c-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c4e2c-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4e2c-116">Element Type</span></span> <br/>   | <span data-ttu-id="c4e2c-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="c4e2c-117">Feature</span></span><br/> |
| <span data-ttu-id="c4e2c-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c4e2c-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4e2c-119">Seite</span><span class="sxs-lookup"><span data-stu-id="c4e2c-119">Page</span></span><br/>    |
| <span data-ttu-id="c4e2c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4e2c-120">Notes</span></span> <br/>          | <span data-ttu-id="c4e2c-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c4e2c-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c4e2c-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c4e2c-122">Structural Content</span></span>

<span data-ttu-id="c4e2c-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="c4e2c-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c4e2c-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c4e2c-124">Structure Variables</span></span>

<span data-ttu-id="c4e2c-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4e2c-126">Name</span><span class="sxs-lookup"><span data-stu-id="c4e2c-126">Name</span></span>                                   | <span data-ttu-id="c4e2c-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c4e2c-127">Data type</span></span>          | <span data-ttu-id="c4e2c-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="c4e2c-128">Unit</span></span>                  | <span data-ttu-id="c4e2c-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c4e2c-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c4e2c-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c4e2c-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e2c-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c4e2c-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="c4e2c-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4e2c-132">string</span></span><br/>  | <span data-ttu-id="c4e2c-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c4e2c-133">characters</span></span><br/> | <span data-ttu-id="c4e2c-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c4e2c-135">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c4e2c-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="c4e2c-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c4e2c-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="c4e2c-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4e2c-138">string</span></span><br/>  | <span data-ttu-id="c4e2c-139">–</span><span class="sxs-lookup"><span data-stu-id="c4e2c-139">n/a</span></span><br/>        | <span data-ttu-id="c4e2c-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c4e2c-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c4e2c-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="c4e2c-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="c4e2c-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="c4e2c-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4e2c-143">string</span></span><br/>  | <span data-ttu-id="c4e2c-144">–</span><span class="sxs-lookup"><span data-stu-id="c4e2c-144">n/a</span></span><br/>        | <span data-ttu-id="c4e2c-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="c4e2c-146">Gibt den allgemeinen Typ des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="c4e2c-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="c4e2c-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="c4e2c-148">integer</span><span class="sxs-lookup"><span data-stu-id="c4e2c-148">integer</span></span><br/> | <span data-ttu-id="c4e2c-149">Blätter</span><span class="sxs-lookup"><span data-stu-id="c4e2c-149">sheets</span></span><br/>     | <span data-ttu-id="c4e2c-150">Größer 0</span><span class="sxs-lookup"><span data-stu-id="c4e2c-150">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="c4e2c-151">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c4e2c-152">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c4e2c-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c4e2c-153">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="c4e2c-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c4e2c-154">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c4e2c-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c4e2c-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4e2c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e2c-156">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c4e2c-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




