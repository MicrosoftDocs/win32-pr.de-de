---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999217"
---
# <a name="joboutputbin"></a><span data-ttu-id="061e0-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="061e0-104">JobOutputBin</span></span>

<span data-ttu-id="061e0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="061e0-105">This topic is not current.</span></span> <span data-ttu-id="061e0-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="061e0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="061e0-107">Beschreibt den installierten Ausgabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="061e0-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="061e0-108">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="061e0-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="061e0-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="061e0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="061e0-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="061e0-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="061e0-111">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="061e0-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="061e0-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="061e0-112">Element Information</span></span>



| <span data-ttu-id="061e0-113">Name</span><span class="sxs-lookup"><span data-stu-id="061e0-113">Name</span></span> | <span data-ttu-id="061e0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="061e0-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="061e0-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="061e0-115">Element Type</span></span> <br/>   | <span data-ttu-id="061e0-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="061e0-116">Feature</span></span><br/> |
| <span data-ttu-id="061e0-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="061e0-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="061e0-118">Auftrag</span><span class="sxs-lookup"><span data-stu-id="061e0-118">Job</span></span><br/>     |
| <span data-ttu-id="061e0-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="061e0-119">Notes</span></span> <br/>          | <span data-ttu-id="061e0-120">Keine</span><span class="sxs-lookup"><span data-stu-id="061e0-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="061e0-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="061e0-121">Structural Content</span></span>

<span data-ttu-id="061e0-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="061e0-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="061e0-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="061e0-123">Structure Variables</span></span>

<span data-ttu-id="061e0-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="061e0-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="061e0-125">Name</span><span class="sxs-lookup"><span data-stu-id="061e0-125">Name</span></span>                                   | <span data-ttu-id="061e0-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="061e0-126">Data type</span></span>          | <span data-ttu-id="061e0-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="061e0-127">Unit</span></span>                  | <span data-ttu-id="061e0-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="061e0-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="061e0-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="061e0-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="061e0-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="061e0-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="061e0-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="061e0-131">string</span></span><br/>  | <span data-ttu-id="061e0-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="061e0-132">characters</span></span><br/> | <span data-ttu-id="061e0-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="061e0-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="061e0-134">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="061e0-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="061e0-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="061e0-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="061e0-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="061e0-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="061e0-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="061e0-137">string</span></span><br/>  | <span data-ttu-id="061e0-138">–</span><span class="sxs-lookup"><span data-stu-id="061e0-138">n/a</span></span><br/>        | <span data-ttu-id="061e0-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="061e0-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="061e0-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="061e0-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="061e0-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="061e0-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="061e0-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="061e0-142">string</span></span><br/>  | <span data-ttu-id="061e0-143">–</span><span class="sxs-lookup"><span data-stu-id="061e0-143">n/a</span></span><br/>        | <span data-ttu-id="061e0-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="061e0-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="061e0-145">Gibt den allgemeinen Typ des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="061e0-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="061e0-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="061e0-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="061e0-147">integer</span><span class="sxs-lookup"><span data-stu-id="061e0-147">integer</span></span><br/> | <span data-ttu-id="061e0-148">Blätter</span><span class="sxs-lookup"><span data-stu-id="061e0-148">sheets</span></span><br/>     | <span data-ttu-id="061e0-149">Maximale ganzzahlige Einschränkung, die vom Gerät zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="061e0-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="061e0-150">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="061e0-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="061e0-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="061e0-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="061e0-152">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="061e0-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="061e0-153">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="061e0-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="061e0-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="061e0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="061e0-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="061e0-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




