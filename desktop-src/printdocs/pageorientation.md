---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f004329c217d4aab6ddc3c1d166037e7c7b5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393902"
---
# <a name="pageorientation"></a><span data-ttu-id="244d5-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="244d5-104">PageOrientation</span></span>

<span data-ttu-id="244d5-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="244d5-105">This topic is not current.</span></span> <span data-ttu-id="244d5-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="244d5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="244d5-107">Beschreibt die Ausrichtung des physischen Medien Blatts.</span><span class="sxs-lookup"><span data-stu-id="244d5-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="244d5-108">Option</span><span class="sxs-lookup"><span data-stu-id="244d5-108">Option</span></span>                       | <span data-ttu-id="244d5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="244d5-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244d5-110">Querformat</span><span class="sxs-lookup"><span data-stu-id="244d5-110">Landscape</span></span> <br/>        | <span data-ttu-id="244d5-111">Der Inhalt wird auf der Seite 90 gedreht? Grad CCW relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="244d5-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="244d5-112">Hochformat</span><span class="sxs-lookup"><span data-stu-id="244d5-112">Portrait</span></span> <br/>         | <span data-ttu-id="244d5-113">Standard Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="244d5-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="244d5-114">Reverselandscape</span><span class="sxs-lookup"><span data-stu-id="244d5-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="244d5-115">Der Inhalt wird auf der Seite 270 gedreht? Grad CCW relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="244d5-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="244d5-116">Reverum Hochformat</span><span class="sxs-lookup"><span data-stu-id="244d5-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="244d5-117">Der Inhalt wird auf der Seite 180 gedreht? Grad relativ zur Standardausrichtung (Hochformat).</span><span class="sxs-lookup"><span data-stu-id="244d5-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="244d5-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="244d5-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="244d5-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="244d5-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="244d5-120">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="244d5-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="244d5-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="244d5-121">Element Information</span></span>



| <span data-ttu-id="244d5-122">Name</span><span class="sxs-lookup"><span data-stu-id="244d5-122">Name</span></span>                       |                                                                                                                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244d5-123">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="244d5-123">Element Type</span></span> <br/>   | <span data-ttu-id="244d5-124">Funktion</span><span class="sxs-lookup"><span data-stu-id="244d5-124">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="244d5-125">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="244d5-125">Scoping Prefix</span></span> <br/> | <span data-ttu-id="244d5-126">Seite</span><span class="sxs-lookup"><span data-stu-id="244d5-126">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="244d5-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="244d5-127">Notes</span></span> <br/>          | <span data-ttu-id="244d5-128">Wenn ein Druckergerät nur eine Querrichtung unterstützen kann und diese Richtung als "umgekehrte Querformat" bezeichnet wird, wird die Seitenausrichtung weiterhin als "Landscape" betrachtet.</span><span class="sxs-lookup"><span data-stu-id="244d5-128">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="244d5-129">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="244d5-129">Structural Content</span></span>

<span data-ttu-id="244d5-130">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="244d5-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="244d5-131">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="244d5-131">Structure Variables</span></span>

<span data-ttu-id="244d5-132">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="244d5-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="244d5-133">Name</span><span class="sxs-lookup"><span data-stu-id="244d5-133">Name</span></span>                               | <span data-ttu-id="244d5-134">Datentyp</span><span class="sxs-lookup"><span data-stu-id="244d5-134">Data type</span></span>         | <span data-ttu-id="244d5-135">Einheit</span><span class="sxs-lookup"><span data-stu-id="244d5-135">Unit</span></span>                  | <span data-ttu-id="244d5-136">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="244d5-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="244d5-137">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="244d5-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="244d5-138">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="244d5-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="244d5-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="244d5-139">string</span></span><br/> | <span data-ttu-id="244d5-140">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="244d5-140">characters</span></span><br/> | <span data-ttu-id="244d5-141">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="244d5-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="244d5-142">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="244d5-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="244d5-143">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="244d5-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="244d5-144">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="244d5-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="244d5-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="244d5-145">string</span></span><br/> | <span data-ttu-id="244d5-146">–</span><span class="sxs-lookup"><span data-stu-id="244d5-146">n/a</span></span><br/>        | <span data-ttu-id="244d5-147">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="244d5-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="244d5-148">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="244d5-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="244d5-149">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="244d5-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="244d5-150">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="244d5-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="244d5-151">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="244d5-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="244d5-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="244d5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244d5-153">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="244d5-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




