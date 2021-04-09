---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: Joberrorsheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869668"
---
# <a name="joberrorsheet"></a><span data-ttu-id="9d69f-104">Joberrorsheet</span><span class="sxs-lookup"><span data-stu-id="9d69f-104">JobErrorSheet</span></span>

<span data-ttu-id="9d69f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9d69f-105">This topic is not current.</span></span> <span data-ttu-id="9d69f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d69f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d69f-107">Beschreibt die Ausgabe des Fehler Blatts.</span><span class="sxs-lookup"><span data-stu-id="9d69f-107">Describes the error sheet output.</span></span> <span data-ttu-id="9d69f-108">Der gesamte Auftrag wird mit einem einzelnen Fehler Blatt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d69f-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="9d69f-109">Das Fehler Blatt sollte auf der Standardseite PageMediaSize ausgegeben werden und mithilfe des standardmäßigen PageMediaType verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d69f-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="9d69f-110">Das Fehler Blatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="9d69f-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="9d69f-111">Dies bedeutet, dass das Fehler Blatt bei allen Beendigungs-oder Verarbeitungsoptionen (z. b. jobduplex, jobstaple oder jobbinding) nicht enthalten sein sollte.</span><span class="sxs-lookup"><span data-stu-id="9d69f-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="9d69f-112">Das Fehler Blatt sollte als abschließendes Blatt des Auftrags auftreten.</span><span class="sxs-lookup"><span data-stu-id="9d69f-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="9d69f-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9d69f-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d69f-114">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9d69f-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9d69f-115">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9d69f-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9d69f-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9d69f-116">Element Information</span></span>



| <span data-ttu-id="9d69f-117">Name</span><span class="sxs-lookup"><span data-stu-id="9d69f-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d69f-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9d69f-118">Element Type</span></span> <br/>   | <span data-ttu-id="9d69f-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="9d69f-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d69f-120">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="9d69f-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d69f-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d69f-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d69f-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d69f-122">Notes</span></span> <br/>          | <span data-ttu-id="9d69f-123">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="9d69f-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9d69f-124">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="9d69f-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9d69f-125">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="9d69f-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9d69f-126">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9d69f-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9d69f-127">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="9d69f-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9d69f-128">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9d69f-128">Structural Content</span></span>

<span data-ttu-id="9d69f-129">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9d69f-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="9d69f-130">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9d69f-130">Structure Variables</span></span>

<span data-ttu-id="9d69f-131">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9d69f-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d69f-132">Name</span><span class="sxs-lookup"><span data-stu-id="9d69f-132">Name</span></span>                                             | <span data-ttu-id="9d69f-133">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9d69f-133">Data type</span></span>         | <span data-ttu-id="9d69f-134">Einheit</span><span class="sxs-lookup"><span data-stu-id="9d69f-134">Unit</span></span>                  | <span data-ttu-id="9d69f-135">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9d69f-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9d69f-136">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9d69f-136">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9d69f-137">\_Errorsheetinstanoptionname\_</span><span class="sxs-lookup"><span data-stu-id="9d69f-137">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="9d69f-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d69f-138">string</span></span><br/> | <span data-ttu-id="9d69f-139">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9d69f-139">characters</span></span><br/> | <span data-ttu-id="9d69f-140">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9d69f-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9d69f-141">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9d69f-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9d69f-142">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9d69f-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9d69f-143">\_Errorsheet-identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9d69f-143">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9d69f-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d69f-144">string</span></span><br/> | <span data-ttu-id="9d69f-145">–</span><span class="sxs-lookup"><span data-stu-id="9d69f-145">n/a</span></span><br/>        | <span data-ttu-id="9d69f-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9d69f-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9d69f-147">Definiert die Auswahlkriterien für die Benutzeroberfläche (UI).</span><span class="sxs-lookup"><span data-stu-id="9d69f-147">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="9d69f-148">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="9d69f-148">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="9d69f-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d69f-149">string</span></span><br/> | <span data-ttu-id="9d69f-150">–</span><span class="sxs-lookup"><span data-stu-id="9d69f-150">n/a</span></span><br/>        | <span data-ttu-id="9d69f-151">Gültiger voll qualifizierter Name, wie durch definiert https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="9d69f-151">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="9d69f-152">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9d69f-152">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="9d69f-153">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9d69f-153">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9d69f-154">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9d69f-154">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="9d69f-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d69f-155">string</span></span><br/> | <span data-ttu-id="9d69f-156">–</span><span class="sxs-lookup"><span data-stu-id="9d69f-156">n/a</span></span><br/>        | <span data-ttu-id="9d69f-157">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9d69f-157">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9d69f-158">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9d69f-158">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9d69f-159">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9d69f-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9d69f-160">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9d69f-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9d69f-161">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9d69f-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="9d69f-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d69f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d69f-163">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9d69f-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




