---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: Joboptimaldestinationcolorprofile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103961265"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="978c2-104">Joboptimaldestinationcolorprofile</span><span class="sxs-lookup"><span data-stu-id="978c2-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="978c2-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="978c2-105">This topic is not current.</span></span> <span data-ttu-id="978c2-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="978c2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="978c2-107">Gibt das optimale Farbprofil an, wenn die aktuelle Gerätekonfiguration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="978c2-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="978c2-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="978c2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="978c2-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="978c2-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="978c2-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="978c2-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="978c2-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="978c2-111">Element Information</span></span>



| <span data-ttu-id="978c2-112">Name</span><span class="sxs-lookup"><span data-stu-id="978c2-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="978c2-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="978c2-113">Element Type</span></span> <br/>   | <span data-ttu-id="978c2-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="978c2-114">Property</span></span><br/> |
| <span data-ttu-id="978c2-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="978c2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="978c2-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="978c2-116">Job</span></span><br/>      |
| <span data-ttu-id="978c2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="978c2-117">Notes</span></span> <br/>          | <span data-ttu-id="978c2-118">Keine</span><span class="sxs-lookup"><span data-stu-id="978c2-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="978c2-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="978c2-119">Structural Content</span></span>

<span data-ttu-id="978c2-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="978c2-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="978c2-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="978c2-121">Structure Variables</span></span>

<span data-ttu-id="978c2-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="978c2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="978c2-123">Name</span><span class="sxs-lookup"><span data-stu-id="978c2-123">Name</span></span>                            | <span data-ttu-id="978c2-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="978c2-124">Data type</span></span>         | <span data-ttu-id="978c2-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="978c2-125">Unit</span></span>           | <span data-ttu-id="978c2-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="978c2-126">Supported values</span></span>          | <span data-ttu-id="978c2-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="978c2-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="978c2-128">\_Profilevalue\_</span><span class="sxs-lookup"><span data-stu-id="978c2-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="978c2-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="978c2-129">string</span></span><br/> | <span data-ttu-id="978c2-130">–</span><span class="sxs-lookup"><span data-stu-id="978c2-130">n/a</span></span><br/> | <span data-ttu-id="978c2-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="978c2-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="978c2-132">Gibt das Farbprofil an.</span><span class="sxs-lookup"><span data-stu-id="978c2-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="978c2-133">\_Pfadwert\_</span><span class="sxs-lookup"><span data-stu-id="978c2-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="978c2-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="978c2-134">string</span></span><br/> | <span data-ttu-id="978c2-135">–</span><span class="sxs-lookup"><span data-stu-id="978c2-135">n/a</span></span><br/> | <span data-ttu-id="978c2-136">–</span><span class="sxs-lookup"><span data-stu-id="978c2-136">n/a</span></span><br/>            | <span data-ttu-id="978c2-137">Gibt den Dateipfad zum Profil an.</span><span class="sxs-lookup"><span data-stu-id="978c2-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="978c2-138">\_Profiledatavalue\_</span><span class="sxs-lookup"><span data-stu-id="978c2-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="978c2-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="978c2-139">string</span></span><br/> | <span data-ttu-id="978c2-140">–</span><span class="sxs-lookup"><span data-stu-id="978c2-140">n/a</span></span><br/> | <span data-ttu-id="978c2-141">–</span><span class="sxs-lookup"><span data-stu-id="978c2-141">n/a</span></span><br/>            | <span data-ttu-id="978c2-142">Enthält Profildaten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="978c2-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="978c2-143">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="978c2-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="978c2-144">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="978c2-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="978c2-145">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="978c2-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="978c2-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="978c2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="978c2-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="978c2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




