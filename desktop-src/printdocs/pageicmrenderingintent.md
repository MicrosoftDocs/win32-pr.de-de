---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: Pageicmrenderingintent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219091"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="e3bce-104">Pageicmrenderingintent</span><span class="sxs-lookup"><span data-stu-id="e3bce-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="e3bce-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e3bce-105">This topic is not current.</span></span> <span data-ttu-id="e3bce-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3bce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3bce-107">Beschreibt die renderingabsicht, wie in der Spezifikation von "ICC V2" definiert.</span><span class="sxs-lookup"><span data-stu-id="e3bce-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="e3bce-108">Dieser Wert sollte ignoriert werden, wenn ein Bild oder ein grafisches Element über ein eingebettetes Profil verfügt, das die renderingabsicht angibt.</span><span class="sxs-lookup"><span data-stu-id="e3bce-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="e3bce-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e3bce-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3bce-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="e3bce-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e3bce-111">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3bce-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e3bce-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e3bce-112">Element Information</span></span>



| <span data-ttu-id="e3bce-113">Name</span><span class="sxs-lookup"><span data-stu-id="e3bce-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="e3bce-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e3bce-114">Element Type</span></span> <br/>   | <span data-ttu-id="e3bce-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="e3bce-115">Feature</span></span><br/> |
| <span data-ttu-id="e3bce-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="e3bce-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3bce-117">Seite</span><span class="sxs-lookup"><span data-stu-id="e3bce-117">Page</span></span><br/>    |
| <span data-ttu-id="e3bce-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3bce-118">Notes</span></span> <br/>          | <span data-ttu-id="e3bce-119">Keine</span><span class="sxs-lookup"><span data-stu-id="e3bce-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="e3bce-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="e3bce-120">Structural Content</span></span>

<span data-ttu-id="e3bce-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="e3bce-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e3bce-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e3bce-122">Structure Variables</span></span>

<span data-ttu-id="e3bce-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e3bce-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3bce-124">Name</span><span class="sxs-lookup"><span data-stu-id="e3bce-124">Name</span></span>                               | <span data-ttu-id="e3bce-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e3bce-125">Data type</span></span>         | <span data-ttu-id="e3bce-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="e3bce-126">Unit</span></span>                  | <span data-ttu-id="e3bce-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e3bce-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e3bce-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e3bce-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e3bce-129">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="e3bce-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e3bce-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e3bce-130">string</span></span><br/> | <span data-ttu-id="e3bce-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e3bce-131">characters</span></span><br/> | <span data-ttu-id="e3bce-132">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="e3bce-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e3bce-133">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="e3bce-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e3bce-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="e3bce-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e3bce-135">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="e3bce-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e3bce-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e3bce-136">string</span></span><br/> | <span data-ttu-id="e3bce-137">–</span><span class="sxs-lookup"><span data-stu-id="e3bce-137">n/a</span></span><br/>        | <span data-ttu-id="e3bce-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="e3bce-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e3bce-139">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e3bce-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e3bce-140">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3bce-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e3bce-141">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="e3bce-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e3bce-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="e3bce-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e3bce-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3bce-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3bce-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e3bce-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




