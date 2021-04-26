---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997977"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="a339b-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="a339b-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="a339b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a339b-105">This topic is not current.</span></span> <span data-ttu-id="a339b-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a339b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a339b-107">Gibt eine Absicht auf hoher Ebene für den Treiber für die Auf population von Fotodruckeinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="a339b-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="a339b-108">Diese Einstellungen behandeln die erwartete Ausgabequalität, die ein Benutzer beim Drucken von Fotos angeben kann.</span><span class="sxs-lookup"><span data-stu-id="a339b-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="a339b-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a339b-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="a339b-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a339b-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="a339b-111">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="a339b-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a339b-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a339b-112">Element Information</span></span>



| <span data-ttu-id="a339b-113">Name</span><span class="sxs-lookup"><span data-stu-id="a339b-113">Name</span></span> | <span data-ttu-id="a339b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a339b-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a339b-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a339b-115">Element Type</span></span> <br/>   | <span data-ttu-id="a339b-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="a339b-116">Feature</span></span><br/> |
| <span data-ttu-id="a339b-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a339b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a339b-118">Seite</span><span class="sxs-lookup"><span data-stu-id="a339b-118">Page</span></span><br/>    |
| <span data-ttu-id="a339b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a339b-119">Notes</span></span> <br/>          | <span data-ttu-id="a339b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="a339b-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a339b-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a339b-121">Structural Content</span></span>

<span data-ttu-id="a339b-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="a339b-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="a339b-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a339b-123">Structure Variables</span></span>

<span data-ttu-id="a339b-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a339b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a339b-125">Name</span><span class="sxs-lookup"><span data-stu-id="a339b-125">Name</span></span>                               | <span data-ttu-id="a339b-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a339b-126">Data type</span></span>         | <span data-ttu-id="a339b-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="a339b-127">Unit</span></span>                  | <span data-ttu-id="a339b-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a339b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a339b-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a339b-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a339b-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a339b-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a339b-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a339b-131">string</span></span><br/> | <span data-ttu-id="a339b-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a339b-132">characters</span></span><br/> | <span data-ttu-id="a339b-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a339b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a339b-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a339b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a339b-135">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="a339b-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a339b-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a339b-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a339b-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a339b-137">string</span></span><br/> | <span data-ttu-id="a339b-138">–</span><span class="sxs-lookup"><span data-stu-id="a339b-138">n/a</span></span><br/>        | <span data-ttu-id="a339b-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a339b-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a339b-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a339b-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a339b-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a339b-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a339b-142">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="a339b-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a339b-143">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a339b-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="a339b-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a339b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a339b-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a339b-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




