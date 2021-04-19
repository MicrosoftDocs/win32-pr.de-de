---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: Jobrollcutatendof Job
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eda63fe0d801bc1039af2c514c284440b1be47
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106353291"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="a28eb-104">Jobrollcutatendof Job</span><span class="sxs-lookup"><span data-stu-id="a28eb-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="a28eb-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a28eb-105">This topic is not current.</span></span> <span data-ttu-id="a28eb-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a28eb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a28eb-107">Beschreibt die Methode zum Durchführen eines rollpaper.</span><span class="sxs-lookup"><span data-stu-id="a28eb-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="a28eb-108">Der rollenvorgang sollte am Ende des Auftrags abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="a28eb-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="a28eb-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a28eb-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a28eb-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a28eb-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a28eb-111">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a28eb-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a28eb-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a28eb-112">Element Information</span></span>



| <span data-ttu-id="a28eb-113">Name</span><span class="sxs-lookup"><span data-stu-id="a28eb-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="a28eb-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a28eb-114">Element Type</span></span> <br/>   | <span data-ttu-id="a28eb-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="a28eb-115">Feature</span></span><br/> |
| <span data-ttu-id="a28eb-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="a28eb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a28eb-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a28eb-117">Job</span></span><br/>     |
| <span data-ttu-id="a28eb-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a28eb-118">Notes</span></span> <br/>          | <span data-ttu-id="a28eb-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a28eb-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a28eb-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a28eb-120">Structural Content</span></span>

<span data-ttu-id="a28eb-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a28eb-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
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

## <a name="structure-variables"></a><span data-ttu-id="a28eb-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a28eb-122">Structure Variables</span></span>

<span data-ttu-id="a28eb-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a28eb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a28eb-124">Name</span><span class="sxs-lookup"><span data-stu-id="a28eb-124">Name</span></span>                               | <span data-ttu-id="a28eb-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a28eb-125">Data type</span></span>         | <span data-ttu-id="a28eb-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="a28eb-126">Unit</span></span>                  | <span data-ttu-id="a28eb-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a28eb-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a28eb-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a28eb-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a28eb-129">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="a28eb-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a28eb-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a28eb-130">string</span></span><br/> | <span data-ttu-id="a28eb-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a28eb-131">characters</span></span><br/> | <span data-ttu-id="a28eb-132">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a28eb-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a28eb-133">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a28eb-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a28eb-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a28eb-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a28eb-135">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="a28eb-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a28eb-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a28eb-136">string</span></span><br/> | <span data-ttu-id="a28eb-137">–</span><span class="sxs-lookup"><span data-stu-id="a28eb-137">n/a</span></span><br/>        | <span data-ttu-id="a28eb-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a28eb-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a28eb-139">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a28eb-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a28eb-140">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a28eb-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a28eb-141">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a28eb-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a28eb-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a28eb-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="a28eb-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a28eb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a28eb-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="a28eb-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




