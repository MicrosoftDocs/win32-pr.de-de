---
description: Erfahren Sie mehr über das JobOutputBin-Element, das den installierten Ausgabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät beschreibt.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408853"
---
# <a name="joboutputbin"></a><span data-ttu-id="8d8e5-103">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="8d8e5-103">JobOutputBin</span></span>

<span data-ttu-id="8d8e5-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-104">This topic is not current.</span></span> <span data-ttu-id="8d8e5-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8d8e5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d8e5-106">Beschreibt den installierten Ausgabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="8d8e5-107">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="8d8e5-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8d8e5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8d8e5-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="8d8e5-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8d8e5-110">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="8d8e5-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8d8e5-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8d8e5-111">Element Information</span></span>



| <span data-ttu-id="8d8e5-112">Name</span><span class="sxs-lookup"><span data-stu-id="8d8e5-112">Name</span></span> | <span data-ttu-id="8d8e5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8d8e5-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8d8e5-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8d8e5-114">Element Type</span></span> <br/>   | <span data-ttu-id="8d8e5-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="8d8e5-115">Feature</span></span><br/> |
| <span data-ttu-id="8d8e5-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8d8e5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8d8e5-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8d8e5-117">Job</span></span><br/>     |
| <span data-ttu-id="8d8e5-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d8e5-118">Notes</span></span> <br/>          | <span data-ttu-id="8d8e5-119">Keine</span><span class="sxs-lookup"><span data-stu-id="8d8e5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="8d8e5-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="8d8e5-120">Structural Content</span></span>

<span data-ttu-id="8d8e5-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="8d8e5-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8d8e5-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8d8e5-122">Structure Variables</span></span>

<span data-ttu-id="8d8e5-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8d8e5-124">Name</span><span class="sxs-lookup"><span data-stu-id="8d8e5-124">Name</span></span>                                   | <span data-ttu-id="8d8e5-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8d8e5-125">Data type</span></span>          | <span data-ttu-id="8d8e5-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="8d8e5-126">Unit</span></span>                  | <span data-ttu-id="8d8e5-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8d8e5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8d8e5-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8d8e5-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8e5-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="8d8e5-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="8d8e5-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d8e5-130">string</span></span><br/>  | <span data-ttu-id="8d8e5-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8d8e5-131">characters</span></span><br/> | <span data-ttu-id="8d8e5-132">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8d8e5-133">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8d8e5-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="8d8e5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8d8e5-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="8d8e5-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d8e5-136">string</span></span><br/>  | <span data-ttu-id="8d8e5-137">–</span><span class="sxs-lookup"><span data-stu-id="8d8e5-137">n/a</span></span><br/>        | <span data-ttu-id="8d8e5-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="8d8e5-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8d8e5-139">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="8d8e5-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="8d8e5-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="8d8e5-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d8e5-141">string</span></span><br/>  | <span data-ttu-id="8d8e5-142">–</span><span class="sxs-lookup"><span data-stu-id="8d8e5-142">n/a</span></span><br/>        | <span data-ttu-id="8d8e5-143">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="8d8e5-144">Gibt den allgemeinen Typ des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="8d8e5-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="8d8e5-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="8d8e5-146">integer</span><span class="sxs-lookup"><span data-stu-id="8d8e5-146">integer</span></span><br/> | <span data-ttu-id="8d8e5-147">Blätter</span><span class="sxs-lookup"><span data-stu-id="8d8e5-147">sheets</span></span><br/>     | <span data-ttu-id="8d8e5-148">Maximal zulässige ganzzahlige Einschränkung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="8d8e5-149">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8d8e5-150">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="8d8e5-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8d8e5-151">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8d8e5-152">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8d8e5-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8d8e5-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d8e5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d8e5-154">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8d8e5-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




