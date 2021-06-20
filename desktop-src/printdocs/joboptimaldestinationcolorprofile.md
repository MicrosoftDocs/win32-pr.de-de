---
description: Hier erfahren Sie mehr über das JobOptimalDestinationColorProfile-Element, das das optimale Farbprofil bei der aktuellen Gerätekonfiguration angibt.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408843"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="c960a-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="c960a-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="c960a-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c960a-104">This topic is not current.</span></span> <span data-ttu-id="c960a-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c960a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c960a-106">Gibt das optimale Farbprofil bei der aktuellen Gerätekonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c960a-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="c960a-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c960a-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c960a-108">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c960a-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c960a-109">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c960a-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c960a-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c960a-110">Element Information</span></span>



| <span data-ttu-id="c960a-111">Name</span><span class="sxs-lookup"><span data-stu-id="c960a-111">Name</span></span> | <span data-ttu-id="c960a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c960a-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="c960a-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c960a-113">Element Type</span></span> <br/>   | <span data-ttu-id="c960a-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c960a-114">Property</span></span><br/> |
| <span data-ttu-id="c960a-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c960a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c960a-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c960a-116">Job</span></span><br/>      |
| <span data-ttu-id="c960a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c960a-117">Notes</span></span> <br/>          | <span data-ttu-id="c960a-118">Keine</span><span class="sxs-lookup"><span data-stu-id="c960a-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="c960a-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c960a-119">Structural Content</span></span>

<span data-ttu-id="c960a-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="c960a-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c960a-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c960a-121">Structure Variables</span></span>

<span data-ttu-id="c960a-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c960a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c960a-123">Name</span><span class="sxs-lookup"><span data-stu-id="c960a-123">Name</span></span>                            | <span data-ttu-id="c960a-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c960a-124">Data type</span></span>         | <span data-ttu-id="c960a-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="c960a-125">Unit</span></span>           | <span data-ttu-id="c960a-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c960a-126">Supported values</span></span>          | <span data-ttu-id="c960a-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c960a-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="c960a-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="c960a-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="c960a-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c960a-129">string</span></span><br/> | <span data-ttu-id="c960a-130">–</span><span class="sxs-lookup"><span data-stu-id="c960a-130">n/a</span></span><br/> | <span data-ttu-id="c960a-131">RGB, RGB, RGB, C RGB</span><span class="sxs-lookup"><span data-stu-id="c960a-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="c960a-132">Gibt das Farbprofil an.</span><span class="sxs-lookup"><span data-stu-id="c960a-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="c960a-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="c960a-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="c960a-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c960a-134">string</span></span><br/> | <span data-ttu-id="c960a-135">–</span><span class="sxs-lookup"><span data-stu-id="c960a-135">n/a</span></span><br/> | <span data-ttu-id="c960a-136">–</span><span class="sxs-lookup"><span data-stu-id="c960a-136">n/a</span></span><br/>            | <span data-ttu-id="c960a-137">Gibt den Dateipfad zum Profil an.</span><span class="sxs-lookup"><span data-stu-id="c960a-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="c960a-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="c960a-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="c960a-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c960a-139">string</span></span><br/> | <span data-ttu-id="c960a-140">–</span><span class="sxs-lookup"><span data-stu-id="c960a-140">n/a</span></span><br/> | <span data-ttu-id="c960a-141">–</span><span class="sxs-lookup"><span data-stu-id="c960a-141">n/a</span></span><br/>            | <span data-ttu-id="c960a-142">Enthält Profildateninhalte.</span><span class="sxs-lookup"><span data-stu-id="c960a-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c960a-143">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c960a-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c960a-144">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="c960a-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c960a-145">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c960a-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c960a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c960a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c960a-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c960a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




