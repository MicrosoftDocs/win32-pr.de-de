---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: Pagedestinationcolorprofile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106353289"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="9f7d3-104">Pagedestinationcolorprofile</span><span class="sxs-lookup"><span data-stu-id="9f7d3-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="9f7d3-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-105">This topic is not current.</span></span> <span data-ttu-id="9f7d3-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9f7d3-107">Definiert die Merkmale des Ziel Farbprofils.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="9f7d3-108">Beschreibt, ob die Anwendung oder der Treiber das zu verwendende Ziel Farbprofil auswählt.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="9f7d3-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9f7d3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9f7d3-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9f7d3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9f7d3-111">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9f7d3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9f7d3-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9f7d3-112">Element Information</span></span>



| <span data-ttu-id="9f7d3-113">Name</span><span class="sxs-lookup"><span data-stu-id="9f7d3-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7d3-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9f7d3-114">Element Type</span></span> <br/>   | <span data-ttu-id="9f7d3-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="9f7d3-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9f7d3-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="9f7d3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9f7d3-117">Seite</span><span class="sxs-lookup"><span data-stu-id="9f7d3-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9f7d3-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f7d3-118">Notes</span></span> <br/>          | <span data-ttu-id="9f7d3-119">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9f7d3-120">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9f7d3-121">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9f7d3-122">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9f7d3-123">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9f7d3-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9f7d3-124">Structural Content</span></span>

<span data-ttu-id="9f7d3-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9f7d3-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="9f7d3-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9f7d3-126">Structure Variables</span></span>

<span data-ttu-id="9f7d3-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9f7d3-128">Name</span><span class="sxs-lookup"><span data-stu-id="9f7d3-128">Name</span></span>                               | <span data-ttu-id="9f7d3-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9f7d3-129">Data type</span></span>         | <span data-ttu-id="9f7d3-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="9f7d3-130">Unit</span></span>                  | <span data-ttu-id="9f7d3-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9f7d3-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9f7d3-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9f7d3-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9f7d3-133">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9f7d3-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f7d3-134">string</span></span><br/> | <span data-ttu-id="9f7d3-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9f7d3-135">characters</span></span><br/> | <span data-ttu-id="9f7d3-136">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9f7d3-137">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9f7d3-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9f7d3-139">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9f7d3-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f7d3-140">string</span></span><br/> | <span data-ttu-id="9f7d3-141">–</span><span class="sxs-lookup"><span data-stu-id="9f7d3-141">n/a</span></span><br/>        | <span data-ttu-id="9f7d3-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9f7d3-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9f7d3-143">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9f7d3-144">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9f7d3-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9f7d3-145">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9f7d3-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9f7d3-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9f7d3-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f7d3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f7d3-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9f7d3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




