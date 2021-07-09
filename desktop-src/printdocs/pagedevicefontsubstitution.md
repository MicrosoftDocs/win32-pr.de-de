---
description: Überprüfen Sie das benutzerkonfigurierbare PageDeviceFontSubsators-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubsona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5650c687a4c96e6c54ef7ea0631e77407e874
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549198"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="819ac-105">PageDeviceFontSubsona</span><span class="sxs-lookup"><span data-stu-id="819ac-105">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="819ac-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="819ac-106">This topic is not current.</span></span> <span data-ttu-id="819ac-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="819ac-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="819ac-108">Beschreibt den aktivierten/deaktivierten Zustand der Geräteschriftartersetzung.</span><span class="sxs-lookup"><span data-stu-id="819ac-108">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="819ac-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="819ac-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="819ac-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="819ac-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="819ac-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="819ac-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="819ac-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="819ac-112">Element Information</span></span>



| <span data-ttu-id="819ac-113">Name</span><span class="sxs-lookup"><span data-stu-id="819ac-113">Name</span></span> | <span data-ttu-id="819ac-114">Wert</span><span class="sxs-lookup"><span data-stu-id="819ac-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="819ac-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="819ac-115">Element Type</span></span> <br/>   | <span data-ttu-id="819ac-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="819ac-116">Feature</span></span><br/> |
| <span data-ttu-id="819ac-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="819ac-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="819ac-118">Seite</span><span class="sxs-lookup"><span data-stu-id="819ac-118">Page</span></span><br/>    |
| <span data-ttu-id="819ac-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="819ac-119">Notes</span></span> <br/>          | <span data-ttu-id="819ac-120">Keine</span><span class="sxs-lookup"><span data-stu-id="819ac-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="819ac-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="819ac-121">Structural Content</span></span>

<span data-ttu-id="819ac-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="819ac-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
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

## <a name="structure-variables"></a><span data-ttu-id="819ac-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="819ac-123">Structure Variables</span></span>

<span data-ttu-id="819ac-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="819ac-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="819ac-125">Name</span><span class="sxs-lookup"><span data-stu-id="819ac-125">Name</span></span>                               | <span data-ttu-id="819ac-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="819ac-126">Data type</span></span>         | <span data-ttu-id="819ac-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="819ac-127">Unit</span></span>                  | <span data-ttu-id="819ac-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="819ac-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="819ac-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="819ac-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="819ac-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="819ac-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="819ac-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="819ac-131">string</span></span><br/> | <span data-ttu-id="819ac-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="819ac-132">characters</span></span><br/> | <span data-ttu-id="819ac-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="819ac-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="819ac-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="819ac-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="819ac-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="819ac-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="819ac-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="819ac-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="819ac-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="819ac-137">string</span></span><br/> | <span data-ttu-id="819ac-138">n/v</span><span class="sxs-lookup"><span data-stu-id="819ac-138">n/a</span></span><br/>        | <span data-ttu-id="819ac-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="819ac-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="819ac-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="819ac-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="819ac-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="819ac-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="819ac-142">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="819ac-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="819ac-143">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="819ac-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="819ac-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="819ac-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="819ac-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="819ac-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




