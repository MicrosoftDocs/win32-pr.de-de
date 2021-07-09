---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageOutputBin-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548998"
---
# <a name="pageoutputbin"></a><span data-ttu-id="eac12-105">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="eac12-105">PageOutputBin</span></span>

<span data-ttu-id="eac12-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="eac12-106">This topic is not current.</span></span> <span data-ttu-id="eac12-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="eac12-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eac12-108">Beschreibt die vollständige Liste der unterstützten Behälter für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="eac12-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="eac12-109">Ermöglicht die Angabe des Ausgabebehälters pro Seite.</span><span class="sxs-lookup"><span data-stu-id="eac12-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="eac12-110">Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eac12-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="eac12-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eac12-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eac12-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="eac12-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eac12-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="eac12-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eac12-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eac12-114">Element Information</span></span>



| <span data-ttu-id="eac12-115">Name</span><span class="sxs-lookup"><span data-stu-id="eac12-115">Name</span></span> | <span data-ttu-id="eac12-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eac12-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="eac12-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="eac12-117">Element Type</span></span> <br/>   | <span data-ttu-id="eac12-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="eac12-118">Feature</span></span><br/> |
| <span data-ttu-id="eac12-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="eac12-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eac12-120">Seite</span><span class="sxs-lookup"><span data-stu-id="eac12-120">Page</span></span><br/>    |
| <span data-ttu-id="eac12-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eac12-121">Notes</span></span> <br/>          | <span data-ttu-id="eac12-122">Keine</span><span class="sxs-lookup"><span data-stu-id="eac12-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="eac12-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="eac12-123">Structural Content</span></span>

<span data-ttu-id="eac12-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="eac12-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="eac12-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="eac12-125">Structure Variables</span></span>

<span data-ttu-id="eac12-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="eac12-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eac12-127">Name</span><span class="sxs-lookup"><span data-stu-id="eac12-127">Name</span></span>                                   | <span data-ttu-id="eac12-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eac12-128">Data type</span></span>          | <span data-ttu-id="eac12-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="eac12-129">Unit</span></span>                  | <span data-ttu-id="eac12-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="eac12-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eac12-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eac12-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eac12-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="eac12-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="eac12-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eac12-133">string</span></span><br/>  | <span data-ttu-id="eac12-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="eac12-134">characters</span></span><br/> | <span data-ttu-id="eac12-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="eac12-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eac12-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="eac12-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eac12-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="eac12-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="eac12-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="eac12-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="eac12-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eac12-139">string</span></span><br/>  | <span data-ttu-id="eac12-140">n/v</span><span class="sxs-lookup"><span data-stu-id="eac12-140">n/a</span></span><br/>        | <span data-ttu-id="eac12-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="eac12-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="eac12-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="eac12-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="eac12-143">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="eac12-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="eac12-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eac12-144">string</span></span><br/>  | <span data-ttu-id="eac12-145">n/v</span><span class="sxs-lookup"><span data-stu-id="eac12-145">n/a</span></span><br/>        | <span data-ttu-id="eac12-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="eac12-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="eac12-147">Gibt den allgemeinen Typ des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="eac12-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="eac12-148">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="eac12-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="eac12-149">integer</span><span class="sxs-lookup"><span data-stu-id="eac12-149">integer</span></span><br/> | <span data-ttu-id="eac12-150">Blätter</span><span class="sxs-lookup"><span data-stu-id="eac12-150">sheets</span></span><br/>     | <span data-ttu-id="eac12-151">Größer 0</span><span class="sxs-lookup"><span data-stu-id="eac12-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="eac12-152">Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Bin-Werts an.</span><span class="sxs-lookup"><span data-stu-id="eac12-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eac12-153">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="eac12-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eac12-154">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="eac12-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eac12-155">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="eac12-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="eac12-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eac12-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac12-157">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="eac12-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




