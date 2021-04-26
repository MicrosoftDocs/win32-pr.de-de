---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d4bfb09a1c3f6f43f11886685a0edfcf2bbd92
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997047"
---
# <a name="documentrollcut"></a><span data-ttu-id="5e79d-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="5e79d-104">DocumentRollCut</span></span>

<span data-ttu-id="5e79d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5e79d-105">This topic is not current.</span></span> <span data-ttu-id="5e79d-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5e79d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5e79d-107">Beschreibt die Schneidmethode für Roll paper.</span><span class="sxs-lookup"><span data-stu-id="5e79d-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="5e79d-108">Jedes Dokument wird separat behandelt.</span><span class="sxs-lookup"><span data-stu-id="5e79d-108">Each document is handled separately.</span></span> <span data-ttu-id="5e79d-109">Die angegebenen Optionen beschreiben die verschiedenen Methoden für roll cut.</span><span class="sxs-lookup"><span data-stu-id="5e79d-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="5e79d-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5e79d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5e79d-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5e79d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5e79d-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5e79d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5e79d-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5e79d-113">Element Information</span></span>



| <span data-ttu-id="5e79d-114">Name</span><span class="sxs-lookup"><span data-stu-id="5e79d-114">Name</span></span> | <span data-ttu-id="5e79d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5e79d-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="5e79d-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5e79d-116">Element Type</span></span> <br/>   | <span data-ttu-id="5e79d-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="5e79d-117">Feature</span></span><br/>  |
| <span data-ttu-id="5e79d-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5e79d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5e79d-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="5e79d-119">Document</span></span><br/> |
| <span data-ttu-id="5e79d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e79d-120">Notes</span></span> <br/>          | <span data-ttu-id="5e79d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="5e79d-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="5e79d-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5e79d-122">Structural Content</span></span>

<span data-ttu-id="5e79d-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="5e79d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="5e79d-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="5e79d-124">Structure Variables</span></span>

<span data-ttu-id="5e79d-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5e79d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5e79d-126">Name</span><span class="sxs-lookup"><span data-stu-id="5e79d-126">Name</span></span>                               | <span data-ttu-id="5e79d-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5e79d-127">Data type</span></span>         | <span data-ttu-id="5e79d-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="5e79d-128">Unit</span></span>                  | <span data-ttu-id="5e79d-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="5e79d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5e79d-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5e79d-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5e79d-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="5e79d-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5e79d-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5e79d-132">string</span></span><br/> | <span data-ttu-id="5e79d-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5e79d-133">characters</span></span><br/> | <span data-ttu-id="5e79d-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5e79d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5e79d-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="5e79d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5e79d-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="5e79d-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5e79d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5e79d-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5e79d-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5e79d-138">string</span></span><br/> | <span data-ttu-id="5e79d-139">–</span><span class="sxs-lookup"><span data-stu-id="5e79d-139">n/a</span></span><br/>        | <span data-ttu-id="5e79d-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="5e79d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5e79d-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5e79d-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5e79d-142">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="5e79d-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5e79d-143">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="5e79d-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5e79d-144">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="5e79d-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="5e79d-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e79d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e79d-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5e79d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




