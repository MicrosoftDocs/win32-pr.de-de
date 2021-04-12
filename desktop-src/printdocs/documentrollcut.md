---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: Documentrollcut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219100"
---
# <a name="documentrollcut"></a><span data-ttu-id="f790b-104">Documentrollcut</span><span class="sxs-lookup"><span data-stu-id="f790b-104">DocumentRollCut</span></span>

<span data-ttu-id="f790b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f790b-105">This topic is not current.</span></span> <span data-ttu-id="f790b-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f790b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f790b-107">Beschreibt die Methode zum Durchführen eines rollpaper.</span><span class="sxs-lookup"><span data-stu-id="f790b-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="f790b-108">Jedes Dokument wird separat behandelt.</span><span class="sxs-lookup"><span data-stu-id="f790b-108">Each document is handled separately.</span></span> <span data-ttu-id="f790b-109">Die angegebenen Optionen beschreiben die verschiedenen Methoden für den Rollforward.</span><span class="sxs-lookup"><span data-stu-id="f790b-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="f790b-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f790b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f790b-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f790b-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f790b-112">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f790b-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f790b-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f790b-113">Element Information</span></span>



| <span data-ttu-id="f790b-114">Name</span><span class="sxs-lookup"><span data-stu-id="f790b-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="f790b-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f790b-115">Element Type</span></span> <br/>   | <span data-ttu-id="f790b-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="f790b-116">Feature</span></span><br/>  |
| <span data-ttu-id="f790b-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f790b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f790b-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="f790b-118">Document</span></span><br/> |
| <span data-ttu-id="f790b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f790b-119">Notes</span></span> <br/>          | <span data-ttu-id="f790b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f790b-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f790b-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f790b-121">Structural Content</span></span>

<span data-ttu-id="f790b-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f790b-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="f790b-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="f790b-123">Structure Variables</span></span>

<span data-ttu-id="f790b-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f790b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f790b-125">Name</span><span class="sxs-lookup"><span data-stu-id="f790b-125">Name</span></span>                               | <span data-ttu-id="f790b-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f790b-126">Data type</span></span>         | <span data-ttu-id="f790b-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="f790b-127">Unit</span></span>                  | <span data-ttu-id="f790b-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="f790b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f790b-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f790b-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f790b-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="f790b-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f790b-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f790b-131">string</span></span><br/> | <span data-ttu-id="f790b-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="f790b-132">characters</span></span><br/> | <span data-ttu-id="f790b-133">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="f790b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f790b-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="f790b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f790b-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="f790b-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f790b-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="f790b-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f790b-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f790b-137">string</span></span><br/> | <span data-ttu-id="f790b-138">–</span><span class="sxs-lookup"><span data-stu-id="f790b-138">n/a</span></span><br/>        | <span data-ttu-id="f790b-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="f790b-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f790b-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f790b-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f790b-141">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f790b-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f790b-142">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="f790b-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f790b-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="f790b-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f790b-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f790b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f790b-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f790b-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




