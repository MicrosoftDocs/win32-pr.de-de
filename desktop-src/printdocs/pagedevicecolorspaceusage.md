---
description: Überprüfen Sie das benutzerkonfigurierbare PageDeviceColorSpaceUsage-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b81a37d103d3ce5f1cbb1fb8c032a18d495c2c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396665"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="7b5d0-105">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="7b5d0-105">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="7b5d0-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-106">This topic is not current.</span></span> <span data-ttu-id="7b5d0-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7b5d0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b5d0-108">In Verbindung mit dem PageDeviceColorSpaceProfileURI-Parameter definiert dieser Parameter das Renderingverhalten für Elemente, die in einem Gerätefarbraum dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-108">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="7b5d0-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7b5d0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b5d0-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7b5d0-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7b5d0-111">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="7b5d0-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7b5d0-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7b5d0-112">Element Information</span></span>



| <span data-ttu-id="7b5d0-113">Name</span><span class="sxs-lookup"><span data-stu-id="7b5d0-113">Name</span></span> | <span data-ttu-id="7b5d0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7b5d0-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5d0-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7b5d0-115">Element Type</span></span> <br/>   | <span data-ttu-id="7b5d0-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="7b5d0-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7b5d0-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7b5d0-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b5d0-118">Seite</span><span class="sxs-lookup"><span data-stu-id="7b5d0-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b5d0-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b5d0-119">Notes</span></span> <br/>          | <span data-ttu-id="7b5d0-120">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="7b5d0-121">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="7b5d0-122">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="7b5d0-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="7b5d0-124">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="7b5d0-125">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7b5d0-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7b5d0-126">Structural Content</span></span>

<span data-ttu-id="7b5d0-127">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="7b5d0-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7b5d0-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="7b5d0-128">Structure Variables</span></span>

<span data-ttu-id="7b5d0-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b5d0-130">Name</span><span class="sxs-lookup"><span data-stu-id="7b5d0-130">Name</span></span>                               | <span data-ttu-id="7b5d0-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7b5d0-131">Data type</span></span>         | <span data-ttu-id="7b5d0-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="7b5d0-132">Unit</span></span>                  | <span data-ttu-id="7b5d0-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="7b5d0-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7b5d0-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7b5d0-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7b5d0-135">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="7b5d0-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7b5d0-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b5d0-136">string</span></span><br/> | <span data-ttu-id="7b5d0-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7b5d0-137">characters</span></span><br/> | <span data-ttu-id="7b5d0-138">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7b5d0-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7b5d0-139">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7b5d0-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7b5d0-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7b5d0-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7b5d0-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b5d0-142">string</span></span><br/> | <span data-ttu-id="7b5d0-143">–</span><span class="sxs-lookup"><span data-stu-id="7b5d0-143">n/a</span></span><br/>        | <span data-ttu-id="7b5d0-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="7b5d0-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7b5d0-145">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7b5d0-146">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="7b5d0-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7b5d0-147">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="7b5d0-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7b5d0-148">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="7b5d0-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7b5d0-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b5d0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b5d0-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7b5d0-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




