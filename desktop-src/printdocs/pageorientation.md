---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997537"
---
# <a name="pageorientation"></a><span data-ttu-id="81684-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="81684-104">PageOrientation</span></span>

<span data-ttu-id="81684-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="81684-105">This topic is not current.</span></span> <span data-ttu-id="81684-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="81684-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="81684-107">Beschreibt die Ausrichtung des physischen Medienblatts.</span><span class="sxs-lookup"><span data-stu-id="81684-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="81684-108">Option</span><span class="sxs-lookup"><span data-stu-id="81684-108">Option</span></span>                       | <span data-ttu-id="81684-109">Definition</span><span class="sxs-lookup"><span data-stu-id="81684-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81684-110">Querformat</span><span class="sxs-lookup"><span data-stu-id="81684-110">Landscape</span></span> <br/>        | <span data-ttu-id="81684-111">Inhalt wird auf Seite 90 gedreht? Grad CCW relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="81684-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="81684-112">Hochformat</span><span class="sxs-lookup"><span data-stu-id="81684-112">Portrait</span></span> <br/>         | <span data-ttu-id="81684-113">Standardausrichtung.</span><span class="sxs-lookup"><span data-stu-id="81684-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="81684-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="81684-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="81684-115">Inhalt wird auf Seite 270 gedreht? Grad CCW relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="81684-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="81684-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="81684-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="81684-117">Inhalt wird auf Seite 180 gedreht? Grad relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="81684-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="81684-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="81684-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="81684-119">Strukturell</span><span class="sxs-lookup"><span data-stu-id="81684-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="81684-120">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="81684-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="81684-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="81684-121">Element Information</span></span>



| <span data-ttu-id="81684-122">Name</span><span class="sxs-lookup"><span data-stu-id="81684-122">Name</span></span> | <span data-ttu-id="81684-123">Wert</span><span class="sxs-lookup"><span data-stu-id="81684-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81684-124">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="81684-124">Element Type</span></span> <br/>   | <span data-ttu-id="81684-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="81684-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="81684-126">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="81684-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="81684-127">Seite</span><span class="sxs-lookup"><span data-stu-id="81684-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="81684-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81684-128">Notes</span></span> <br/>          | <span data-ttu-id="81684-129">Wenn ein Druckergerät nur eine Querformatrichtung unterstützen kann und diese Richtung als "Umgekehrte Querformat" bezeichnet wird, wird die Seitenausrichtung weiterhin als "Querformat" betrachtet.</span><span class="sxs-lookup"><span data-stu-id="81684-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="81684-130">Strukturell</span><span class="sxs-lookup"><span data-stu-id="81684-130">Structural Content</span></span>

<span data-ttu-id="81684-131">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="81684-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="81684-132">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="81684-132">Structure Variables</span></span>

<span data-ttu-id="81684-133">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="81684-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="81684-134">Name</span><span class="sxs-lookup"><span data-stu-id="81684-134">Name</span></span>                               | <span data-ttu-id="81684-135">Datentyp</span><span class="sxs-lookup"><span data-stu-id="81684-135">Data type</span></span>         | <span data-ttu-id="81684-136">Einheit</span><span class="sxs-lookup"><span data-stu-id="81684-136">Unit</span></span>                  | <span data-ttu-id="81684-137">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="81684-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="81684-138">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="81684-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="81684-139">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="81684-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="81684-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="81684-140">string</span></span><br/> | <span data-ttu-id="81684-141">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="81684-141">characters</span></span><br/> | <span data-ttu-id="81684-142">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="81684-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="81684-143">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="81684-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="81684-144">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="81684-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="81684-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="81684-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="81684-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="81684-146">string</span></span><br/> | <span data-ttu-id="81684-147">–</span><span class="sxs-lookup"><span data-stu-id="81684-147">n/a</span></span><br/>        | <span data-ttu-id="81684-148">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="81684-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="81684-149">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="81684-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="81684-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="81684-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="81684-151">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="81684-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="81684-152">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="81684-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="81684-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81684-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81684-154">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="81684-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




