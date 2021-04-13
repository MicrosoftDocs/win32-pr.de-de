---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09ae5bdcf7e1742ae15b0b6d832b3d15d47718b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104352018"
---
# <a name="pageoutputquality"></a><span data-ttu-id="1fe1d-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="1fe1d-104">PageOutputQuality</span></span>

<span data-ttu-id="1fe1d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-105">This topic is not current.</span></span> <span data-ttu-id="1fe1d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fe1d-107">Beschreibt die Qualitätsstufe der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="1fe1d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1fe1d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1fe1d-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="1fe1d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1fe1d-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1fe1d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1fe1d-111">Element Information</span></span>



| <span data-ttu-id="1fe1d-112">Name</span><span class="sxs-lookup"><span data-stu-id="1fe1d-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="1fe1d-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1fe1d-113">Element Type</span></span> <br/>   | <span data-ttu-id="1fe1d-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="1fe1d-114">Feature</span></span><br/> |
| <span data-ttu-id="1fe1d-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="1fe1d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1fe1d-116">Seite</span><span class="sxs-lookup"><span data-stu-id="1fe1d-116">Page</span></span><br/>    |
| <span data-ttu-id="1fe1d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fe1d-117">Notes</span></span> <br/>          | <span data-ttu-id="1fe1d-118">Keine</span><span class="sxs-lookup"><span data-stu-id="1fe1d-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1fe1d-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="1fe1d-119">Structural Content</span></span>

<span data-ttu-id="1fe1d-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="1fe1d-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="1fe1d-121">Structure Variables</span></span>

<span data-ttu-id="1fe1d-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1fe1d-123">Name</span><span class="sxs-lookup"><span data-stu-id="1fe1d-123">Name</span></span>                               | <span data-ttu-id="1fe1d-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1fe1d-124">Data type</span></span>         | <span data-ttu-id="1fe1d-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="1fe1d-125">Unit</span></span>                  | <span data-ttu-id="1fe1d-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="1fe1d-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1fe1d-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1fe1d-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1fe1d-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="1fe1d-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1fe1d-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1fe1d-129">string</span></span><br/> | <span data-ttu-id="1fe1d-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="1fe1d-130">characters</span></span><br/> | <span data-ttu-id="1fe1d-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1fe1d-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1fe1d-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="1fe1d-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="1fe1d-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1fe1d-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1fe1d-135">string</span></span><br/> | <span data-ttu-id="1fe1d-136">–</span><span class="sxs-lookup"><span data-stu-id="1fe1d-136">n/a</span></span><br/>        | <span data-ttu-id="1fe1d-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="1fe1d-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="1fe1d-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1fe1d-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1fe1d-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1fe1d-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="1fe1d-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fe1d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fe1d-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="1fe1d-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




