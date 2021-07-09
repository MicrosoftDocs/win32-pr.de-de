---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageMirrorImage-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: PageMirrorImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe917d6973fbd074111a5da7b6fe5620e7251e9
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549093"
---
# <a name="pagemirrorimage"></a><span data-ttu-id="7888c-105">PageMirrorImage</span><span class="sxs-lookup"><span data-stu-id="7888c-105">PageMirrorImage</span></span>

<span data-ttu-id="7888c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7888c-106">This topic is not current.</span></span> <span data-ttu-id="7888c-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7888c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7888c-108">Beschreibt die Spiegelungseinstellung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7888c-108">Describes the mirroring setting of the output.</span></span>

-   [<span data-ttu-id="7888c-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7888c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7888c-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="7888c-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7888c-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="7888c-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7888c-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7888c-112">Element Information</span></span>



| <span data-ttu-id="7888c-113">Name</span><span class="sxs-lookup"><span data-stu-id="7888c-113">Name</span></span> | <span data-ttu-id="7888c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7888c-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7888c-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7888c-115">Element Type</span></span> <br/>   | <span data-ttu-id="7888c-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="7888c-116">Feature</span></span><br/> |
| <span data-ttu-id="7888c-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7888c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7888c-118">Seite</span><span class="sxs-lookup"><span data-stu-id="7888c-118">Page</span></span><br/>    |
| <span data-ttu-id="7888c-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7888c-119">Notes</span></span> <br/>          | <span data-ttu-id="7888c-120">Keine</span><span class="sxs-lookup"><span data-stu-id="7888c-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7888c-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="7888c-121">Structural Content</span></span>

<span data-ttu-id="7888c-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="7888c-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

## <a name="structure-variables"></a><span data-ttu-id="7888c-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="7888c-123">Structure Variables</span></span>

<span data-ttu-id="7888c-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7888c-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7888c-125">Name</span><span class="sxs-lookup"><span data-stu-id="7888c-125">Name</span></span>                               | <span data-ttu-id="7888c-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7888c-126">Data type</span></span>         | <span data-ttu-id="7888c-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="7888c-127">Unit</span></span>                  | <span data-ttu-id="7888c-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="7888c-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7888c-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7888c-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7888c-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="7888c-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7888c-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7888c-131">string</span></span><br/> | <span data-ttu-id="7888c-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7888c-132">characters</span></span><br/> | <span data-ttu-id="7888c-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="7888c-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7888c-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="7888c-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7888c-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="7888c-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7888c-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7888c-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7888c-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7888c-137">string</span></span><br/> | <span data-ttu-id="7888c-138">n/v</span><span class="sxs-lookup"><span data-stu-id="7888c-138">n/a</span></span><br/>        | <span data-ttu-id="7888c-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="7888c-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7888c-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7888c-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7888c-141">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="7888c-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7888c-142">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="7888c-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7888c-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="7888c-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="7888c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7888c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7888c-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7888c-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




