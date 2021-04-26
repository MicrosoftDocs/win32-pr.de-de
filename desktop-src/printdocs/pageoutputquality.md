---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c63238c290d6b8f0bb208e94e52dc66c8d2e6be
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994477"
---
# <a name="pageoutputquality"></a><span data-ttu-id="550e4-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="550e4-104">PageOutputQuality</span></span>

<span data-ttu-id="550e4-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="550e4-105">This topic is not current.</span></span> <span data-ttu-id="550e4-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="550e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="550e4-107">Beschreibt die Qualitätsstufe der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="550e4-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="550e4-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="550e4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="550e4-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="550e4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="550e4-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="550e4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="550e4-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="550e4-111">Element Information</span></span>



| <span data-ttu-id="550e4-112">Name</span><span class="sxs-lookup"><span data-stu-id="550e4-112">Name</span></span> | <span data-ttu-id="550e4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="550e4-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="550e4-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="550e4-114">Element Type</span></span> <br/>   | <span data-ttu-id="550e4-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="550e4-115">Feature</span></span><br/> |
| <span data-ttu-id="550e4-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="550e4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="550e4-117">Seite</span><span class="sxs-lookup"><span data-stu-id="550e4-117">Page</span></span><br/>    |
| <span data-ttu-id="550e4-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="550e4-118">Notes</span></span> <br/>          | <span data-ttu-id="550e4-119">Keine</span><span class="sxs-lookup"><span data-stu-id="550e4-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="550e4-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="550e4-120">Structural Content</span></span>

<span data-ttu-id="550e4-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="550e4-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="550e4-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="550e4-122">Structure Variables</span></span>

<span data-ttu-id="550e4-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="550e4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="550e4-124">Name</span><span class="sxs-lookup"><span data-stu-id="550e4-124">Name</span></span>                               | <span data-ttu-id="550e4-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="550e4-125">Data type</span></span>         | <span data-ttu-id="550e4-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="550e4-126">Unit</span></span>                  | <span data-ttu-id="550e4-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="550e4-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="550e4-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="550e4-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="550e4-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="550e4-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="550e4-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="550e4-130">string</span></span><br/> | <span data-ttu-id="550e4-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="550e4-131">characters</span></span><br/> | <span data-ttu-id="550e4-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="550e4-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="550e4-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="550e4-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="550e4-134">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="550e4-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="550e4-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="550e4-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="550e4-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="550e4-136">string</span></span><br/> | <span data-ttu-id="550e4-137">–</span><span class="sxs-lookup"><span data-stu-id="550e4-137">n/a</span></span><br/>        | <span data-ttu-id="550e4-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="550e4-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="550e4-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="550e4-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="550e4-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="550e4-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="550e4-141">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="550e4-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="550e4-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="550e4-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="550e4-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="550e4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="550e4-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="550e4-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




