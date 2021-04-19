---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: Documentbannersheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac772fdbd9bf378716c42362dc1657a100f1231
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106353288"
---
# <a name="documentbannersheet"></a><span data-ttu-id="f8188-104">Documentbannersheet</span><span class="sxs-lookup"><span data-stu-id="f8188-104">DocumentBannerSheet</span></span>

<span data-ttu-id="f8188-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f8188-105">This topic is not current.</span></span> <span data-ttu-id="f8188-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f8188-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f8188-107">Beschreibt das Banner Blatt, das für ein bestimmtes Dokument ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8188-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="f8188-108">Das Banner Blatt sollte auf der Standardseite PageMediaSize ausgegeben werden. dabei wird der Standardwert PageMediaType verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8188-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="f8188-109">Das Banner Blatt sollte auch vom Rest des Dokuments isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="f8188-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="f8188-110">Dies bedeutet, dass das Banner Blatt bei allen Endoptionen für das Beenden oder Verarbeiten von Dokumenten (z. b. DocumentDuplex, DocumentStaple oder documentbinding) nicht enthalten sein sollte.</span><span class="sxs-lookup"><span data-stu-id="f8188-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="f8188-111">Das Banner Blatt ist möglicherweise nicht vom Rest des Auftrags isoliert.</span><span class="sxs-lookup"><span data-stu-id="f8188-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="f8188-112">Dies bedeutet, dass alle Auftrags Beendigungs-oder Verarbeitungsoptionen das Dokument Banner Blatt enthalten können.</span><span class="sxs-lookup"><span data-stu-id="f8188-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="f8188-113">Das Banner Blatt sollte als erstes Blatt des Dokuments angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8188-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="f8188-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f8188-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f8188-115">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f8188-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="f8188-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f8188-116">Element Information</span></span>



| <span data-ttu-id="f8188-117">Name</span><span class="sxs-lookup"><span data-stu-id="f8188-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8188-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f8188-118">Element Type</span></span> <br/>   | <span data-ttu-id="f8188-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="f8188-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f8188-120">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f8188-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f8188-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="f8188-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f8188-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8188-122">Notes</span></span> <br/>          | <span data-ttu-id="f8188-123">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="f8188-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="f8188-124">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="f8188-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="f8188-125">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="f8188-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="f8188-126">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f8188-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="f8188-127">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="f8188-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f8188-128">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f8188-128">Structural Content</span></span>

<span data-ttu-id="f8188-129">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f8188-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="f8188-130">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="f8188-130">Structure Variables</span></span>

<span data-ttu-id="f8188-131">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f8188-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f8188-132">Name</span><span class="sxs-lookup"><span data-stu-id="f8188-132">Name</span></span>                               | <span data-ttu-id="f8188-133">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f8188-133">Data type</span></span>         | <span data-ttu-id="f8188-134">Einheit</span><span class="sxs-lookup"><span data-stu-id="f8188-134">Unit</span></span>                   | <span data-ttu-id="f8188-135">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="f8188-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f8188-136">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f8188-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f8188-137">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="f8188-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f8188-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f8188-138">string</span></span><br/> | <span data-ttu-id="f8188-139">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="f8188-139">characters</span></span> <br/> | <span data-ttu-id="f8188-140">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="f8188-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f8188-141">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="f8188-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f8188-142">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="f8188-142">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="f8188-143">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="f8188-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f8188-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f8188-144">string</span></span><br/> | <span data-ttu-id="f8188-145">–</span><span class="sxs-lookup"><span data-stu-id="f8188-145">n/a</span></span><br/>         | <span data-ttu-id="f8188-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="f8188-146">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="f8188-147">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f8188-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f8188-148">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f8188-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f8188-149">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="f8188-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f8188-150">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="f8188-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f8188-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8188-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8188-152">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f8188-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




