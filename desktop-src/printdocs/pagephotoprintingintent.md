---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: Pagephotoprintingintent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3985d6f21d0d7731d1c08d080d64a4948b58196d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104530602"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="a9b1d-104">Pagephotoprintingintent</span><span class="sxs-lookup"><span data-stu-id="a9b1d-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="a9b1d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-105">This topic is not current.</span></span> <span data-ttu-id="a9b1d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a9b1d-107">Gibt eine allgemeine Absicht des Treibers für die Auffüllung von Foto Druckeinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="a9b1d-108">Diese Einstellungen befassen sich mit der erwarteten Ausgabequalität, die ein Benutzer beim Drucken von Fotos angeben kann.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="a9b1d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a9b1d-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="a9b1d-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a9b1d-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="a9b1d-111">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="a9b1d-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a9b1d-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a9b1d-112">Element Information</span></span>



| <span data-ttu-id="a9b1d-113">Name</span><span class="sxs-lookup"><span data-stu-id="a9b1d-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="a9b1d-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a9b1d-114">Element Type</span></span> <br/>   | <span data-ttu-id="a9b1d-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="a9b1d-115">Feature</span></span><br/> |
| <span data-ttu-id="a9b1d-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="a9b1d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a9b1d-117">Seite</span><span class="sxs-lookup"><span data-stu-id="a9b1d-117">Page</span></span><br/>    |
| <span data-ttu-id="a9b1d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9b1d-118">Notes</span></span> <br/>          | <span data-ttu-id="a9b1d-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a9b1d-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a9b1d-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a9b1d-120">Structural Content</span></span>

<span data-ttu-id="a9b1d-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a9b1d-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a9b1d-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a9b1d-122">Structure Variables</span></span>

<span data-ttu-id="a9b1d-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a9b1d-124">Name</span><span class="sxs-lookup"><span data-stu-id="a9b1d-124">Name</span></span>                               | <span data-ttu-id="a9b1d-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a9b1d-125">Data type</span></span>         | <span data-ttu-id="a9b1d-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="a9b1d-126">Unit</span></span>                  | <span data-ttu-id="a9b1d-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a9b1d-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a9b1d-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a9b1d-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a9b1d-129">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="a9b1d-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a9b1d-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a9b1d-130">string</span></span><br/> | <span data-ttu-id="a9b1d-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a9b1d-131">characters</span></span><br/> | <span data-ttu-id="a9b1d-132">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a9b1d-133">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a9b1d-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a9b1d-135">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="a9b1d-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a9b1d-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a9b1d-136">string</span></span><br/> | <span data-ttu-id="a9b1d-137">–</span><span class="sxs-lookup"><span data-stu-id="a9b1d-137">n/a</span></span><br/>        | <span data-ttu-id="a9b1d-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a9b1d-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a9b1d-139">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a9b1d-140">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a9b1d-141">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a9b1d-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a9b1d-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a9b1d-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9b1d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b1d-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="a9b1d-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




