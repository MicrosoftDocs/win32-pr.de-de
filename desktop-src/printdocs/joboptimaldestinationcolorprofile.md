---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999251"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="fd22d-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="fd22d-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="fd22d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="fd22d-105">This topic is not current.</span></span> <span data-ttu-id="fd22d-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="fd22d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fd22d-107">Gibt das optimale Farbprofil bei der aktuellen Gerätekonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="fd22d-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="fd22d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fd22d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fd22d-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="fd22d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fd22d-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fd22d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fd22d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fd22d-111">Element Information</span></span>



| <span data-ttu-id="fd22d-112">Name</span><span class="sxs-lookup"><span data-stu-id="fd22d-112">Name</span></span> | <span data-ttu-id="fd22d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fd22d-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="fd22d-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fd22d-114">Element Type</span></span> <br/>   | <span data-ttu-id="fd22d-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd22d-115">Property</span></span><br/> |
| <span data-ttu-id="fd22d-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="fd22d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fd22d-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd22d-117">Job</span></span><br/>      |
| <span data-ttu-id="fd22d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd22d-118">Notes</span></span> <br/>          | <span data-ttu-id="fd22d-119">Keine</span><span class="sxs-lookup"><span data-stu-id="fd22d-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="fd22d-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="fd22d-120">Structural Content</span></span>

<span data-ttu-id="fd22d-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="fd22d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="fd22d-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="fd22d-122">Structure Variables</span></span>

<span data-ttu-id="fd22d-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fd22d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fd22d-124">Name</span><span class="sxs-lookup"><span data-stu-id="fd22d-124">Name</span></span>                            | <span data-ttu-id="fd22d-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fd22d-125">Data type</span></span>         | <span data-ttu-id="fd22d-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="fd22d-126">Unit</span></span>           | <span data-ttu-id="fd22d-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="fd22d-127">Supported values</span></span>          | <span data-ttu-id="fd22d-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fd22d-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="fd22d-129">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="fd22d-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="fd22d-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd22d-130">string</span></span><br/> | <span data-ttu-id="fd22d-131">–</span><span class="sxs-lookup"><span data-stu-id="fd22d-131">n/a</span></span><br/> | <span data-ttu-id="fd22d-132">RGB, RGB, RGB, C WIE</span><span class="sxs-lookup"><span data-stu-id="fd22d-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="fd22d-133">Gibt das Farbprofil an.</span><span class="sxs-lookup"><span data-stu-id="fd22d-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="fd22d-134">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="fd22d-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="fd22d-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd22d-135">string</span></span><br/> | <span data-ttu-id="fd22d-136">–</span><span class="sxs-lookup"><span data-stu-id="fd22d-136">n/a</span></span><br/> | <span data-ttu-id="fd22d-137">–</span><span class="sxs-lookup"><span data-stu-id="fd22d-137">n/a</span></span><br/>            | <span data-ttu-id="fd22d-138">Gibt den Dateipfad zum Profil an.</span><span class="sxs-lookup"><span data-stu-id="fd22d-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="fd22d-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="fd22d-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="fd22d-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd22d-140">string</span></span><br/> | <span data-ttu-id="fd22d-141">–</span><span class="sxs-lookup"><span data-stu-id="fd22d-141">n/a</span></span><br/> | <span data-ttu-id="fd22d-142">–</span><span class="sxs-lookup"><span data-stu-id="fd22d-142">n/a</span></span><br/>            | <span data-ttu-id="fd22d-143">Enthält Profildateninhalt.</span><span class="sxs-lookup"><span data-stu-id="fd22d-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fd22d-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fd22d-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fd22d-145">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="fd22d-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fd22d-146">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="fd22d-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="fd22d-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd22d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd22d-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="fd22d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




