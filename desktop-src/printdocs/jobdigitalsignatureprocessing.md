---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: Jobdigitalsignatureprocessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2c60fd005f42bd3f9861e86156a7da9164a81e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106365247"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="4899a-104">Jobdigitalsignatureprocessing</span><span class="sxs-lookup"><span data-stu-id="4899a-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="4899a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4899a-105">This topic is not current.</span></span> <span data-ttu-id="4899a-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4899a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4899a-107">Beschreibt die Konfiguration der digitalen Signatur Verarbeitung für den gesamten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4899a-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="4899a-108">Gilt nur für Inhalte, die digitale Signaturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="4899a-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="4899a-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4899a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4899a-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4899a-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="4899a-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4899a-111">Element Information</span></span>



| <span data-ttu-id="4899a-112">Name</span><span class="sxs-lookup"><span data-stu-id="4899a-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="4899a-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4899a-113">Element Type</span></span> <br/>   | <span data-ttu-id="4899a-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="4899a-114">Feature</span></span><br/> |
| <span data-ttu-id="4899a-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="4899a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4899a-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="4899a-116">Job</span></span><br/>     |
| <span data-ttu-id="4899a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4899a-117">Notes</span></span> <br/>          | <span data-ttu-id="4899a-118">Keine</span><span class="sxs-lookup"><span data-stu-id="4899a-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="4899a-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4899a-119">Structural Content</span></span>

<span data-ttu-id="4899a-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4899a-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4899a-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4899a-121">Structure Variables</span></span>

<span data-ttu-id="4899a-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4899a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4899a-123">Name</span><span class="sxs-lookup"><span data-stu-id="4899a-123">Name</span></span>                               | <span data-ttu-id="4899a-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4899a-124">Data type</span></span>         | <span data-ttu-id="4899a-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="4899a-125">Unit</span></span>                   | <span data-ttu-id="4899a-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4899a-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4899a-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4899a-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4899a-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="4899a-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4899a-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4899a-129">string</span></span><br/> | <span data-ttu-id="4899a-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4899a-130">characters</span></span> <br/> | <span data-ttu-id="4899a-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="4899a-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4899a-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4899a-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4899a-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4899a-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="4899a-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="4899a-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4899a-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4899a-135">string</span></span><br/> | <span data-ttu-id="4899a-136">–</span><span class="sxs-lookup"><span data-stu-id="4899a-136">n/a</span></span><br/>         | <span data-ttu-id="4899a-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4899a-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="4899a-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4899a-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4899a-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="4899a-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4899a-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="4899a-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4899a-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4899a-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4899a-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4899a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4899a-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="4899a-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




