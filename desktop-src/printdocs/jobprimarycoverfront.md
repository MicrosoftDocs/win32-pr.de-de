---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 270b16f6-677c-430a-aa69-1b5c6dfd3ba4
title: Jobprimarycoverfront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15d6f4f5095dfd4a980751c62d25997726d076d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219109"
---
# <a name="jobprimarycoverfront"></a><span data-ttu-id="0bc45-104">Jobprimarycoverfront</span><span class="sxs-lookup"><span data-stu-id="0bc45-104">JobPrimaryCoverFront</span></span>

<span data-ttu-id="0bc45-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0bc45-105">This topic is not current.</span></span> <span data-ttu-id="0bc45-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0bc45-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0bc45-107">Beschreibt das Deck Blatt "Front (Anfang)".</span><span class="sxs-lookup"><span data-stu-id="0bc45-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="0bc45-108">Der gesamte Auftrag verfügt über ein einzelnes primär Blatt.</span><span class="sxs-lookup"><span data-stu-id="0bc45-108">The entire job will have a single primary sheet.</span></span> <span data-ttu-id="0bc45-109">Das Deckblatt sollte auf der Seite PageMediaSize und PageMediaType gedruckt werden, die für die erste Seite des Auftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0bc45-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the job.</span></span> <span data-ttu-id="0bc45-110">Das Deck Blatt sollte in Verarbeitungsoptionen (z. b. jobduplexalldocumentscontiguron, jobnupalldocumentscontiguron) integriert werden, wie in der angegebenen Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="0bc45-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="0bc45-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0bc45-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0bc45-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0bc45-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0bc45-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0bc45-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0bc45-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0bc45-114">Element Information</span></span>



| <span data-ttu-id="0bc45-115">Name</span><span class="sxs-lookup"><span data-stu-id="0bc45-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc45-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0bc45-116">Element Type</span></span> <br/>   | <span data-ttu-id="0bc45-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="0bc45-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0bc45-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="0bc45-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0bc45-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0bc45-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0bc45-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bc45-120">Notes</span></span> <br/>          | <span data-ttu-id="0bc45-121">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="0bc45-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="0bc45-122">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0bc45-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="0bc45-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0bc45-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="0bc45-124">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0bc45-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="0bc45-125">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="0bc45-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0bc45-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0bc45-126">Structural Content</span></span>

<span data-ttu-id="0bc45-127">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="0bc45-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0bc45-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0bc45-128">Structure Variables</span></span>

<span data-ttu-id="0bc45-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0bc45-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0bc45-130">Name</span><span class="sxs-lookup"><span data-stu-id="0bc45-130">Name</span></span>                               | <span data-ttu-id="0bc45-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0bc45-131">Data type</span></span>         | <span data-ttu-id="0bc45-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="0bc45-132">Unit</span></span>           | <span data-ttu-id="0bc45-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0bc45-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0bc45-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0bc45-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0bc45-135">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="0bc45-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0bc45-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bc45-136">string</span></span><br/> | <span data-ttu-id="0bc45-137">–</span><span class="sxs-lookup"><span data-stu-id="0bc45-137">n/a</span></span><br/> | <span data-ttu-id="0bc45-138">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="0bc45-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0bc45-139">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="0bc45-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0bc45-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="0bc45-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0bc45-141">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="0bc45-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0bc45-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bc45-142">string</span></span><br/> | <span data-ttu-id="0bc45-143">–</span><span class="sxs-lookup"><span data-stu-id="0bc45-143">n/a</span></span><br/> | <span data-ttu-id="0bc45-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc45-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0bc45-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0bc45-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0bc45-146">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0bc45-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0bc45-147">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="0bc45-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0bc45-148">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="0bc45-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0bc45-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bc45-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc45-150">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0bc45-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




