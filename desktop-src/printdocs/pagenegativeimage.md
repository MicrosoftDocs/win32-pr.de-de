---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8882c1a5aa026d06b43055a6a74a58c266ea009
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994495"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="952ce-104">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="952ce-104">PageNegativeImage</span></span>

<span data-ttu-id="952ce-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="952ce-105">This topic is not current.</span></span> <span data-ttu-id="952ce-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="952ce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="952ce-107">Beschreibt die negative Einstellung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="952ce-107">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="952ce-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="952ce-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="952ce-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="952ce-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="952ce-110">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="952ce-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="952ce-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="952ce-111">Element Information</span></span>



| <span data-ttu-id="952ce-112">Name</span><span class="sxs-lookup"><span data-stu-id="952ce-112">Name</span></span> | <span data-ttu-id="952ce-113">Wert</span><span class="sxs-lookup"><span data-stu-id="952ce-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="952ce-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="952ce-114">Element Type</span></span> <br/>   | <span data-ttu-id="952ce-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="952ce-115">Feature</span></span><br/> |
| <span data-ttu-id="952ce-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="952ce-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="952ce-117">Seite</span><span class="sxs-lookup"><span data-stu-id="952ce-117">Page</span></span><br/>    |
| <span data-ttu-id="952ce-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="952ce-118">Notes</span></span> <br/>          | <span data-ttu-id="952ce-119">Keine</span><span class="sxs-lookup"><span data-stu-id="952ce-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="952ce-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="952ce-120">Structural Content</span></span>

<span data-ttu-id="952ce-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="952ce-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="952ce-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="952ce-122">Structure Variables</span></span>

<span data-ttu-id="952ce-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="952ce-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="952ce-124">Name</span><span class="sxs-lookup"><span data-stu-id="952ce-124">Name</span></span>                               | <span data-ttu-id="952ce-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="952ce-125">Data type</span></span>         | <span data-ttu-id="952ce-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="952ce-126">Unit</span></span>                  | <span data-ttu-id="952ce-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="952ce-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="952ce-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="952ce-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="952ce-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="952ce-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="952ce-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="952ce-130">string</span></span><br/> | <span data-ttu-id="952ce-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="952ce-131">characters</span></span><br/> | <span data-ttu-id="952ce-132">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="952ce-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="952ce-133">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="952ce-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="952ce-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="952ce-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="952ce-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="952ce-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="952ce-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="952ce-136">string</span></span><br/> | <span data-ttu-id="952ce-137">–</span><span class="sxs-lookup"><span data-stu-id="952ce-137">n/a</span></span><br/>        | <span data-ttu-id="952ce-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="952ce-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="952ce-139">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="952ce-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="952ce-140">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="952ce-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="952ce-141">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="952ce-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="952ce-142">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="952ce-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="952ce-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="952ce-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="952ce-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="952ce-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




