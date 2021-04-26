---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81a037b6b32ff71b53688dfd6fc8afd5f10bb69
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997657"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="7a105-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="7a105-104">PageColorManagement</span></span>

<span data-ttu-id="7a105-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7a105-105">This topic is not current.</span></span> <span data-ttu-id="7a105-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7a105-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a105-107">Konfiguriert die Farbverwaltung für die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="7a105-107">Configures color management for the current page.</span></span> <span data-ttu-id="7a105-108">Dies gilt in SHIM – DM \_ ICMMethod Add System als automatisch.</span><span class="sxs-lookup"><span data-stu-id="7a105-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="7a105-109">Beschreibt, welche Komponente die Farbverwaltung durchführen soll (d. h. Treiber).</span><span class="sxs-lookup"><span data-stu-id="7a105-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="7a105-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7a105-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a105-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7a105-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7a105-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7a105-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7a105-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7a105-113">Element Information</span></span>



| <span data-ttu-id="7a105-114">Name</span><span class="sxs-lookup"><span data-stu-id="7a105-114">Name</span></span> | <span data-ttu-id="7a105-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7a105-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7a105-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7a105-116">Element Type</span></span> <br/>   | <span data-ttu-id="7a105-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="7a105-117">Feature</span></span><br/> |
| <span data-ttu-id="7a105-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7a105-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a105-119">Seite</span><span class="sxs-lookup"><span data-stu-id="7a105-119">Page</span></span><br/>    |
| <span data-ttu-id="7a105-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a105-120">Notes</span></span> <br/>          | <span data-ttu-id="7a105-121">Keine</span><span class="sxs-lookup"><span data-stu-id="7a105-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="7a105-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7a105-122">Structural Content</span></span>

<span data-ttu-id="7a105-123">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="7a105-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7a105-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="7a105-124">Structure Variables</span></span>

<span data-ttu-id="7a105-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7a105-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a105-126">Name</span><span class="sxs-lookup"><span data-stu-id="7a105-126">Name</span></span>                               | <span data-ttu-id="7a105-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7a105-127">Data type</span></span>         | <span data-ttu-id="7a105-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="7a105-128">Unit</span></span>                  | <span data-ttu-id="7a105-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="7a105-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7a105-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7a105-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a105-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="7a105-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7a105-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7a105-132">string</span></span><br/> | <span data-ttu-id="7a105-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7a105-133">characters</span></span><br/> | <span data-ttu-id="7a105-134">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7a105-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7a105-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="7a105-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7a105-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="7a105-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7a105-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7a105-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7a105-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7a105-138">string</span></span><br/> | <span data-ttu-id="7a105-139">–</span><span class="sxs-lookup"><span data-stu-id="7a105-139">n/a</span></span><br/>        | <span data-ttu-id="7a105-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="7a105-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7a105-141">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7a105-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7a105-142">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="7a105-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7a105-143">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="7a105-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7a105-144">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="7a105-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7a105-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a105-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a105-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7a105-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




