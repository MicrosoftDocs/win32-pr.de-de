---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17eea84ba45ea7c121080f7649b03492c6f3409
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995557"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="4df7d-104">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="4df7d-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="4df7d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4df7d-105">This topic is not current.</span></span> <span data-ttu-id="4df7d-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4df7d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4df7d-107">Beschreibt die Renderingabsicht gemäß definition in der SPECIFICATION v2-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="4df7d-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="4df7d-108">Dieser Wert sollte ignoriert werden, wenn ein Bild oder grafisches Element über ein eingebettetes Profil verfügt, das die Renderingabsicht angibt.</span><span class="sxs-lookup"><span data-stu-id="4df7d-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="4df7d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4df7d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4df7d-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4df7d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4df7d-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4df7d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4df7d-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4df7d-112">Element Information</span></span>



| <span data-ttu-id="4df7d-113">Name</span><span class="sxs-lookup"><span data-stu-id="4df7d-113">Name</span></span> | <span data-ttu-id="4df7d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4df7d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="4df7d-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4df7d-115">Element Type</span></span> <br/>   | <span data-ttu-id="4df7d-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="4df7d-116">Feature</span></span><br/> |
| <span data-ttu-id="4df7d-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4df7d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4df7d-118">Seite</span><span class="sxs-lookup"><span data-stu-id="4df7d-118">Page</span></span><br/>    |
| <span data-ttu-id="4df7d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4df7d-119">Notes</span></span> <br/>          | <span data-ttu-id="4df7d-120">Keine</span><span class="sxs-lookup"><span data-stu-id="4df7d-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="4df7d-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4df7d-121">Structural Content</span></span>

<span data-ttu-id="4df7d-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="4df7d-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4df7d-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4df7d-123">Structure Variables</span></span>

<span data-ttu-id="4df7d-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4df7d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4df7d-125">Name</span><span class="sxs-lookup"><span data-stu-id="4df7d-125">Name</span></span>                               | <span data-ttu-id="4df7d-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4df7d-126">Data type</span></span>         | <span data-ttu-id="4df7d-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="4df7d-127">Unit</span></span>                  | <span data-ttu-id="4df7d-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4df7d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4df7d-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4df7d-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4df7d-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="4df7d-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4df7d-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4df7d-131">string</span></span><br/> | <span data-ttu-id="4df7d-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4df7d-132">characters</span></span><br/> | <span data-ttu-id="4df7d-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4df7d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4df7d-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4df7d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4df7d-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4df7d-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4df7d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4df7d-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4df7d-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4df7d-137">string</span></span><br/> | <span data-ttu-id="4df7d-138">–</span><span class="sxs-lookup"><span data-stu-id="4df7d-138">n/a</span></span><br/>        | <span data-ttu-id="4df7d-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4df7d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4df7d-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4df7d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4df7d-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4df7d-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4df7d-142">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="4df7d-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4df7d-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4df7d-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4df7d-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4df7d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df7d-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4df7d-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




