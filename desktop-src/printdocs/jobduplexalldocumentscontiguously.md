---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: Jobduplexalldocumentszusammen hängend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106363059"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="56597-104">Jobduplexalldocumentszusammen hängend</span><span class="sxs-lookup"><span data-stu-id="56597-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="56597-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="56597-105">This topic is not current.</span></span> <span data-ttu-id="56597-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56597-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56597-107">Beschreibt die Duplex Merkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="56597-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="56597-108">Das Duplex Feature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="56597-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="56597-109">Alle Dokumente im Auftrag werden zusammenhängend zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="56597-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="56597-110">Jobduplexalldocumentscontiguron und DocumentDuplex schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="56597-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="56597-111">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="56597-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="56597-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56597-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56597-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="56597-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="56597-114">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="56597-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="56597-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56597-115">Element Information</span></span>



| <span data-ttu-id="56597-116">Name</span><span class="sxs-lookup"><span data-stu-id="56597-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="56597-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="56597-117">Element Type</span></span> <br/>   | <span data-ttu-id="56597-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="56597-118">Feature</span></span><br/> |
| <span data-ttu-id="56597-119">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="56597-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56597-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="56597-120">Job</span></span><br/>     |
| <span data-ttu-id="56597-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56597-121">Notes</span></span> <br/>          | <span data-ttu-id="56597-122">Keine</span><span class="sxs-lookup"><span data-stu-id="56597-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="56597-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="56597-123">Structural Content</span></span>

<span data-ttu-id="56597-124">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="56597-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="56597-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="56597-125">Structure Variables</span></span>

<span data-ttu-id="56597-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="56597-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56597-127">Name</span><span class="sxs-lookup"><span data-stu-id="56597-127">Name</span></span>                               | <span data-ttu-id="56597-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="56597-128">Data type</span></span>         | <span data-ttu-id="56597-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="56597-129">Unit</span></span>                  | <span data-ttu-id="56597-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="56597-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="56597-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56597-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56597-132">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="56597-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="56597-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56597-133">string</span></span><br/> | <span data-ttu-id="56597-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="56597-134">characters</span></span><br/> | <span data-ttu-id="56597-135">Gültiger voll qualifizierter Name, wie durch definiert https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="56597-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="56597-136">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="56597-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="56597-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="56597-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="56597-138">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="56597-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="56597-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56597-139">string</span></span><br/> | <span data-ttu-id="56597-140">–</span><span class="sxs-lookup"><span data-stu-id="56597-140">n/a</span></span><br/>        | <span data-ttu-id="56597-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="56597-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="56597-142">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="56597-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="56597-143">\_Duplexmodevalue\_</span><span class="sxs-lookup"><span data-stu-id="56597-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="56597-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56597-144">string</span></span><br/> | <span data-ttu-id="56597-145">–</span><span class="sxs-lookup"><span data-stu-id="56597-145">n/a</span></span><br/>        | <span data-ttu-id="56597-146">Automatisch, manuell.</span><span class="sxs-lookup"><span data-stu-id="56597-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="56597-147">Definiert den Duplex Modus.</span><span class="sxs-lookup"><span data-stu-id="56597-147">Defines the duplex mode.</span></span> <span data-ttu-id="56597-148">Automatischer Duplex Vorgang wird von der Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56597-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="56597-149">Manuelles Duplexing wird von Software und Benutzer durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="56597-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="56597-150">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="56597-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="56597-151">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="56597-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="56597-152">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="56597-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="56597-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56597-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56597-154">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="56597-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




