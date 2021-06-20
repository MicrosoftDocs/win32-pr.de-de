---
description: Erfahren Sie mehr über das JobPrimaryCoverFront-Element, das das front-Coversheet beschreibt. Der gesamte Auftrag hat ein einzelnes primäres Blatt.
ms.assetid: 270b16f6-677c-430a-aa69-1b5c6dfd3ba4
title: JobPrimaryCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60aef4a70404ce6777b9bfe2848fddffa4e89d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408673"
---
# <a name="jobprimarycoverfront"></a><span data-ttu-id="c7ee5-104">JobPrimaryCoverFront</span><span class="sxs-lookup"><span data-stu-id="c7ee5-104">JobPrimaryCoverFront</span></span>

<span data-ttu-id="c7ee5-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-105">This topic is not current.</span></span> <span data-ttu-id="c7ee5-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c7ee5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7ee5-107">Beschreibt das Front-Cover-Blatt (Anfang).</span><span class="sxs-lookup"><span data-stu-id="c7ee5-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="c7ee5-108">Der gesamte Auftrag hat ein einzelnes primäres Blatt.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-108">The entire job will have a single primary sheet.</span></span> <span data-ttu-id="c7ee5-109">Das Titelblatt sollte auf der ersten Seite des Auftrags auf pageMediaSize und PageMediaType gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the job.</span></span> <span data-ttu-id="c7ee5-110">Das Coversheet sollte in Verarbeitungsoptionen (z. B. JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) integriert werden, wie in der angegebenen Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="c7ee5-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c7ee5-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7ee5-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c7ee5-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c7ee5-113">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c7ee5-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c7ee5-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c7ee5-114">Element Information</span></span>



| <span data-ttu-id="c7ee5-115">Name</span><span class="sxs-lookup"><span data-stu-id="c7ee5-115">Name</span></span> | <span data-ttu-id="c7ee5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c7ee5-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ee5-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c7ee5-117">Element Type</span></span> <br/>   | <span data-ttu-id="c7ee5-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="c7ee5-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c7ee5-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c7ee5-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7ee5-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c7ee5-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c7ee5-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7ee5-121">Notes</span></span> <br/>          | <span data-ttu-id="c7ee5-122">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c7ee5-123">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c7ee5-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c7ee5-125">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c7ee5-126">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c7ee5-127">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c7ee5-127">Structural Content</span></span>

<span data-ttu-id="c7ee5-128">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="c7ee5-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c7ee5-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c7ee5-129">Structure Variables</span></span>

<span data-ttu-id="c7ee5-130">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7ee5-131">Name</span><span class="sxs-lookup"><span data-stu-id="c7ee5-131">Name</span></span>                               | <span data-ttu-id="c7ee5-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c7ee5-132">Data type</span></span>         | <span data-ttu-id="c7ee5-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="c7ee5-133">Unit</span></span>           | <span data-ttu-id="c7ee5-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c7ee5-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c7ee5-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c7ee5-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c7ee5-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c7ee5-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c7ee5-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c7ee5-137">string</span></span><br/> | <span data-ttu-id="c7ee5-138">–</span><span class="sxs-lookup"><span data-stu-id="c7ee5-138">n/a</span></span><br/> | <span data-ttu-id="c7ee5-139">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c7ee5-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c7ee5-140">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c7ee5-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c7ee5-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c7ee5-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c7ee5-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c7ee5-143">string</span></span><br/> | <span data-ttu-id="c7ee5-144">–</span><span class="sxs-lookup"><span data-stu-id="c7ee5-144">n/a</span></span><br/> | <span data-ttu-id="c7ee5-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c7ee5-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c7ee5-146">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c7ee5-147">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c7ee5-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c7ee5-148">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="c7ee5-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c7ee5-149">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c7ee5-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c7ee5-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7ee5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7ee5-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c7ee5-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




