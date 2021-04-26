---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959bbddbfa06e47fe2bc744af3ead0a72b13af7b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998417"
---
# <a name="documentduplex"></a><span data-ttu-id="efa18-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="efa18-104">DocumentDuplex</span></span>

<span data-ttu-id="efa18-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="efa18-105">This topic is not current.</span></span> <span data-ttu-id="efa18-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="efa18-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="efa18-107">Beschreibt die Duplexmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="efa18-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="efa18-108">Das Duplexfeature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="efa18-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="efa18-109">Jedes Dokument ist separat duplexed.</span><span class="sxs-lookup"><span data-stu-id="efa18-109">Each document is duplexed separately.</span></span> <span data-ttu-id="efa18-110">DocumentDuplex und JobDuplexAllDocumentsContiguously schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="efa18-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="efa18-111">Es liegt an dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="efa18-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="efa18-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="efa18-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="efa18-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="efa18-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="efa18-114">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="efa18-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="efa18-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="efa18-115">Element Information</span></span>



| <span data-ttu-id="efa18-116">Name</span><span class="sxs-lookup"><span data-stu-id="efa18-116">Name</span></span> | <span data-ttu-id="efa18-117">Wert</span><span class="sxs-lookup"><span data-stu-id="efa18-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="efa18-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="efa18-118">Element Type</span></span> <br/>   | <span data-ttu-id="efa18-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="efa18-119">Feature</span></span><br/>  |
| <span data-ttu-id="efa18-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="efa18-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="efa18-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="efa18-121">Document</span></span><br/> |
| <span data-ttu-id="efa18-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="efa18-122">Notes</span></span> <br/>          | <span data-ttu-id="efa18-123">Keine</span><span class="sxs-lookup"><span data-stu-id="efa18-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="efa18-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="efa18-124">Structural Content</span></span>

<span data-ttu-id="efa18-125">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="efa18-125">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="efa18-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="efa18-126">Structure Variables</span></span>

<span data-ttu-id="efa18-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efa18-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="efa18-128">Name</span><span class="sxs-lookup"><span data-stu-id="efa18-128">Name</span></span>                               | <span data-ttu-id="efa18-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="efa18-129">Data type</span></span>         | <span data-ttu-id="efa18-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="efa18-130">Unit</span></span>                  | <span data-ttu-id="efa18-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="efa18-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="efa18-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="efa18-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa18-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="efa18-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="efa18-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efa18-134">string</span></span><br/> | <span data-ttu-id="efa18-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="efa18-135">characters</span></span><br/> | <span data-ttu-id="efa18-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="efa18-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="efa18-137">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="efa18-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="efa18-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="efa18-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="efa18-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="efa18-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="efa18-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efa18-140">string</span></span><br/> | <span data-ttu-id="efa18-141">–</span><span class="sxs-lookup"><span data-stu-id="efa18-141">n/a</span></span><br/>        | <span data-ttu-id="efa18-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="efa18-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="efa18-143">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="efa18-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="efa18-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="efa18-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="efa18-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efa18-145">string</span></span><br/> | <span data-ttu-id="efa18-146">–</span><span class="sxs-lookup"><span data-stu-id="efa18-146">n/a</span></span><br/>        | <span data-ttu-id="efa18-147">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="efa18-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="efa18-148">Definiert den Duplexmodus.</span><span class="sxs-lookup"><span data-stu-id="efa18-148">Defines the duplex mode.</span></span> <span data-ttu-id="efa18-149">Automatischer Duplexvorgang wird von Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efa18-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="efa18-150">Das manuelle Duplexing wird von Software und dem Benutzer durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="efa18-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="efa18-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="efa18-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="efa18-152">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="efa18-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="efa18-153">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="efa18-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="efa18-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efa18-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa18-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="efa18-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




