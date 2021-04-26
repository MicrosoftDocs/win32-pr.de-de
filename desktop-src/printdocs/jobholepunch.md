---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56316c94dc56a2646446a8cd63885cceaa1407fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999297"
---
# <a name="jobholepunch"></a><span data-ttu-id="5f9e9-104">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="5f9e9-104">JobHolePunch</span></span>

<span data-ttu-id="5f9e9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-105">This topic is not current.</span></span> <span data-ttu-id="5f9e9-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5f9e9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f9e9-107">Beschreibt die Öffnungseigenschaften der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="5f9e9-108">Alle Dokumente werden zusammengeheftet.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-108">All documents are punched together.</span></span> <span data-ttu-id="5f9e9-109">Die Schlüsselwörter JobHolePunch und DocumentHolePunch schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="5f9e9-110">Beide sollten nicht gleichzeitig in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="5f9e9-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f9e9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f9e9-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="5f9e9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5f9e9-113">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="5f9e9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5f9e9-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f9e9-114">Element Information</span></span>



| <span data-ttu-id="5f9e9-115">Name</span><span class="sxs-lookup"><span data-stu-id="5f9e9-115">Name</span></span> | <span data-ttu-id="5f9e9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5f9e9-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9e9-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5f9e9-117">Element Type</span></span> <br/>   | <span data-ttu-id="5f9e9-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="5f9e9-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="5f9e9-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5f9e9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f9e9-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5f9e9-120">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="5f9e9-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f9e9-121">Notes</span></span> <br/>          | <span data-ttu-id="5f9e9-122">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5f9e9-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="5f9e9-123">Structural Content</span></span>

<span data-ttu-id="5f9e9-124">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5f9e9-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="5f9e9-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="5f9e9-125">Structure Variables</span></span>

<span data-ttu-id="5f9e9-126">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f9e9-127">Name</span><span class="sxs-lookup"><span data-stu-id="5f9e9-127">Name</span></span>                               | <span data-ttu-id="5f9e9-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5f9e9-128">Data type</span></span>         | <span data-ttu-id="5f9e9-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="5f9e9-129">Unit</span></span>                  | <span data-ttu-id="5f9e9-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="5f9e9-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5f9e9-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5f9e9-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5f9e9-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="5f9e9-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5f9e9-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f9e9-133">string</span></span><br/> | <span data-ttu-id="5f9e9-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5f9e9-134">characters</span></span><br/> | <span data-ttu-id="5f9e9-135">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5f9e9-136">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5f9e9-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5f9e9-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5f9e9-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5f9e9-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f9e9-139">string</span></span><br/> | <span data-ttu-id="5f9e9-140">–</span><span class="sxs-lookup"><span data-stu-id="5f9e9-140">n/a</span></span><br/>        | <span data-ttu-id="5f9e9-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="5f9e9-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5f9e9-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5f9e9-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5f9e9-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5f9e9-144">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="5f9e9-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5f9e9-145">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="5f9e9-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="5f9e9-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f9e9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f9e9-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5f9e9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




