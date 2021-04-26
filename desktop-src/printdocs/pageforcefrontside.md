---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996937"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="3a960-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="3a960-104">PageForceFrontSide</span></span>

<span data-ttu-id="3a960-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3a960-105">This topic is not current.</span></span> <span data-ttu-id="3a960-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3a960-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a960-107">Erzwingt, dass die Ausgabe auf der Vorderseite eines Medienblatts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a960-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="3a960-108">Relevant für Medienblätter mit unterschiedlichen Oberflächen auf jeder Seite.</span><span class="sxs-lookup"><span data-stu-id="3a960-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="3a960-109">In Fällen, in denen dieses Feature die Verarbeitungsoptionen beeinträchtigt (z. B. DocumentDuplex), hat PageForceFrontSide Vorrang vor der spezifischen Seite, auf die das Feature angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a960-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="3a960-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a960-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a960-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3a960-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3a960-112">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="3a960-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3a960-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3a960-113">Element Information</span></span>



| <span data-ttu-id="3a960-114">Name</span><span class="sxs-lookup"><span data-stu-id="3a960-114">Name</span></span> | <span data-ttu-id="3a960-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3a960-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3a960-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3a960-116">Element Type</span></span> <br/>   | <span data-ttu-id="3a960-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="3a960-117">Feature</span></span><br/> |
| <span data-ttu-id="3a960-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3a960-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a960-119">Seite</span><span class="sxs-lookup"><span data-stu-id="3a960-119">Page</span></span><br/>    |
| <span data-ttu-id="3a960-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a960-120">Notes</span></span> <br/>          | <span data-ttu-id="3a960-121">Keine</span><span class="sxs-lookup"><span data-stu-id="3a960-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="3a960-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3a960-122">Structural Content</span></span>

<span data-ttu-id="3a960-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3a960-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="3a960-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3a960-124">Structure Variables</span></span>

<span data-ttu-id="3a960-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a960-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a960-126">Name</span><span class="sxs-lookup"><span data-stu-id="3a960-126">Name</span></span>                               | <span data-ttu-id="3a960-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3a960-127">Data type</span></span>         | <span data-ttu-id="3a960-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="3a960-128">Unit</span></span>                  | <span data-ttu-id="3a960-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3a960-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3a960-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3a960-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3a960-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3a960-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3a960-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a960-132">string</span></span><br/> | <span data-ttu-id="3a960-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3a960-133">characters</span></span><br/> | <span data-ttu-id="3a960-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3a960-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3a960-135">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3a960-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3a960-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3a960-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3a960-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3a960-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3a960-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a960-138">string</span></span><br/> | <span data-ttu-id="3a960-139">–</span><span class="sxs-lookup"><span data-stu-id="3a960-139">n/a</span></span><br/>        | <span data-ttu-id="3a960-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3a960-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3a960-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3a960-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3a960-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3a960-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3a960-143">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="3a960-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3a960-144">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3a960-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="3a960-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a960-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a960-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3a960-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




