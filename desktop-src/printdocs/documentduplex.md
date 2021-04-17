---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219103"
---
# <a name="documentduplex"></a><span data-ttu-id="ac7cc-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="ac7cc-104">DocumentDuplex</span></span>

<span data-ttu-id="ac7cc-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-105">This topic is not current.</span></span> <span data-ttu-id="ac7cc-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ac7cc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ac7cc-107">Beschreibt die Duplex Merkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="ac7cc-108">Das Duplex Feature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="ac7cc-109">Jedes Dokument wird separat duplext.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-109">Each document is duplexed separately.</span></span> <span data-ttu-id="ac7cc-110">DocumentDuplex und jobduplexalldocumentsangrenzenden schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="ac7cc-111">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="ac7cc-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ac7cc-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ac7cc-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ac7cc-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ac7cc-114">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ac7cc-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ac7cc-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ac7cc-115">Element Information</span></span>



| <span data-ttu-id="ac7cc-116">Name</span><span class="sxs-lookup"><span data-stu-id="ac7cc-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="ac7cc-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ac7cc-117">Element Type</span></span> <br/>   | <span data-ttu-id="ac7cc-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="ac7cc-118">Feature</span></span><br/>  |
| <span data-ttu-id="ac7cc-119">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="ac7cc-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ac7cc-120">Dokument</span><span class="sxs-lookup"><span data-stu-id="ac7cc-120">Document</span></span><br/> |
| <span data-ttu-id="ac7cc-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac7cc-121">Notes</span></span> <br/>          | <span data-ttu-id="ac7cc-122">Keine</span><span class="sxs-lookup"><span data-stu-id="ac7cc-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ac7cc-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ac7cc-123">Structural Content</span></span>

<span data-ttu-id="ac7cc-124">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac7cc-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="structure-variables"></a><span data-ttu-id="ac7cc-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="ac7cc-125">Structure Variables</span></span>

<span data-ttu-id="ac7cc-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ac7cc-127">Name</span><span class="sxs-lookup"><span data-stu-id="ac7cc-127">Name</span></span>                               | <span data-ttu-id="ac7cc-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ac7cc-128">Data type</span></span>         | <span data-ttu-id="ac7cc-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="ac7cc-129">Unit</span></span>                  | <span data-ttu-id="ac7cc-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="ac7cc-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ac7cc-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ac7cc-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7cc-132">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="ac7cc-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ac7cc-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ac7cc-133">string</span></span><br/> | <span data-ttu-id="ac7cc-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="ac7cc-134">characters</span></span><br/> | <span data-ttu-id="ac7cc-135">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ac7cc-136">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ac7cc-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="ac7cc-138">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="ac7cc-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ac7cc-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ac7cc-139">string</span></span><br/> | <span data-ttu-id="ac7cc-140">–</span><span class="sxs-lookup"><span data-stu-id="ac7cc-140">n/a</span></span><br/>        | <span data-ttu-id="ac7cc-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="ac7cc-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ac7cc-142">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="ac7cc-143">\_Duplexmodevalue\_</span><span class="sxs-lookup"><span data-stu-id="ac7cc-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="ac7cc-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ac7cc-144">string</span></span><br/> | <span data-ttu-id="ac7cc-145">–</span><span class="sxs-lookup"><span data-stu-id="ac7cc-145">n/a</span></span><br/>        | <span data-ttu-id="ac7cc-146">Automatisch, manuell.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="ac7cc-147">Definiert den Duplex Modus.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-147">Defines the duplex mode.</span></span> <span data-ttu-id="ac7cc-148">Automatischer Duplex Vorgang wird von der Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="ac7cc-149">Manuelles Duplexing wird von Software und Benutzer durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ac7cc-150">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ac7cc-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ac7cc-151">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="ac7cc-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ac7cc-152">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="ac7cc-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="related-topics"></a><span data-ttu-id="ac7cc-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac7cc-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac7cc-154">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="ac7cc-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




