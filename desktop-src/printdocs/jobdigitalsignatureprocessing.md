---
description: Erfahren Sie mehr über das JobDigitalSignatureProcessing-Element, das das Konfigurieren der Verarbeitung digitaler Signaturen für den gesamten Auftrag beschreibt.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9491a921d9d733dd0de0a4e5133d5c6690b2b4a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408943"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="60288-103">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="60288-103">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="60288-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="60288-104">This topic is not current.</span></span> <span data-ttu-id="60288-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="60288-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60288-106">Beschreibt das Konfigurieren der Digitalen Signaturverarbeitung für den gesamten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="60288-106">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="60288-107">Gilt nur für Inhalte, die digitale Signaturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="60288-107">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="60288-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="60288-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60288-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="60288-109">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="60288-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="60288-110">Element Information</span></span>



| <span data-ttu-id="60288-111">Name</span><span class="sxs-lookup"><span data-stu-id="60288-111">Name</span></span> | <span data-ttu-id="60288-112">Wert</span><span class="sxs-lookup"><span data-stu-id="60288-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="60288-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="60288-113">Element Type</span></span> <br/>   | <span data-ttu-id="60288-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="60288-114">Feature</span></span><br/> |
| <span data-ttu-id="60288-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="60288-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60288-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="60288-116">Job</span></span><br/>     |
| <span data-ttu-id="60288-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60288-117">Notes</span></span> <br/>          | <span data-ttu-id="60288-118">Keine</span><span class="sxs-lookup"><span data-stu-id="60288-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="60288-119">Strukturell</span><span class="sxs-lookup"><span data-stu-id="60288-119">Structural Content</span></span>

<span data-ttu-id="60288-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="60288-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="60288-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="60288-121">Structure Variables</span></span>

<span data-ttu-id="60288-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="60288-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60288-123">Name</span><span class="sxs-lookup"><span data-stu-id="60288-123">Name</span></span>                               | <span data-ttu-id="60288-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="60288-124">Data type</span></span>         | <span data-ttu-id="60288-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="60288-125">Unit</span></span>                   | <span data-ttu-id="60288-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="60288-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="60288-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="60288-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="60288-128">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="60288-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="60288-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60288-129">string</span></span><br/> | <span data-ttu-id="60288-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="60288-130">characters</span></span> <br/> | <span data-ttu-id="60288-131">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="60288-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="60288-132">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="60288-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="60288-133">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="60288-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="60288-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="60288-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="60288-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60288-135">string</span></span><br/> | <span data-ttu-id="60288-136">–</span><span class="sxs-lookup"><span data-stu-id="60288-136">n/a</span></span><br/>         | <span data-ttu-id="60288-137">True, False</span><span class="sxs-lookup"><span data-stu-id="60288-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="60288-138">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="60288-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="60288-139">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="60288-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="60288-140">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="60288-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="60288-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="60288-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="60288-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60288-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60288-143">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="60288-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




