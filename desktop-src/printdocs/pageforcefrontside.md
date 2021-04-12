---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: Pageforcefrontside
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e357cf59bca455102f6ca29bd66bc09455ee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219104"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="11ae5-104">Pageforcefrontside</span><span class="sxs-lookup"><span data-stu-id="11ae5-104">PageForceFrontSide</span></span>

<span data-ttu-id="11ae5-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="11ae5-105">This topic is not current.</span></span> <span data-ttu-id="11ae5-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11ae5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11ae5-107">Erzwingt, dass die Ausgabe an der Vorderseite eines Medien Blatts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="11ae5-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="11ae5-108">Relevant für Medien Blätter mit unterschiedlichen Oberflächen auf jeder Seite.</span><span class="sxs-lookup"><span data-stu-id="11ae5-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="11ae5-109">In Fällen, in denen dieses Feature mit Verarbeitungsoptionen (z. b. DocumentDuplex) beeinträchtigt wird, hat pageforcefrontside Vorrang vor der jeweiligen Seite, auf die die Funktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="11ae5-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="11ae5-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="11ae5-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="11ae5-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="11ae5-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="11ae5-112">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="11ae5-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="11ae5-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="11ae5-113">Element Information</span></span>



| <span data-ttu-id="11ae5-114">Name</span><span class="sxs-lookup"><span data-stu-id="11ae5-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="11ae5-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="11ae5-115">Element Type</span></span> <br/>   | <span data-ttu-id="11ae5-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="11ae5-116">Feature</span></span><br/> |
| <span data-ttu-id="11ae5-117">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="11ae5-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11ae5-118">Seite</span><span class="sxs-lookup"><span data-stu-id="11ae5-118">Page</span></span><br/>    |
| <span data-ttu-id="11ae5-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11ae5-119">Notes</span></span> <br/>          | <span data-ttu-id="11ae5-120">Keine</span><span class="sxs-lookup"><span data-stu-id="11ae5-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="11ae5-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="11ae5-121">Structural Content</span></span>

<span data-ttu-id="11ae5-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="11ae5-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="11ae5-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="11ae5-123">Structure Variables</span></span>

<span data-ttu-id="11ae5-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="11ae5-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11ae5-125">Name</span><span class="sxs-lookup"><span data-stu-id="11ae5-125">Name</span></span>                               | <span data-ttu-id="11ae5-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="11ae5-126">Data type</span></span>         | <span data-ttu-id="11ae5-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="11ae5-127">Unit</span></span>                  | <span data-ttu-id="11ae5-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="11ae5-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="11ae5-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11ae5-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="11ae5-130">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="11ae5-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="11ae5-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11ae5-131">string</span></span><br/> | <span data-ttu-id="11ae5-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="11ae5-132">characters</span></span><br/> | <span data-ttu-id="11ae5-133">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="11ae5-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="11ae5-134">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="11ae5-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="11ae5-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="11ae5-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="11ae5-136">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="11ae5-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="11ae5-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11ae5-137">string</span></span><br/> | <span data-ttu-id="11ae5-138">–</span><span class="sxs-lookup"><span data-stu-id="11ae5-138">n/a</span></span><br/>        | <span data-ttu-id="11ae5-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="11ae5-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="11ae5-140">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="11ae5-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="11ae5-141">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="11ae5-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="11ae5-142">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="11ae5-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="11ae5-143">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="11ae5-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="11ae5-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11ae5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ae5-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="11ae5-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




