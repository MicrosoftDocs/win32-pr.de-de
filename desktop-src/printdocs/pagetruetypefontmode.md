---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageTrueTypeFontMode-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf30af3684693f594f497dbad95d4f9a7743d624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395615"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="a2d0b-105">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="a2d0b-105">PageTrueTypeFontMode</span></span>

<span data-ttu-id="a2d0b-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-106">This topic is not current.</span></span> <span data-ttu-id="a2d0b-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a2d0b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a2d0b-108">Beschreibt die Zu verwendende Methode der TrueType-Schriftartbehandlung.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-108">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="a2d0b-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a2d0b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a2d0b-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a2d0b-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a2d0b-111">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="a2d0b-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a2d0b-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a2d0b-112">Element Information</span></span>



| <span data-ttu-id="a2d0b-113">Name</span><span class="sxs-lookup"><span data-stu-id="a2d0b-113">Name</span></span> | <span data-ttu-id="a2d0b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a2d0b-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a2d0b-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a2d0b-115">Element Type</span></span> <br/>   | <span data-ttu-id="a2d0b-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="a2d0b-116">Feature</span></span><br/> |
| <span data-ttu-id="a2d0b-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a2d0b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a2d0b-118">Seite</span><span class="sxs-lookup"><span data-stu-id="a2d0b-118">Page</span></span><br/>    |
| <span data-ttu-id="a2d0b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2d0b-119">Notes</span></span> <br/>          | <span data-ttu-id="a2d0b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="a2d0b-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a2d0b-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a2d0b-121">Structural Content</span></span>

<span data-ttu-id="a2d0b-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="a2d0b-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
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

## <a name="structure-variables"></a><span data-ttu-id="a2d0b-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a2d0b-123">Structure Variables</span></span>

<span data-ttu-id="a2d0b-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a2d0b-125">Name</span><span class="sxs-lookup"><span data-stu-id="a2d0b-125">Name</span></span>                               | <span data-ttu-id="a2d0b-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2d0b-126">Data type</span></span>         | <span data-ttu-id="a2d0b-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="a2d0b-127">Unit</span></span>                  | <span data-ttu-id="a2d0b-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a2d0b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a2d0b-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a2d0b-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a2d0b-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a2d0b-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a2d0b-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a2d0b-131">string</span></span><br/> | <span data-ttu-id="a2d0b-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a2d0b-132">characters</span></span><br/> | <span data-ttu-id="a2d0b-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a2d0b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a2d0b-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a2d0b-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a2d0b-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a2d0b-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a2d0b-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a2d0b-137">string</span></span><br/> | <span data-ttu-id="a2d0b-138">–</span><span class="sxs-lookup"><span data-stu-id="a2d0b-138">n/a</span></span><br/>        | <span data-ttu-id="a2d0b-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a2d0b-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a2d0b-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a2d0b-141">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="a2d0b-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a2d0b-142">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="a2d0b-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a2d0b-143">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a2d0b-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="a2d0b-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2d0b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d0b-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a2d0b-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




