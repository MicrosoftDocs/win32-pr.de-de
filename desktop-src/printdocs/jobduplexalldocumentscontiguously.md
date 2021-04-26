---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998217"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="aec46-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="aec46-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="aec46-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="aec46-105">This topic is not current.</span></span> <span data-ttu-id="aec46-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="aec46-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aec46-107">Beschreibt die Duplexmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="aec46-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="aec46-108">Das Duplexfeature ermöglicht das Drucken auf beiden Seiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="aec46-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="aec46-109">Alle Dokumente im Auftrag werden zusammenhängend miteinander verduplext.</span><span class="sxs-lookup"><span data-stu-id="aec46-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="aec46-110">JobDuplexAllDocumentsContiguously und DocumentDuplex schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="aec46-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="aec46-111">Der Treiber muss die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aec46-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="aec46-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="aec46-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aec46-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="aec46-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aec46-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="aec46-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aec46-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="aec46-115">Element Information</span></span>



| <span data-ttu-id="aec46-116">Name</span><span class="sxs-lookup"><span data-stu-id="aec46-116">Name</span></span> | <span data-ttu-id="aec46-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aec46-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="aec46-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="aec46-118">Element Type</span></span> <br/>   | <span data-ttu-id="aec46-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="aec46-119">Feature</span></span><br/> |
| <span data-ttu-id="aec46-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="aec46-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aec46-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="aec46-121">Job</span></span><br/>     |
| <span data-ttu-id="aec46-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aec46-122">Notes</span></span> <br/>          | <span data-ttu-id="aec46-123">Keine</span><span class="sxs-lookup"><span data-stu-id="aec46-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="aec46-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="aec46-124">Structural Content</span></span>

<span data-ttu-id="aec46-125">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="aec46-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="aec46-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="aec46-126">Structure Variables</span></span>

<span data-ttu-id="aec46-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="aec46-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aec46-128">Name</span><span class="sxs-lookup"><span data-stu-id="aec46-128">Name</span></span>                               | <span data-ttu-id="aec46-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aec46-129">Data type</span></span>         | <span data-ttu-id="aec46-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="aec46-130">Unit</span></span>                  | <span data-ttu-id="aec46-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="aec46-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="aec46-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="aec46-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec46-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="aec46-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="aec46-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="aec46-134">string</span></span><br/> | <span data-ttu-id="aec46-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="aec46-135">characters</span></span><br/> | <span data-ttu-id="aec46-136">Gültiger vollqualifizierter Name, wie durch https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname definiert.</span><span class="sxs-lookup"><span data-stu-id="aec46-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="aec46-137">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="aec46-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aec46-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="aec46-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="aec46-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aec46-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="aec46-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="aec46-140">string</span></span><br/> | <span data-ttu-id="aec46-141">–</span><span class="sxs-lookup"><span data-stu-id="aec46-141">n/a</span></span><br/>        | <span data-ttu-id="aec46-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="aec46-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="aec46-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="aec46-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="aec46-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="aec46-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="aec46-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="aec46-145">string</span></span><br/> | <span data-ttu-id="aec46-146">–</span><span class="sxs-lookup"><span data-stu-id="aec46-146">n/a</span></span><br/>        | <span data-ttu-id="aec46-147">Automatisch, Manuell.</span><span class="sxs-lookup"><span data-stu-id="aec46-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="aec46-148">Definiert den Duplexmodus.</span><span class="sxs-lookup"><span data-stu-id="aec46-148">Defines the duplex mode.</span></span> <span data-ttu-id="aec46-149">Die automatische Duplexduplex wird von der Hardware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aec46-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="aec46-150">Manuelles Duplexing wird von Software und dem Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aec46-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aec46-151">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="aec46-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aec46-152">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="aec46-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aec46-153">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="aec46-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="aec46-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aec46-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec46-155">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="aec46-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




