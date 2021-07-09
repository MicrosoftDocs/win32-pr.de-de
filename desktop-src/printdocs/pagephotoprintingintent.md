---
description: Überprüfen Sie das Vom Benutzer konfigurierbare PagePhotoPrintingIntent-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548978"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="8751a-105">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="8751a-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="8751a-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8751a-106">This topic is not current.</span></span> <span data-ttu-id="8751a-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8751a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8751a-108">Gibt dem Treiber eine absichtsorientierte Absicht für die Auffüllung von Fotodruckeinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="8751a-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="8751a-109">Diese Einstellungen befassen sich mit der erwarteten Ausgabequalität, die ein Benutzer beim Drucken von Fotos angeben kann.</span><span class="sxs-lookup"><span data-stu-id="8751a-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="8751a-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8751a-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="8751a-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="8751a-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="8751a-112">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="8751a-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8751a-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8751a-113">Element Information</span></span>



| <span data-ttu-id="8751a-114">Name</span><span class="sxs-lookup"><span data-stu-id="8751a-114">Name</span></span> | <span data-ttu-id="8751a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8751a-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8751a-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8751a-116">Element Type</span></span> <br/>   | <span data-ttu-id="8751a-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="8751a-117">Feature</span></span><br/> |
| <span data-ttu-id="8751a-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8751a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8751a-119">Seite</span><span class="sxs-lookup"><span data-stu-id="8751a-119">Page</span></span><br/>    |
| <span data-ttu-id="8751a-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8751a-120">Notes</span></span> <br/>          | <span data-ttu-id="8751a-121">Keine</span><span class="sxs-lookup"><span data-stu-id="8751a-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="8751a-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="8751a-122">Structural Content</span></span>

<span data-ttu-id="8751a-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="8751a-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8751a-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8751a-124">Structure Variables</span></span>

<span data-ttu-id="8751a-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8751a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8751a-126">Name</span><span class="sxs-lookup"><span data-stu-id="8751a-126">Name</span></span>                               | <span data-ttu-id="8751a-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8751a-127">Data type</span></span>         | <span data-ttu-id="8751a-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="8751a-128">Unit</span></span>                  | <span data-ttu-id="8751a-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8751a-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8751a-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8751a-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8751a-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="8751a-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8751a-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8751a-132">string</span></span><br/> | <span data-ttu-id="8751a-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8751a-133">characters</span></span><br/> | <span data-ttu-id="8751a-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="8751a-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8751a-135">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8751a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8751a-136">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="8751a-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="8751a-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8751a-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8751a-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8751a-138">string</span></span><br/> | <span data-ttu-id="8751a-139">n/v</span><span class="sxs-lookup"><span data-stu-id="8751a-139">n/a</span></span><br/>        | <span data-ttu-id="8751a-140">True, False</span><span class="sxs-lookup"><span data-stu-id="8751a-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="8751a-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8751a-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8751a-142">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="8751a-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8751a-143">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="8751a-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8751a-144">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8751a-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8751a-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8751a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8751a-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8751a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




