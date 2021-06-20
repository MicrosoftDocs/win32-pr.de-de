---
description: Erfahren Sie mehr über das DocumentRollCut-Element, das die Schneidmethode für Roll paper beschreibt. Jedes Dokument wird separat behandelt.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f7232cbe9dafce25aa2ee482ca40bf99145841
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409183"
---
# <a name="documentrollcut"></a><span data-ttu-id="8caaf-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="8caaf-104">DocumentRollCut</span></span>

<span data-ttu-id="8caaf-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8caaf-105">This topic is not current.</span></span> <span data-ttu-id="8caaf-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8caaf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8caaf-107">Beschreibt die Schneidmethode für Roll paper.</span><span class="sxs-lookup"><span data-stu-id="8caaf-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="8caaf-108">Jedes Dokument wird separat behandelt.</span><span class="sxs-lookup"><span data-stu-id="8caaf-108">Each document is handled separately.</span></span> <span data-ttu-id="8caaf-109">Die angegebenen Optionen beschreiben die verschiedenen Methoden für roll cut.</span><span class="sxs-lookup"><span data-stu-id="8caaf-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="8caaf-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8caaf-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8caaf-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8caaf-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8caaf-112">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="8caaf-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8caaf-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8caaf-113">Element Information</span></span>



| <span data-ttu-id="8caaf-114">Name</span><span class="sxs-lookup"><span data-stu-id="8caaf-114">Name</span></span> | <span data-ttu-id="8caaf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8caaf-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="8caaf-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8caaf-116">Element Type</span></span> <br/>   | <span data-ttu-id="8caaf-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="8caaf-117">Feature</span></span><br/>  |
| <span data-ttu-id="8caaf-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8caaf-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8caaf-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="8caaf-119">Document</span></span><br/> |
| <span data-ttu-id="8caaf-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8caaf-120">Notes</span></span> <br/>          | <span data-ttu-id="8caaf-121">Keine</span><span class="sxs-lookup"><span data-stu-id="8caaf-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8caaf-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8caaf-122">Structural Content</span></span>

<span data-ttu-id="8caaf-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="8caaf-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8caaf-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8caaf-124">Structure Variables</span></span>

<span data-ttu-id="8caaf-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8caaf-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8caaf-126">Name</span><span class="sxs-lookup"><span data-stu-id="8caaf-126">Name</span></span>                               | <span data-ttu-id="8caaf-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8caaf-127">Data type</span></span>         | <span data-ttu-id="8caaf-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="8caaf-128">Unit</span></span>                  | <span data-ttu-id="8caaf-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8caaf-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8caaf-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8caaf-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8caaf-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="8caaf-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8caaf-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8caaf-132">string</span></span><br/> | <span data-ttu-id="8caaf-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8caaf-133">characters</span></span><br/> | <span data-ttu-id="8caaf-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8caaf-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8caaf-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8caaf-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8caaf-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="8caaf-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8caaf-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8caaf-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8caaf-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8caaf-138">string</span></span><br/> | <span data-ttu-id="8caaf-139">–</span><span class="sxs-lookup"><span data-stu-id="8caaf-139">n/a</span></span><br/>        | <span data-ttu-id="8caaf-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="8caaf-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8caaf-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8caaf-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8caaf-142">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="8caaf-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8caaf-143">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="8caaf-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8caaf-144">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8caaf-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8caaf-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8caaf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8caaf-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8caaf-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




