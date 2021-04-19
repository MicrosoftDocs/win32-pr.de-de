---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: Jobpage Order
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e554da890464afdaed033490def1a915f9d7d800
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106350605"
---
# <a name="jobpageorder"></a><span data-ttu-id="be95d-104">Jobpage Order</span><span class="sxs-lookup"><span data-stu-id="be95d-104">JobPageOrder</span></span>

<span data-ttu-id="be95d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="be95d-105">This topic is not current.</span></span> <span data-ttu-id="be95d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="be95d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be95d-107">Definiert die Reihenfolge physischer Seiten für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="be95d-107">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="be95d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="be95d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="be95d-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="be95d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="be95d-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="be95d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="be95d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="be95d-111">Element Information</span></span>



| <span data-ttu-id="be95d-112">Name</span><span class="sxs-lookup"><span data-stu-id="be95d-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="be95d-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="be95d-113">Element Type</span></span> <br/>   | <span data-ttu-id="be95d-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="be95d-114">Feature</span></span><br/> |
| <span data-ttu-id="be95d-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="be95d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="be95d-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="be95d-116">Job</span></span><br/>     |
| <span data-ttu-id="be95d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be95d-117">Notes</span></span> <br/>          | <span data-ttu-id="be95d-118">Keine</span><span class="sxs-lookup"><span data-stu-id="be95d-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="be95d-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="be95d-119">Structural Content</span></span>

<span data-ttu-id="be95d-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="be95d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="be95d-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="be95d-121">Structure Variables</span></span>

<span data-ttu-id="be95d-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="be95d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="be95d-123">Name</span><span class="sxs-lookup"><span data-stu-id="be95d-123">Name</span></span>                               | <span data-ttu-id="be95d-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="be95d-124">Data type</span></span>         | <span data-ttu-id="be95d-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="be95d-125">Unit</span></span>                  | <span data-ttu-id="be95d-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="be95d-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="be95d-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be95d-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="be95d-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="be95d-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="be95d-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="be95d-129">string</span></span><br/> | <span data-ttu-id="be95d-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="be95d-130">characters</span></span><br/> | <span data-ttu-id="be95d-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="be95d-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="be95d-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="be95d-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="be95d-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="be95d-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="be95d-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="be95d-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="be95d-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="be95d-135">string</span></span><br/> | <span data-ttu-id="be95d-136">–</span><span class="sxs-lookup"><span data-stu-id="be95d-136">n/a</span></span><br/>        | <span data-ttu-id="be95d-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="be95d-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="be95d-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="be95d-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="be95d-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="be95d-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="be95d-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="be95d-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="be95d-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="be95d-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="be95d-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be95d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be95d-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="be95d-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




