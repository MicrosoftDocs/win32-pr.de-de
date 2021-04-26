---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf26811bc8c008fa06d647b25e48914a6e724d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999177"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="3a5ad-104">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="3a5ad-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="3a5ad-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-105">This topic is not current.</span></span> <span data-ttu-id="3a5ad-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3a5ad-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a5ad-107">In Verbindung mit dem PageDeviceColorSpaceProfileURI-Parameter definiert dieser Parameter das Renderingverhalten für Elemente, die in einem Gerätefarbraum dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="3a5ad-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a5ad-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a5ad-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a5ad-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3a5ad-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3a5ad-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3a5ad-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a5ad-111">Element Information</span></span>



| <span data-ttu-id="3a5ad-112">Name</span><span class="sxs-lookup"><span data-stu-id="3a5ad-112">Name</span></span> | <span data-ttu-id="3a5ad-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5ad-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5ad-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3a5ad-114">Element Type</span></span> <br/>   | <span data-ttu-id="3a5ad-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="3a5ad-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3a5ad-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3a5ad-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a5ad-117">Seite</span><span class="sxs-lookup"><span data-stu-id="3a5ad-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3a5ad-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a5ad-118">Notes</span></span> <br/>          | <span data-ttu-id="3a5ad-119">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="3a5ad-120">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="3a5ad-121">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="3a5ad-122">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="3a5ad-123">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="3a5ad-124">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3a5ad-125">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3a5ad-125">Structural Content</span></span>

<span data-ttu-id="3a5ad-126">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="3a5ad-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3a5ad-127">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3a5ad-127">Structure Variables</span></span>

<span data-ttu-id="3a5ad-128">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a5ad-129">Name</span><span class="sxs-lookup"><span data-stu-id="3a5ad-129">Name</span></span>                               | <span data-ttu-id="3a5ad-130">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3a5ad-130">Data type</span></span>         | <span data-ttu-id="3a5ad-131">Einheit</span><span class="sxs-lookup"><span data-stu-id="3a5ad-131">Unit</span></span>                  | <span data-ttu-id="3a5ad-132">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3a5ad-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3a5ad-133">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3a5ad-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3a5ad-134">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3a5ad-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3a5ad-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a5ad-135">string</span></span><br/> | <span data-ttu-id="3a5ad-136">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3a5ad-136">characters</span></span><br/> | <span data-ttu-id="3a5ad-137">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3a5ad-138">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3a5ad-139">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3a5ad-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3a5ad-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3a5ad-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a5ad-141">string</span></span><br/> | <span data-ttu-id="3a5ad-142">–</span><span class="sxs-lookup"><span data-stu-id="3a5ad-142">n/a</span></span><br/>        | <span data-ttu-id="3a5ad-143">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3a5ad-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3a5ad-144">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3a5ad-145">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="3a5ad-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3a5ad-146">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3a5ad-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3a5ad-147">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3a5ad-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3a5ad-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a5ad-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a5ad-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3a5ad-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




