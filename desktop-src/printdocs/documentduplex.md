---
description: Erfahren Sie mehr über das DocumentDuplex-Element, das die Duplexmerkmale der Ausgabe beschreibt. Das Duplexfeature ermöglicht das Drucken auf beiden Seiten des Mediums.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ad8521835213594f10507ab6fd4b9cca24040
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409343"
---
# <a name="documentduplex"></a><span data-ttu-id="3fd8f-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="3fd8f-104">DocumentDuplex</span></span>

<span data-ttu-id="3fd8f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-105">This topic is not current.</span></span> <span data-ttu-id="3fd8f-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3fd8f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3fd8f-107">Beschreibt die Duplexmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="3fd8f-108">Das Duplexfeature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="3fd8f-109">Jedes Dokument ist separat duplexed.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-109">Each document is duplexed separately.</span></span> <span data-ttu-id="3fd8f-110">DocumentDuplex und JobDuplexAllDocumentsContiguously schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="3fd8f-111">Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="3fd8f-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3fd8f-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3fd8f-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3fd8f-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3fd8f-114">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3fd8f-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3fd8f-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3fd8f-115">Element Information</span></span>



| <span data-ttu-id="3fd8f-116">Name</span><span class="sxs-lookup"><span data-stu-id="3fd8f-116">Name</span></span> | <span data-ttu-id="3fd8f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd8f-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3fd8f-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3fd8f-118">Element Type</span></span> <br/>   | <span data-ttu-id="3fd8f-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="3fd8f-119">Feature</span></span><br/>  |
| <span data-ttu-id="3fd8f-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3fd8f-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3fd8f-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="3fd8f-121">Document</span></span><br/> |
| <span data-ttu-id="3fd8f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3fd8f-122">Notes</span></span> <br/>          | <span data-ttu-id="3fd8f-123">Keine</span><span class="sxs-lookup"><span data-stu-id="3fd8f-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3fd8f-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="3fd8f-124">Structural Content</span></span>

<span data-ttu-id="3fd8f-125">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="3fd8f-125">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3fd8f-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3fd8f-126">Structure Variables</span></span>

<span data-ttu-id="3fd8f-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3fd8f-128">Name</span><span class="sxs-lookup"><span data-stu-id="3fd8f-128">Name</span></span>                               | <span data-ttu-id="3fd8f-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3fd8f-129">Data type</span></span>         | <span data-ttu-id="3fd8f-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="3fd8f-130">Unit</span></span>                  | <span data-ttu-id="3fd8f-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3fd8f-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3fd8f-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3fd8f-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd8f-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3fd8f-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3fd8f-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3fd8f-134">string</span></span><br/> | <span data-ttu-id="3fd8f-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3fd8f-135">characters</span></span><br/> | <span data-ttu-id="3fd8f-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3fd8f-137">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3fd8f-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="3fd8f-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3fd8f-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3fd8f-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3fd8f-140">string</span></span><br/> | <span data-ttu-id="3fd8f-141">–</span><span class="sxs-lookup"><span data-stu-id="3fd8f-141">n/a</span></span><br/>        | <span data-ttu-id="3fd8f-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="3fd8f-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3fd8f-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="3fd8f-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="3fd8f-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="3fd8f-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3fd8f-145">string</span></span><br/> | <span data-ttu-id="3fd8f-146">–</span><span class="sxs-lookup"><span data-stu-id="3fd8f-146">n/a</span></span><br/>        | <span data-ttu-id="3fd8f-147">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="3fd8f-148">Definiert den Duplexmodus.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-148">Defines the duplex mode.</span></span> <span data-ttu-id="3fd8f-149">Die automatische Duplexduplex wird von der Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="3fd8f-150">Manuelles Duplexing wird von Der Software und dem Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3fd8f-151">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="3fd8f-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3fd8f-152">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="3fd8f-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3fd8f-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="3fd8f-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3fd8f-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3fd8f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fd8f-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3fd8f-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




