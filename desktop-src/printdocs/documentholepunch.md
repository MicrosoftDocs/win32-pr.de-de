---
description: Erfahren Sie mehr über das DocumentHolePunch-Element, das die Lücke beschreibt, die die Eigenschaften der Ausgabe enthält.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409292"
---
# <a name="documentholepunch"></a><span data-ttu-id="c5920-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="c5920-103">DocumentHolePunch</span></span>

<span data-ttu-id="c5920-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c5920-104">This topic is not current.</span></span> <span data-ttu-id="c5920-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c5920-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5920-106">Beschreibt die Lücke der Eigenschaften der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c5920-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="c5920-107">Jedes Dokument wird separat geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5920-107">Each document is punched separately.</span></span> <span data-ttu-id="c5920-108">Die Schlüsselwörter JobHolePunch und DocumentHolePunch schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="c5920-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="c5920-109">Beides sollte nicht gleichzeitig in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5920-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="c5920-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c5920-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c5920-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c5920-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c5920-112">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c5920-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c5920-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c5920-113">Element Information</span></span>



| <span data-ttu-id="c5920-114">Name</span><span class="sxs-lookup"><span data-stu-id="c5920-114">Name</span></span> | <span data-ttu-id="c5920-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c5920-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c5920-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c5920-116">Element Type</span></span> <br/>   | <span data-ttu-id="c5920-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="c5920-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="c5920-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c5920-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c5920-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="c5920-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="c5920-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5920-120">Notes</span></span> <br/>          | <span data-ttu-id="c5920-121">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="c5920-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c5920-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c5920-122">Structural Content</span></span>

<span data-ttu-id="c5920-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="c5920-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="c5920-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c5920-124">Structure Variables</span></span>

<span data-ttu-id="c5920-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c5920-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c5920-126">Name</span><span class="sxs-lookup"><span data-stu-id="c5920-126">Name</span></span>                               | <span data-ttu-id="c5920-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c5920-127">Data type</span></span>         | <span data-ttu-id="c5920-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="c5920-128">Unit</span></span>                  | <span data-ttu-id="c5920-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c5920-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c5920-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c5920-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c5920-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c5920-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c5920-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5920-132">string</span></span><br/> | <span data-ttu-id="c5920-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c5920-133">characters</span></span><br/> | <span data-ttu-id="c5920-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c5920-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c5920-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c5920-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c5920-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c5920-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c5920-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c5920-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c5920-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5920-138">string</span></span><br/> | <span data-ttu-id="c5920-139">–</span><span class="sxs-lookup"><span data-stu-id="c5920-139">n/a</span></span><br/>        | <span data-ttu-id="c5920-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c5920-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c5920-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c5920-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c5920-142">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c5920-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c5920-143">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="c5920-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c5920-144">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c5920-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="c5920-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5920-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5920-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c5920-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




