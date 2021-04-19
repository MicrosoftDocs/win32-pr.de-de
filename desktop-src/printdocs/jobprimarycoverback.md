---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: Jobprimarycoverback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073e65f80c3bee31423d0cf813d454a32e6f559b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106366575"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="5532e-104">Jobprimarycoverback</span><span class="sxs-lookup"><span data-stu-id="5532e-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="5532e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5532e-105">This topic is not current.</span></span> <span data-ttu-id="5532e-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5532e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5532e-107">Beschreibt das Deckblatt "Back (End)".</span><span class="sxs-lookup"><span data-stu-id="5532e-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="5532e-108">Jeder Auftrag verfügt über ein separates primär Blatt.</span><span class="sxs-lookup"><span data-stu-id="5532e-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="5532e-109">Das Deckblatt sollte auf der Seite PageMediaSize und PageMediaType gedruckt werden, die für die letzte Seite des Auftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5532e-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="5532e-110">Das Deck Blatt sollte in Verarbeitungsoptionen (z. b. jobduplexalldocumentscontiguron, jobnupalldocumentscontiguron) integriert werden, wie in der angegebenen Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="5532e-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="5532e-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5532e-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5532e-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5532e-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5532e-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5532e-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5532e-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5532e-114">Element Information</span></span>



| <span data-ttu-id="5532e-115">Name</span><span class="sxs-lookup"><span data-stu-id="5532e-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5532e-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5532e-116">Element Type</span></span> <br/>   | <span data-ttu-id="5532e-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="5532e-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5532e-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="5532e-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5532e-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5532e-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5532e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="5532e-120">Notes</span></span> <br/>          | <span data-ttu-id="5532e-121">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="5532e-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5532e-122">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5532e-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5532e-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="5532e-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5532e-124">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5532e-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5532e-125">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="5532e-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5532e-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5532e-126">Structural Content</span></span>

<span data-ttu-id="5532e-127">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5532e-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  <!-- Specifies the XPS part name for the back cover sheet. -->
  <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="5532e-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="5532e-128">Structure Variables</span></span>

<span data-ttu-id="5532e-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5532e-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5532e-130">Name</span><span class="sxs-lookup"><span data-stu-id="5532e-130">Name</span></span>                               | <span data-ttu-id="5532e-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5532e-131">Data type</span></span>         | <span data-ttu-id="5532e-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="5532e-132">Unit</span></span>                  | <span data-ttu-id="5532e-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="5532e-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5532e-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5532e-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5532e-135">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="5532e-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5532e-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5532e-136">string</span></span><br/> | <span data-ttu-id="5532e-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5532e-137">characters</span></span><br/> | <span data-ttu-id="5532e-138">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="5532e-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5532e-139">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="5532e-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5532e-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="5532e-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5532e-141">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="5532e-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5532e-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5532e-142">string</span></span><br/> | <span data-ttu-id="5532e-143">–</span><span class="sxs-lookup"><span data-stu-id="5532e-143">n/a</span></span><br/>        | <span data-ttu-id="5532e-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="5532e-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5532e-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5532e-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5532e-146">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5532e-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5532e-147">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="5532e-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5532e-148">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="5532e-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5532e-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5532e-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5532e-150">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="5532e-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




