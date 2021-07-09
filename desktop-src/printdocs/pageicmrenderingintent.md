---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageICMRenderingIntent-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549178"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="a1d79-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="a1d79-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="a1d79-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a1d79-106">This topic is not current.</span></span> <span data-ttu-id="a1d79-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a1d79-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1d79-108">Beschreibt die Renderingabsicht gemäß definition in der SPECIFICATION v2-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="a1d79-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="a1d79-109">Dieser Wert sollte ignoriert werden, wenn ein Bild oder grafisches Element über ein eingebettetes Profil verfügt, das die Renderingabsicht angibt.</span><span class="sxs-lookup"><span data-stu-id="a1d79-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="a1d79-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a1d79-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a1d79-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a1d79-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a1d79-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a1d79-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a1d79-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a1d79-113">Element Information</span></span>



| <span data-ttu-id="a1d79-114">Name</span><span class="sxs-lookup"><span data-stu-id="a1d79-114">Name</span></span> | <span data-ttu-id="a1d79-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a1d79-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a1d79-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a1d79-116">Element Type</span></span> <br/>   | <span data-ttu-id="a1d79-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="a1d79-117">Feature</span></span><br/> |
| <span data-ttu-id="a1d79-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a1d79-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1d79-119">Seite</span><span class="sxs-lookup"><span data-stu-id="a1d79-119">Page</span></span><br/>    |
| <span data-ttu-id="a1d79-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1d79-120">Notes</span></span> <br/>          | <span data-ttu-id="a1d79-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a1d79-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="a1d79-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a1d79-122">Structural Content</span></span>

<span data-ttu-id="a1d79-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="a1d79-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="a1d79-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a1d79-124">Structure Variables</span></span>

<span data-ttu-id="a1d79-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a1d79-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1d79-126">Name</span><span class="sxs-lookup"><span data-stu-id="a1d79-126">Name</span></span>                               | <span data-ttu-id="a1d79-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a1d79-127">Data type</span></span>         | <span data-ttu-id="a1d79-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="a1d79-128">Unit</span></span>                  | <span data-ttu-id="a1d79-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a1d79-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a1d79-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a1d79-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1d79-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a1d79-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a1d79-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a1d79-132">string</span></span><br/> | <span data-ttu-id="a1d79-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a1d79-133">characters</span></span><br/> | <span data-ttu-id="a1d79-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a1d79-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a1d79-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a1d79-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a1d79-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a1d79-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a1d79-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a1d79-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a1d79-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a1d79-138">string</span></span><br/> | <span data-ttu-id="a1d79-139">n/v</span><span class="sxs-lookup"><span data-stu-id="a1d79-139">n/a</span></span><br/>        | <span data-ttu-id="a1d79-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a1d79-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a1d79-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a1d79-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a1d79-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a1d79-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a1d79-143">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="a1d79-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a1d79-144">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a1d79-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a1d79-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1d79-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d79-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a1d79-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




