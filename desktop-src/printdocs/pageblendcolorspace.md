---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: "\"Pgeblendcolorspace\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf68660929839fad79be26daebf32b9bc0f7ea5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106353650"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="3a8ef-104">"Pgeblendcolorspace"</span><span class="sxs-lookup"><span data-stu-id="3a8ef-104">PageBlendColorSpace</span></span>

<span data-ttu-id="3a8ef-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-105">This topic is not current.</span></span> <span data-ttu-id="3a8ef-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3a8ef-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a8ef-107">Beschreibt den Farb Raum, der für Mischungs Vorgänge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="3a8ef-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a8ef-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a8ef-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a8ef-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3a8ef-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3a8ef-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3a8ef-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a8ef-111">Element Information</span></span>



| <span data-ttu-id="3a8ef-112">Name</span><span class="sxs-lookup"><span data-stu-id="3a8ef-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8ef-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3a8ef-113">Element Type</span></span> <br/>   | <span data-ttu-id="3a8ef-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="3a8ef-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3a8ef-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="3a8ef-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a8ef-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3a8ef-116">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3a8ef-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a8ef-117">Notes</span></span> <br/>          | <span data-ttu-id="3a8ef-118">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="3a8ef-119">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="3a8ef-120">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="3a8ef-121">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="3a8ef-122">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3a8ef-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a8ef-123">Structural Content</span></span>

<span data-ttu-id="3a8ef-124">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3a8ef-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="3a8ef-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3a8ef-125">Structure Variables</span></span>

<span data-ttu-id="3a8ef-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a8ef-127">Name</span><span class="sxs-lookup"><span data-stu-id="3a8ef-127">Name</span></span>                               | <span data-ttu-id="3a8ef-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3a8ef-128">Data type</span></span>         | <span data-ttu-id="3a8ef-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="3a8ef-129">Unit</span></span>                  | <span data-ttu-id="3a8ef-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3a8ef-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3a8ef-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3a8ef-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3a8ef-132">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="3a8ef-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3a8ef-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a8ef-133">string</span></span><br/> | <span data-ttu-id="3a8ef-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3a8ef-134">characters</span></span><br/> | <span data-ttu-id="3a8ef-135">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3a8ef-136">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3a8ef-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3a8ef-138">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="3a8ef-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3a8ef-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a8ef-139">string</span></span><br/> | <span data-ttu-id="3a8ef-140">–</span><span class="sxs-lookup"><span data-stu-id="3a8ef-140">n/a</span></span><br/>        | <span data-ttu-id="3a8ef-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3a8ef-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3a8ef-142">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3a8ef-143">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3a8ef-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3a8ef-144">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3a8ef-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3a8ef-145">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3a8ef-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="3a8ef-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a8ef-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a8ef-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="3a8ef-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




