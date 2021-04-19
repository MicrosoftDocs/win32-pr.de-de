---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: Jobprimarybannersheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc44973b06dc99c86ca9d50717ca9bf2b6335fa
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106353290"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="8f215-104">Jobprimarybannersheet</span><span class="sxs-lookup"><span data-stu-id="8f215-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="8f215-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8f215-105">This topic is not current.</span></span> <span data-ttu-id="8f215-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f215-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f215-107">Beschreibt das Banner Blatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f215-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="8f215-108">Das Banner Blatt sollte auf der Standardseite PageMediaSize ausgegeben werden, und es wird der Standardwert PageMediaType verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f215-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="8f215-109">Das Banner Blatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="8f215-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="8f215-110">Dies bedeutet, dass alle Beendigungs-oder Verarbeitungsoptionen (z. b. jobduplexalldocumentscontiguron, JobStapleAllDocuments oder jobbindalldocuments) das Banner Blatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="8f215-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="8f215-111">Das Banner Blatt sollte als erstes Blatt des Auftrags auftreten.</span><span class="sxs-lookup"><span data-stu-id="8f215-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="8f215-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8f215-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f215-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8f215-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8f215-114">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8f215-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8f215-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8f215-115">Element Information</span></span>



| <span data-ttu-id="8f215-116">Name</span><span class="sxs-lookup"><span data-stu-id="8f215-116">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f215-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8f215-117">Element Type</span></span> <br/>   | <span data-ttu-id="8f215-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="8f215-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8f215-119">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="8f215-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f215-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="8f215-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8f215-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f215-121">Notes</span></span> <br/>          | <span data-ttu-id="8f215-122">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="8f215-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="8f215-123">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8f215-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="8f215-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="8f215-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="8f215-125">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8f215-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="8f215-126">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="8f215-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="8f215-127">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="8f215-127">Structural Content</span></span>

<span data-ttu-id="8f215-128">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="8f215-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="8f215-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="8f215-129">Structure Variables</span></span>

<span data-ttu-id="8f215-130">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f215-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f215-131">Name</span><span class="sxs-lookup"><span data-stu-id="8f215-131">Name</span></span>                               | <span data-ttu-id="8f215-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8f215-132">Data type</span></span>         | <span data-ttu-id="8f215-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="8f215-133">Unit</span></span>                  | <span data-ttu-id="8f215-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="8f215-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8f215-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8f215-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f215-136">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="8f215-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8f215-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8f215-137">string</span></span><br/> | <span data-ttu-id="8f215-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8f215-138">characters</span></span><br/> | <span data-ttu-id="8f215-139">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="8f215-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8f215-140">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="8f215-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8f215-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="8f215-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8f215-142">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="8f215-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8f215-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8f215-143">string</span></span><br/> | <span data-ttu-id="8f215-144">–</span><span class="sxs-lookup"><span data-stu-id="8f215-144">n/a</span></span><br/>        | <span data-ttu-id="8f215-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="8f215-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8f215-146">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8f215-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8f215-147">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8f215-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8f215-148">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="8f215-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8f215-149">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="8f215-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="8f215-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f215-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f215-151">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="8f215-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




