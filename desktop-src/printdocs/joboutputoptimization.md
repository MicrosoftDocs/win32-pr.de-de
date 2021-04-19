---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: Joboutputoptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d07bb98ea639753acc1b99b53d3785480a283a5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106363057"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="9fe84-104">Joboutputoptimization</span><span class="sxs-lookup"><span data-stu-id="9fe84-104">JobOutputOptimization</span></span>

<span data-ttu-id="9fe84-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9fe84-105">This topic is not current.</span></span> <span data-ttu-id="9fe84-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9fe84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9fe84-107">Beschreibt die Auftrags Verarbeitung, die zur Optimierung der Ausgabe für bestimmte Anwendungsszenarien vorgesehen ist, die durch die angegebene Option angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9fe84-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="9fe84-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9fe84-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9fe84-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9fe84-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9fe84-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9fe84-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9fe84-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9fe84-111">Element Information</span></span>



| <span data-ttu-id="9fe84-112">Name</span><span class="sxs-lookup"><span data-stu-id="9fe84-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9fe84-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9fe84-113">Element Type</span></span> <br/>   | <span data-ttu-id="9fe84-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="9fe84-114">Feature</span></span><br/> |
| <span data-ttu-id="9fe84-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="9fe84-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9fe84-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9fe84-116">Job</span></span><br/>     |
| <span data-ttu-id="9fe84-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fe84-117">Notes</span></span> <br/>          | <span data-ttu-id="9fe84-118">Keine</span><span class="sxs-lookup"><span data-stu-id="9fe84-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9fe84-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9fe84-119">Structural Content</span></span>

<span data-ttu-id="9fe84-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9fe84-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="9fe84-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9fe84-121">Structure Variables</span></span>

<span data-ttu-id="9fe84-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9fe84-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9fe84-123">Name</span><span class="sxs-lookup"><span data-stu-id="9fe84-123">Name</span></span>                               | <span data-ttu-id="9fe84-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9fe84-124">Data type</span></span>         | <span data-ttu-id="9fe84-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="9fe84-125">Unit</span></span>                  | <span data-ttu-id="9fe84-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9fe84-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9fe84-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9fe84-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9fe84-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="9fe84-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9fe84-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9fe84-129">string</span></span><br/> | <span data-ttu-id="9fe84-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9fe84-130">characters</span></span><br/> | <span data-ttu-id="9fe84-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe84-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9fe84-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9fe84-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9fe84-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9fe84-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9fe84-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9fe84-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9fe84-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9fe84-135">string</span></span><br/> | <span data-ttu-id="9fe84-136">–</span><span class="sxs-lookup"><span data-stu-id="9fe84-136">n/a</span></span><br/>        | <span data-ttu-id="9fe84-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9fe84-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9fe84-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe84-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9fe84-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9fe84-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9fe84-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe84-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9fe84-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9fe84-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="9fe84-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9fe84-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fe84-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9fe84-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




