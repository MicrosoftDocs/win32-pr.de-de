---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76364aca1a9b6c8019a709c1cd0b7b1ad03020c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997747"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="a114b-104">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="a114b-104">JobOutputOptimization</span></span>

<span data-ttu-id="a114b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a114b-105">This topic is not current.</span></span> <span data-ttu-id="a114b-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a114b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a114b-107">Beschreibt die Auftragsverarbeitung, die die Ausgabe für bestimmte Verwendungsszenarien optimieren soll, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="a114b-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="a114b-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a114b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a114b-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a114b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a114b-110">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a114b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a114b-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a114b-111">Element Information</span></span>



| <span data-ttu-id="a114b-112">Name</span><span class="sxs-lookup"><span data-stu-id="a114b-112">Name</span></span> | <span data-ttu-id="a114b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a114b-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a114b-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a114b-114">Element Type</span></span> <br/>   | <span data-ttu-id="a114b-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="a114b-115">Feature</span></span><br/> |
| <span data-ttu-id="a114b-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a114b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a114b-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a114b-117">Job</span></span><br/>     |
| <span data-ttu-id="a114b-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a114b-118">Notes</span></span> <br/>          | <span data-ttu-id="a114b-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a114b-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a114b-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a114b-120">Structural Content</span></span>

<span data-ttu-id="a114b-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a114b-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a114b-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a114b-122">Structure Variables</span></span>

<span data-ttu-id="a114b-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a114b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a114b-124">Name</span><span class="sxs-lookup"><span data-stu-id="a114b-124">Name</span></span>                               | <span data-ttu-id="a114b-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a114b-125">Data type</span></span>         | <span data-ttu-id="a114b-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="a114b-126">Unit</span></span>                  | <span data-ttu-id="a114b-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a114b-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a114b-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a114b-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a114b-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a114b-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a114b-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a114b-130">string</span></span><br/> | <span data-ttu-id="a114b-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a114b-131">characters</span></span><br/> | <span data-ttu-id="a114b-132">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a114b-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a114b-133">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a114b-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a114b-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a114b-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a114b-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a114b-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a114b-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a114b-136">string</span></span><br/> | <span data-ttu-id="a114b-137">–</span><span class="sxs-lookup"><span data-stu-id="a114b-137">n/a</span></span><br/>        | <span data-ttu-id="a114b-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a114b-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a114b-139">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a114b-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a114b-140">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a114b-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a114b-141">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a114b-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a114b-142">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a114b-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a114b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a114b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a114b-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a114b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




