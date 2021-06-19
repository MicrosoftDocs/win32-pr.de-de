---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageOutputQuality-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395588"
---
# <a name="pageoutputquality"></a><span data-ttu-id="822ac-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="822ac-105">PageOutputQuality</span></span>

<span data-ttu-id="822ac-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="822ac-106">This topic is not current.</span></span> <span data-ttu-id="822ac-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="822ac-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="822ac-108">Beschreibt den Qualitätsgrad der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="822ac-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="822ac-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="822ac-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="822ac-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="822ac-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="822ac-111">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="822ac-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="822ac-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="822ac-112">Element Information</span></span>



| <span data-ttu-id="822ac-113">Name</span><span class="sxs-lookup"><span data-stu-id="822ac-113">Name</span></span> | <span data-ttu-id="822ac-114">Wert</span><span class="sxs-lookup"><span data-stu-id="822ac-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="822ac-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="822ac-115">Element Type</span></span> <br/>   | <span data-ttu-id="822ac-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="822ac-116">Feature</span></span><br/> |
| <span data-ttu-id="822ac-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="822ac-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="822ac-118">Seite</span><span class="sxs-lookup"><span data-stu-id="822ac-118">Page</span></span><br/>    |
| <span data-ttu-id="822ac-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="822ac-119">Notes</span></span> <br/>          | <span data-ttu-id="822ac-120">Keine</span><span class="sxs-lookup"><span data-stu-id="822ac-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="822ac-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="822ac-121">Structural Content</span></span>

<span data-ttu-id="822ac-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="822ac-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="822ac-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="822ac-123">Structure Variables</span></span>

<span data-ttu-id="822ac-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="822ac-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="822ac-125">Name</span><span class="sxs-lookup"><span data-stu-id="822ac-125">Name</span></span>                               | <span data-ttu-id="822ac-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="822ac-126">Data type</span></span>         | <span data-ttu-id="822ac-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="822ac-127">Unit</span></span>                  | <span data-ttu-id="822ac-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="822ac-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="822ac-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="822ac-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="822ac-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="822ac-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="822ac-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="822ac-131">string</span></span><br/> | <span data-ttu-id="822ac-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="822ac-132">characters</span></span><br/> | <span data-ttu-id="822ac-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="822ac-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="822ac-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="822ac-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="822ac-135">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="822ac-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="822ac-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="822ac-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="822ac-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="822ac-137">string</span></span><br/> | <span data-ttu-id="822ac-138">–</span><span class="sxs-lookup"><span data-stu-id="822ac-138">n/a</span></span><br/>        | <span data-ttu-id="822ac-139">True, False</span><span class="sxs-lookup"><span data-stu-id="822ac-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="822ac-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="822ac-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="822ac-141">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="822ac-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="822ac-142">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="822ac-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="822ac-143">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="822ac-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="822ac-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="822ac-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="822ac-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="822ac-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




