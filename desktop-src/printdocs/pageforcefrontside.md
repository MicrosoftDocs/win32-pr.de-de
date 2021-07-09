---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageForceFrontSide-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549188"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="5b87c-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="5b87c-105">PageForceFrontSide</span></span>

<span data-ttu-id="5b87c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5b87c-106">This topic is not current.</span></span> <span data-ttu-id="5b87c-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5b87c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5b87c-108">Erzwingt, dass die Ausgabe an der Vorderseite eines Medienblatts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b87c-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="5b87c-109">Relevant für Medienblätter mit unterschiedlichen Oberflächen auf jeder Seite.</span><span class="sxs-lookup"><span data-stu-id="5b87c-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="5b87c-110">In Fällen, in denen dieses Feature Verarbeitungsoptionen (z. B. DocumentDuplex) beeinträchtigt, hat PageForceFrontSide Vorrang für die spezifische Seite, auf die das Feature angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b87c-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="5b87c-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5b87c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5b87c-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5b87c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5b87c-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5b87c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5b87c-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5b87c-114">Element Information</span></span>



| <span data-ttu-id="5b87c-115">Name</span><span class="sxs-lookup"><span data-stu-id="5b87c-115">Name</span></span> | <span data-ttu-id="5b87c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5b87c-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5b87c-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5b87c-117">Element Type</span></span> <br/>   | <span data-ttu-id="5b87c-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="5b87c-118">Feature</span></span><br/> |
| <span data-ttu-id="5b87c-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5b87c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5b87c-120">Seite</span><span class="sxs-lookup"><span data-stu-id="5b87c-120">Page</span></span><br/>    |
| <span data-ttu-id="5b87c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b87c-121">Notes</span></span> <br/>          | <span data-ttu-id="5b87c-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5b87c-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5b87c-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5b87c-123">Structural Content</span></span>

<span data-ttu-id="5b87c-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="5b87c-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5b87c-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="5b87c-125">Structure Variables</span></span>

<span data-ttu-id="5b87c-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5b87c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5b87c-127">Name</span><span class="sxs-lookup"><span data-stu-id="5b87c-127">Name</span></span>                               | <span data-ttu-id="5b87c-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5b87c-128">Data type</span></span>         | <span data-ttu-id="5b87c-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="5b87c-129">Unit</span></span>                  | <span data-ttu-id="5b87c-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="5b87c-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5b87c-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5b87c-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5b87c-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="5b87c-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5b87c-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5b87c-133">string</span></span><br/> | <span data-ttu-id="5b87c-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5b87c-134">characters</span></span><br/> | <span data-ttu-id="5b87c-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5b87c-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5b87c-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="5b87c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5b87c-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="5b87c-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5b87c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5b87c-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5b87c-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5b87c-139">string</span></span><br/> | <span data-ttu-id="5b87c-140">n/v</span><span class="sxs-lookup"><span data-stu-id="5b87c-140">n/a</span></span><br/>        | <span data-ttu-id="5b87c-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="5b87c-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5b87c-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5b87c-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5b87c-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5b87c-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5b87c-144">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="5b87c-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5b87c-145">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="5b87c-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5b87c-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b87c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b87c-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5b87c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




