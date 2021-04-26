---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998287"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="ea277-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="ea277-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="ea277-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ea277-105">This topic is not current.</span></span> <span data-ttu-id="ea277-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ea277-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ea277-107">Beschreibt das Konfigurieren der digitalen Signaturverarbeitung für den gesamten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="ea277-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="ea277-108">Gilt nur für Inhalte, die digitale Signaturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ea277-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="ea277-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ea277-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ea277-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ea277-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="ea277-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ea277-111">Element Information</span></span>



| <span data-ttu-id="ea277-112">Name</span><span class="sxs-lookup"><span data-stu-id="ea277-112">Name</span></span> | <span data-ttu-id="ea277-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ea277-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ea277-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ea277-114">Element Type</span></span> <br/>   | <span data-ttu-id="ea277-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="ea277-115">Feature</span></span><br/> |
| <span data-ttu-id="ea277-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ea277-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ea277-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ea277-117">Job</span></span><br/>     |
| <span data-ttu-id="ea277-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea277-118">Notes</span></span> <br/>          | <span data-ttu-id="ea277-119">Keine</span><span class="sxs-lookup"><span data-stu-id="ea277-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ea277-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ea277-120">Structural Content</span></span>

<span data-ttu-id="ea277-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="ea277-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="ea277-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="ea277-122">Structure Variables</span></span>

<span data-ttu-id="ea277-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ea277-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ea277-124">Name</span><span class="sxs-lookup"><span data-stu-id="ea277-124">Name</span></span>                               | <span data-ttu-id="ea277-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ea277-125">Data type</span></span>         | <span data-ttu-id="ea277-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="ea277-126">Unit</span></span>                   | <span data-ttu-id="ea277-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="ea277-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ea277-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ea277-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ea277-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ea277-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ea277-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ea277-130">string</span></span><br/> | <span data-ttu-id="ea277-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="ea277-131">characters</span></span> <br/> | <span data-ttu-id="ea277-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ea277-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ea277-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="ea277-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ea277-134">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="ea277-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="ea277-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ea277-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ea277-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ea277-136">string</span></span><br/> | <span data-ttu-id="ea277-137">–</span><span class="sxs-lookup"><span data-stu-id="ea277-137">n/a</span></span><br/>         | <span data-ttu-id="ea277-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="ea277-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="ea277-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ea277-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ea277-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ea277-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ea277-141">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="ea277-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ea277-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="ea277-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ea277-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea277-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea277-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ea277-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




