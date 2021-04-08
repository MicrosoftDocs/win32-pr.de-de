---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: Pagede vicecolorspaceusage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77f143457ea24d5c23aba443209ba35ce02454
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869660"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="4d04d-104">Pagede vicecolorspaceusage</span><span class="sxs-lookup"><span data-stu-id="4d04d-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="4d04d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4d04d-105">This topic is not current.</span></span> <span data-ttu-id="4d04d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4d04d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d04d-107">In Verbindung mit dem pagedevicecolorspaceprofileuri-Parameter definiert dieser Parameter das Renderingverhalten für Elemente, die in einem Geräte Farbraum dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d04d-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="4d04d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d04d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d04d-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4d04d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4d04d-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="4d04d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4d04d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d04d-111">Element Information</span></span>



| <span data-ttu-id="4d04d-112">Name</span><span class="sxs-lookup"><span data-stu-id="4d04d-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04d-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4d04d-113">Element Type</span></span> <br/>   | <span data-ttu-id="4d04d-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="4d04d-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4d04d-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="4d04d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d04d-116">Seite</span><span class="sxs-lookup"><span data-stu-id="4d04d-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d04d-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d04d-117">Notes</span></span> <br/>          | <span data-ttu-id="4d04d-118">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen Print Tickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d04d-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="4d04d-119">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="4d04d-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4d04d-120">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="4d04d-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4d04d-121">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="4d04d-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4d04d-122">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4d04d-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4d04d-123">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="4d04d-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4d04d-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4d04d-124">Structural Content</span></span>

<span data-ttu-id="4d04d-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4d04d-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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

## <a name="structure-variables"></a><span data-ttu-id="4d04d-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4d04d-126">Structure Variables</span></span>

<span data-ttu-id="4d04d-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4d04d-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d04d-128">Name</span><span class="sxs-lookup"><span data-stu-id="4d04d-128">Name</span></span>                               | <span data-ttu-id="4d04d-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4d04d-129">Data type</span></span>         | <span data-ttu-id="4d04d-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="4d04d-130">Unit</span></span>                  | <span data-ttu-id="4d04d-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4d04d-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4d04d-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4d04d-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4d04d-133">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="4d04d-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4d04d-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d04d-134">string</span></span><br/> | <span data-ttu-id="4d04d-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4d04d-135">characters</span></span><br/> | <span data-ttu-id="4d04d-136">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="4d04d-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4d04d-137">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4d04d-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4d04d-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4d04d-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4d04d-139">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="4d04d-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4d04d-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d04d-140">string</span></span><br/> | <span data-ttu-id="4d04d-141">–</span><span class="sxs-lookup"><span data-stu-id="4d04d-141">n/a</span></span><br/>        | <span data-ttu-id="4d04d-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4d04d-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4d04d-143">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4d04d-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4d04d-144">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="4d04d-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4d04d-145">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="4d04d-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4d04d-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4d04d-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="4d04d-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d04d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d04d-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="4d04d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




