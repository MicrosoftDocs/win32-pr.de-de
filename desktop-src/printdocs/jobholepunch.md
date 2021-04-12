---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: Jobholepunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bcd709c6115a9f4af3084c28ca047950d1b81fd
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219092"
---
# <a name="jobholepunch"></a><span data-ttu-id="df253-104">Jobholepunch</span><span class="sxs-lookup"><span data-stu-id="df253-104">JobHolePunch</span></span>

<span data-ttu-id="df253-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="df253-105">This topic is not current.</span></span> <span data-ttu-id="df253-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="df253-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df253-107">Beschreibt die Eigenschaften des boxthreads der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="df253-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="df253-108">Alle Dokumente werden gleichzeitig gepunktet.</span><span class="sxs-lookup"><span data-stu-id="df253-108">All documents are punched together.</span></span> <span data-ttu-id="df253-109">Die jobholepunch-und documentholepunch-Schlüsselwörter schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="df253-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="df253-110">Beide sollten nicht gleichzeitig in einem PrintTicket-oder Druckfunktionen-Dokument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="df253-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="df253-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df253-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="df253-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="df253-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="df253-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="df253-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="df253-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df253-114">Element Information</span></span>



| <span data-ttu-id="df253-115">Name</span><span class="sxs-lookup"><span data-stu-id="df253-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df253-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="df253-116">Element Type</span></span> <br/>   | <span data-ttu-id="df253-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="df253-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="df253-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="df253-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="df253-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="df253-119">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="df253-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="df253-120">Notes</span></span> <br/>          | <span data-ttu-id="df253-121">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="df253-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="df253-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="df253-122">Structural Content</span></span>

<span data-ttu-id="df253-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="df253-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="df253-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="df253-124">Structure Variables</span></span>

<span data-ttu-id="df253-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="df253-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="df253-126">Name</span><span class="sxs-lookup"><span data-stu-id="df253-126">Name</span></span>                               | <span data-ttu-id="df253-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="df253-127">Data type</span></span>         | <span data-ttu-id="df253-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="df253-128">Unit</span></span>                  | <span data-ttu-id="df253-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="df253-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="df253-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="df253-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="df253-131">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="df253-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="df253-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df253-132">string</span></span><br/> | <span data-ttu-id="df253-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="df253-133">characters</span></span><br/> | <span data-ttu-id="df253-134">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="df253-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="df253-135">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="df253-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="df253-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="df253-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="df253-137">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="df253-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="df253-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df253-138">string</span></span><br/> | <span data-ttu-id="df253-139">–</span><span class="sxs-lookup"><span data-stu-id="df253-139">n/a</span></span><br/>        | <span data-ttu-id="df253-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="df253-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="df253-141">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="df253-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="df253-142">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="df253-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="df253-143">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="df253-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="df253-144">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="df253-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="df253-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df253-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df253-146">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="df253-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




