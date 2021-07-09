---
description: Abrufen von Informationen zum vom Benutzer konfigurierbaren JobHolePunch-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549358"
---
# <a name="jobholepunch"></a><span data-ttu-id="edc88-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="edc88-105">JobHolePunch</span></span>

<span data-ttu-id="edc88-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="edc88-106">This topic is not current.</span></span> <span data-ttu-id="edc88-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="edc88-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="edc88-108">Beschreibt die Öffnungseigenschaften der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="edc88-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="edc88-109">Alle Dokumente werden zusammengeheftet.</span><span class="sxs-lookup"><span data-stu-id="edc88-109">All documents are punched together.</span></span> <span data-ttu-id="edc88-110">Die Schlüsselwörter JobHolePunch und DocumentHolePunch schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="edc88-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="edc88-111">Beide sollten nicht gleichzeitig in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edc88-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="edc88-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="edc88-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="edc88-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="edc88-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="edc88-114">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="edc88-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="edc88-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="edc88-115">Element Information</span></span>



| <span data-ttu-id="edc88-116">Name</span><span class="sxs-lookup"><span data-stu-id="edc88-116">Name</span></span> | <span data-ttu-id="edc88-117">Wert</span><span class="sxs-lookup"><span data-stu-id="edc88-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc88-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="edc88-118">Element Type</span></span> <br/>   | <span data-ttu-id="edc88-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="edc88-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="edc88-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="edc88-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="edc88-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="edc88-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="edc88-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edc88-122">Notes</span></span> <br/>          | <span data-ttu-id="edc88-123">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="edc88-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="edc88-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="edc88-124">Structural Content</span></span>

<span data-ttu-id="edc88-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="edc88-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="edc88-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="edc88-126">Structure Variables</span></span>

<span data-ttu-id="edc88-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="edc88-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="edc88-128">Name</span><span class="sxs-lookup"><span data-stu-id="edc88-128">Name</span></span>                               | <span data-ttu-id="edc88-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="edc88-129">Data type</span></span>         | <span data-ttu-id="edc88-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="edc88-130">Unit</span></span>                  | <span data-ttu-id="edc88-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="edc88-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="edc88-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="edc88-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="edc88-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="edc88-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="edc88-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="edc88-134">string</span></span><br/> | <span data-ttu-id="edc88-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="edc88-135">characters</span></span><br/> | <span data-ttu-id="edc88-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="edc88-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="edc88-137">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="edc88-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="edc88-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="edc88-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="edc88-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="edc88-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="edc88-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="edc88-140">string</span></span><br/> | <span data-ttu-id="edc88-141">n/v</span><span class="sxs-lookup"><span data-stu-id="edc88-141">n/a</span></span><br/>        | <span data-ttu-id="edc88-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="edc88-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="edc88-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="edc88-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="edc88-144">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="edc88-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="edc88-145">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="edc88-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="edc88-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="edc88-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="edc88-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="edc88-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edc88-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="edc88-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




