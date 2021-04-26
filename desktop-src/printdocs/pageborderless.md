---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20eb3379c76bfef3cd7ce6bb75dcf71479f0449
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997687"
---
# <a name="pageborderless"></a><span data-ttu-id="561c7-104">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="561c7-104">PageBorderless</span></span>

<span data-ttu-id="561c7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="561c7-105">This topic is not current.</span></span> <span data-ttu-id="561c7-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="561c7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="561c7-107">Beschreibt, wann Bildinhalte an den physischen Rändern des Mediums gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="561c7-107">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="561c7-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="561c7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="561c7-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="561c7-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="561c7-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="561c7-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="561c7-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="561c7-111">Element Information</span></span>



| <span data-ttu-id="561c7-112">Name</span><span class="sxs-lookup"><span data-stu-id="561c7-112">Name</span></span> | <span data-ttu-id="561c7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="561c7-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="561c7-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="561c7-114">Element Type</span></span> <br/>   | <span data-ttu-id="561c7-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="561c7-115">Feature</span></span><br/> |
| <span data-ttu-id="561c7-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="561c7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="561c7-117">Seite</span><span class="sxs-lookup"><span data-stu-id="561c7-117">Page</span></span><br/>    |
| <span data-ttu-id="561c7-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="561c7-118">Notes</span></span> <br/>          | <span data-ttu-id="561c7-119">Keine</span><span class="sxs-lookup"><span data-stu-id="561c7-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="561c7-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="561c7-120">Structural Content</span></span>

<span data-ttu-id="561c7-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="561c7-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="561c7-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="561c7-122">Structure Variables</span></span>

<span data-ttu-id="561c7-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="561c7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="561c7-124">Name</span><span class="sxs-lookup"><span data-stu-id="561c7-124">Name</span></span>                               | <span data-ttu-id="561c7-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="561c7-125">Data type</span></span>         | <span data-ttu-id="561c7-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="561c7-126">Unit</span></span>                  | <span data-ttu-id="561c7-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="561c7-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="561c7-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="561c7-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="561c7-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="561c7-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="561c7-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="561c7-130">string</span></span><br/> | <span data-ttu-id="561c7-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="561c7-131">characters</span></span><br/> | <span data-ttu-id="561c7-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="561c7-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="561c7-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="561c7-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="561c7-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="561c7-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="561c7-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="561c7-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="561c7-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="561c7-136">string</span></span><br/> | <span data-ttu-id="561c7-137">–</span><span class="sxs-lookup"><span data-stu-id="561c7-137">n/a</span></span><br/>        | <span data-ttu-id="561c7-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="561c7-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="561c7-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="561c7-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="561c7-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="561c7-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="561c7-141">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="561c7-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="561c7-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="561c7-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="561c7-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="561c7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="561c7-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="561c7-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




