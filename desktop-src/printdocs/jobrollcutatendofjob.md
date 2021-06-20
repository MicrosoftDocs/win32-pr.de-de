---
description: Erfahren Sie mehr über das JobRollCutAtEndOfJob-Element, das die Schneidmethode für Roll paper beschreibt. Das Roll sollte am Ende des Auftrags ausgeschnitten werden.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fdb973f3fda9fea28f64f0edb232910f2d2201
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408663"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="c0a47-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="c0a47-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="c0a47-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c0a47-105">This topic is not current.</span></span> <span data-ttu-id="c0a47-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c0a47-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c0a47-107">Beschreibt die Schneidmethode für Roll paper.</span><span class="sxs-lookup"><span data-stu-id="c0a47-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="c0a47-108">Das Roll sollte am Ende des Auftrags ausgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="c0a47-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="c0a47-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c0a47-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c0a47-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c0a47-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c0a47-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="c0a47-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c0a47-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c0a47-112">Element Information</span></span>



| <span data-ttu-id="c0a47-113">Name</span><span class="sxs-lookup"><span data-stu-id="c0a47-113">Name</span></span> | <span data-ttu-id="c0a47-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c0a47-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c0a47-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c0a47-115">Element Type</span></span> <br/>   | <span data-ttu-id="c0a47-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="c0a47-116">Feature</span></span><br/> |
| <span data-ttu-id="c0a47-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c0a47-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c0a47-118">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c0a47-118">Job</span></span><br/>     |
| <span data-ttu-id="c0a47-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0a47-119">Notes</span></span> <br/>          | <span data-ttu-id="c0a47-120">Keine</span><span class="sxs-lookup"><span data-stu-id="c0a47-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c0a47-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c0a47-121">Structural Content</span></span>

<span data-ttu-id="c0a47-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="c0a47-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
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

## <a name="structure-variables"></a><span data-ttu-id="c0a47-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c0a47-123">Structure Variables</span></span>

<span data-ttu-id="c0a47-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0a47-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c0a47-125">Name</span><span class="sxs-lookup"><span data-stu-id="c0a47-125">Name</span></span>                               | <span data-ttu-id="c0a47-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c0a47-126">Data type</span></span>         | <span data-ttu-id="c0a47-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="c0a47-127">Unit</span></span>                  | <span data-ttu-id="c0a47-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c0a47-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c0a47-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c0a47-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c0a47-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c0a47-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c0a47-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0a47-131">string</span></span><br/> | <span data-ttu-id="c0a47-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c0a47-132">characters</span></span><br/> | <span data-ttu-id="c0a47-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="c0a47-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c0a47-134">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c0a47-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c0a47-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c0a47-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c0a47-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c0a47-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c0a47-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0a47-137">string</span></span><br/> | <span data-ttu-id="c0a47-138">–</span><span class="sxs-lookup"><span data-stu-id="c0a47-138">n/a</span></span><br/>        | <span data-ttu-id="c0a47-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c0a47-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c0a47-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c0a47-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c0a47-141">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="c0a47-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c0a47-142">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="c0a47-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c0a47-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c0a47-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c0a47-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0a47-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a47-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c0a47-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




