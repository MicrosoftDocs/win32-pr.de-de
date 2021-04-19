---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: Paarlose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd73e2808380bf73a7df7156c10c40cfa339765
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106370365"
---
# <a name="pageborderless"></a><span data-ttu-id="2e57f-104">Paarlose</span><span class="sxs-lookup"><span data-stu-id="2e57f-104">PageBorderless</span></span>

<span data-ttu-id="2e57f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2e57f-105">This topic is not current.</span></span> <span data-ttu-id="2e57f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e57f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e57f-107">Beschreibt, wann Bildinhalt an die physischen Kanten der Medien gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e57f-107">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="2e57f-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2e57f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e57f-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2e57f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2e57f-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2e57f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2e57f-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2e57f-111">Element Information</span></span>



| <span data-ttu-id="2e57f-112">Name</span><span class="sxs-lookup"><span data-stu-id="2e57f-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2e57f-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2e57f-113">Element Type</span></span> <br/>   | <span data-ttu-id="2e57f-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="2e57f-114">Feature</span></span><br/> |
| <span data-ttu-id="2e57f-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="2e57f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e57f-116">Seite</span><span class="sxs-lookup"><span data-stu-id="2e57f-116">Page</span></span><br/>    |
| <span data-ttu-id="2e57f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e57f-117">Notes</span></span> <br/>          | <span data-ttu-id="2e57f-118">Keine</span><span class="sxs-lookup"><span data-stu-id="2e57f-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2e57f-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="2e57f-119">Structural Content</span></span>

<span data-ttu-id="2e57f-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="2e57f-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="2e57f-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="2e57f-121">Structure Variables</span></span>

<span data-ttu-id="2e57f-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2e57f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e57f-123">Name</span><span class="sxs-lookup"><span data-stu-id="2e57f-123">Name</span></span>                               | <span data-ttu-id="2e57f-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2e57f-124">Data type</span></span>         | <span data-ttu-id="2e57f-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="2e57f-125">Unit</span></span>                  | <span data-ttu-id="2e57f-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="2e57f-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2e57f-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2e57f-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2e57f-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="2e57f-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2e57f-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e57f-129">string</span></span><br/> | <span data-ttu-id="2e57f-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="2e57f-130">characters</span></span><br/> | <span data-ttu-id="2e57f-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="2e57f-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2e57f-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="2e57f-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2e57f-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="2e57f-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2e57f-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="2e57f-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2e57f-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e57f-135">string</span></span><br/> | <span data-ttu-id="2e57f-136">–</span><span class="sxs-lookup"><span data-stu-id="2e57f-136">n/a</span></span><br/>        | <span data-ttu-id="2e57f-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="2e57f-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2e57f-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2e57f-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2e57f-139">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2e57f-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2e57f-140">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="2e57f-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2e57f-141">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="2e57f-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="2e57f-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e57f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e57f-143">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="2e57f-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




