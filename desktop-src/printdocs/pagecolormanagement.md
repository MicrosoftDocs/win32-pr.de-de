---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: Pagecolormanagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106363906"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="f0ec9-104">Pagecolormanagement</span><span class="sxs-lookup"><span data-stu-id="f0ec9-104">PageColorManagement</span></span>

<span data-ttu-id="f0ec9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-105">This topic is not current.</span></span> <span data-ttu-id="f0ec9-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f0ec9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f0ec9-107">Konfiguriert die Farbverwaltung für die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-107">Configures color management for the current page.</span></span> <span data-ttu-id="f0ec9-108">Dies wird im Shim-DM \_ ICMMethod Add System als automatisch betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="f0ec9-109">Beschreibt, welche Komponente die Farbverwaltung ausführen soll (d. h. Treiber).</span><span class="sxs-lookup"><span data-stu-id="f0ec9-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="f0ec9-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f0ec9-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f0ec9-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f0ec9-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f0ec9-112">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f0ec9-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f0ec9-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f0ec9-113">Element Information</span></span>



| <span data-ttu-id="f0ec9-114">Name</span><span class="sxs-lookup"><span data-stu-id="f0ec9-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="f0ec9-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f0ec9-115">Element Type</span></span> <br/>   | <span data-ttu-id="f0ec9-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="f0ec9-116">Feature</span></span><br/> |
| <span data-ttu-id="f0ec9-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f0ec9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f0ec9-118">Seite</span><span class="sxs-lookup"><span data-stu-id="f0ec9-118">Page</span></span><br/>    |
| <span data-ttu-id="f0ec9-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0ec9-119">Notes</span></span> <br/>          | <span data-ttu-id="f0ec9-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f0ec9-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="f0ec9-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f0ec9-121">Structural Content</span></span>

<span data-ttu-id="f0ec9-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f0ec9-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="f0ec9-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="f0ec9-123">Structure Variables</span></span>

<span data-ttu-id="f0ec9-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f0ec9-125">Name</span><span class="sxs-lookup"><span data-stu-id="f0ec9-125">Name</span></span>                               | <span data-ttu-id="f0ec9-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f0ec9-126">Data type</span></span>         | <span data-ttu-id="f0ec9-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="f0ec9-127">Unit</span></span>                  | <span data-ttu-id="f0ec9-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="f0ec9-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f0ec9-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f0ec9-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f0ec9-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="f0ec9-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f0ec9-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f0ec9-131">string</span></span><br/> | <span data-ttu-id="f0ec9-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="f0ec9-132">characters</span></span><br/> | <span data-ttu-id="f0ec9-133">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f0ec9-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f0ec9-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f0ec9-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="f0ec9-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f0ec9-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f0ec9-137">string</span></span><br/> | <span data-ttu-id="f0ec9-138">–</span><span class="sxs-lookup"><span data-stu-id="f0ec9-138">n/a</span></span><br/>        | <span data-ttu-id="f0ec9-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="f0ec9-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f0ec9-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f0ec9-141">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f0ec9-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f0ec9-142">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="f0ec9-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f0ec9-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="f0ec9-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f0ec9-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0ec9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ec9-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f0ec9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




