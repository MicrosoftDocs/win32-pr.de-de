---
description: Erfahren Sie mehr über die JobOutputOptimization, die die Auftragsverarbeitung beschreibt, die die Ausgabe für bestimmte Verwendungsszenarien optimieren soll, wie durch die angegebene Option angegeben.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408793"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="3a144-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="3a144-103">JobOutputOptimization</span></span>

<span data-ttu-id="3a144-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3a144-104">This topic is not current.</span></span> <span data-ttu-id="3a144-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3a144-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a144-106">Beschreibt die Auftragsverarbeitung, die die Ausgabe für bestimmte Verwendungsszenarien optimieren soll, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="3a144-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="3a144-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a144-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a144-108">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a144-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3a144-109">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3a144-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3a144-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a144-110">Element Information</span></span>



| <span data-ttu-id="3a144-111">Name</span><span class="sxs-lookup"><span data-stu-id="3a144-111">Name</span></span> | <span data-ttu-id="3a144-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3a144-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3a144-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3a144-113">Element Type</span></span> <br/>   | <span data-ttu-id="3a144-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="3a144-114">Feature</span></span><br/> |
| <span data-ttu-id="3a144-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3a144-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a144-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3a144-116">Job</span></span><br/>     |
| <span data-ttu-id="3a144-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a144-117">Notes</span></span> <br/>          | <span data-ttu-id="3a144-118">Keine</span><span class="sxs-lookup"><span data-stu-id="3a144-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="3a144-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a144-119">Structural Content</span></span>

<span data-ttu-id="3a144-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="3a144-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3a144-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3a144-121">Structure Variables</span></span>

<span data-ttu-id="3a144-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3a144-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a144-123">Name</span><span class="sxs-lookup"><span data-stu-id="3a144-123">Name</span></span>                               | <span data-ttu-id="3a144-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3a144-124">Data type</span></span>         | <span data-ttu-id="3a144-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="3a144-125">Unit</span></span>                  | <span data-ttu-id="3a144-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3a144-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3a144-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3a144-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3a144-128">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3a144-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3a144-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a144-129">string</span></span><br/> | <span data-ttu-id="3a144-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3a144-130">characters</span></span><br/> | <span data-ttu-id="3a144-131">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="3a144-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3a144-132">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3a144-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3a144-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3a144-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3a144-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3a144-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3a144-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a144-135">string</span></span><br/> | <span data-ttu-id="3a144-136">–</span><span class="sxs-lookup"><span data-stu-id="3a144-136">n/a</span></span><br/>        | <span data-ttu-id="3a144-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3a144-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3a144-138">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3a144-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3a144-139">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3a144-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3a144-140">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="3a144-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3a144-141">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3a144-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3a144-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a144-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a144-143">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3a144-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




