---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageColorManagement-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549228"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="8647b-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="8647b-105">PageColorManagement</span></span>

<span data-ttu-id="8647b-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8647b-106">This topic is not current.</span></span> <span data-ttu-id="8647b-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8647b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8647b-108">Konfiguriert die Farbverwaltung für die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="8647b-108">Configures color management for the current page.</span></span> <span data-ttu-id="8647b-109">Dies gilt in SHIM – DM \_ ICMMethod Add System als automatisch.</span><span class="sxs-lookup"><span data-stu-id="8647b-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="8647b-110">Beschreibt, welche Komponente die Farbverwaltung durchführen soll (d. h. Treiber).</span><span class="sxs-lookup"><span data-stu-id="8647b-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="8647b-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8647b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8647b-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8647b-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8647b-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8647b-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8647b-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8647b-114">Element Information</span></span>



| <span data-ttu-id="8647b-115">Name</span><span class="sxs-lookup"><span data-stu-id="8647b-115">Name</span></span> | <span data-ttu-id="8647b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8647b-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8647b-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8647b-117">Element Type</span></span> <br/>   | <span data-ttu-id="8647b-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="8647b-118">Feature</span></span><br/> |
| <span data-ttu-id="8647b-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8647b-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8647b-120">Seite</span><span class="sxs-lookup"><span data-stu-id="8647b-120">Page</span></span><br/>    |
| <span data-ttu-id="8647b-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8647b-121">Notes</span></span> <br/>          | <span data-ttu-id="8647b-122">Keine</span><span class="sxs-lookup"><span data-stu-id="8647b-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="8647b-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8647b-123">Structural Content</span></span>

<span data-ttu-id="8647b-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="8647b-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="8647b-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8647b-125">Structure Variables</span></span>

<span data-ttu-id="8647b-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8647b-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8647b-127">Name</span><span class="sxs-lookup"><span data-stu-id="8647b-127">Name</span></span>                               | <span data-ttu-id="8647b-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8647b-128">Data type</span></span>         | <span data-ttu-id="8647b-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="8647b-129">Unit</span></span>                  | <span data-ttu-id="8647b-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8647b-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8647b-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8647b-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8647b-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="8647b-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8647b-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8647b-133">string</span></span><br/> | <span data-ttu-id="8647b-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8647b-134">characters</span></span><br/> | <span data-ttu-id="8647b-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8647b-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8647b-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8647b-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8647b-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="8647b-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8647b-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8647b-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8647b-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8647b-139">string</span></span><br/> | <span data-ttu-id="8647b-140">n/v</span><span class="sxs-lookup"><span data-stu-id="8647b-140">n/a</span></span><br/>        | <span data-ttu-id="8647b-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="8647b-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8647b-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8647b-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8647b-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8647b-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8647b-144">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="8647b-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8647b-145">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8647b-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="8647b-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8647b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8647b-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8647b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




