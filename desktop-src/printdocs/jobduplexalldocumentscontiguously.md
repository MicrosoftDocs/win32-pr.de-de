---
description: Erfahren Sie mehr über das JobDuplexAllDocumentsContiguously-Element, das die Duplexmerkmale der Ausgabe beschreibt.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a8911a4c62644bfc073a2a9c1dcfd67dad536a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408953"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="92f23-103">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="92f23-103">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="92f23-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="92f23-104">This topic is not current.</span></span> <span data-ttu-id="92f23-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="92f23-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92f23-106">Beschreibt die Duplexmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="92f23-106">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="92f23-107">Das Duplexfeature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="92f23-107">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="92f23-108">Alle Dokumente im Auftrag werden zusammenhängend miteinander verduplext.</span><span class="sxs-lookup"><span data-stu-id="92f23-108">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="92f23-109">JobDuplexAllDocumentsContiguously und DocumentDuplex schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="92f23-109">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="92f23-110">Der Treiber muss die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="92f23-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="92f23-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92f23-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92f23-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="92f23-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="92f23-113">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="92f23-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="92f23-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92f23-114">Element Information</span></span>



| <span data-ttu-id="92f23-115">Name</span><span class="sxs-lookup"><span data-stu-id="92f23-115">Name</span></span> | <span data-ttu-id="92f23-116">Wert</span><span class="sxs-lookup"><span data-stu-id="92f23-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="92f23-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="92f23-117">Element Type</span></span> <br/>   | <span data-ttu-id="92f23-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="92f23-118">Feature</span></span><br/> |
| <span data-ttu-id="92f23-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="92f23-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="92f23-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="92f23-120">Job</span></span><br/>     |
| <span data-ttu-id="92f23-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92f23-121">Notes</span></span> <br/>          | <span data-ttu-id="92f23-122">Keine</span><span class="sxs-lookup"><span data-stu-id="92f23-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="92f23-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="92f23-123">Structural Content</span></span>

<span data-ttu-id="92f23-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="92f23-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="92f23-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="92f23-125">Structure Variables</span></span>

<span data-ttu-id="92f23-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="92f23-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="92f23-127">Name</span><span class="sxs-lookup"><span data-stu-id="92f23-127">Name</span></span>                               | <span data-ttu-id="92f23-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="92f23-128">Data type</span></span>         | <span data-ttu-id="92f23-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="92f23-129">Unit</span></span>                  | <span data-ttu-id="92f23-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="92f23-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="92f23-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="92f23-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92f23-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="92f23-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="92f23-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92f23-133">string</span></span><br/> | <span data-ttu-id="92f23-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="92f23-134">characters</span></span><br/> | <span data-ttu-id="92f23-135">Gültiger vollqualifizierter Name gemäß der Definition von https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="92f23-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="92f23-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="92f23-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="92f23-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="92f23-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="92f23-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="92f23-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="92f23-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92f23-139">string</span></span><br/> | <span data-ttu-id="92f23-140">–</span><span class="sxs-lookup"><span data-stu-id="92f23-140">n/a</span></span><br/>        | <span data-ttu-id="92f23-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="92f23-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="92f23-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="92f23-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="92f23-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="92f23-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="92f23-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92f23-144">string</span></span><br/> | <span data-ttu-id="92f23-145">–</span><span class="sxs-lookup"><span data-stu-id="92f23-145">n/a</span></span><br/>        | <span data-ttu-id="92f23-146">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="92f23-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="92f23-147">Definiert den Duplexmodus.</span><span class="sxs-lookup"><span data-stu-id="92f23-147">Defines the duplex mode.</span></span> <span data-ttu-id="92f23-148">Automatischer Duplexvorgang wird von Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92f23-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="92f23-149">Das manuelle Duplexing wird von Software und dem Benutzer durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="92f23-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="92f23-150">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="92f23-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="92f23-151">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="92f23-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="92f23-152">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="92f23-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="92f23-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92f23-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f23-154">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="92f23-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




