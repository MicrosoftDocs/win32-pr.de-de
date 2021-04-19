---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: Documentcoverfront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b143ea6a3e1edd667d56619c190d99d1de93496f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106366388"
---
# <a name="documentcoverfront"></a><span data-ttu-id="56de6-104">Documentcoverfront</span><span class="sxs-lookup"><span data-stu-id="56de6-104">DocumentCoverFront</span></span>

<span data-ttu-id="56de6-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="56de6-105">This topic is not current.</span></span> <span data-ttu-id="56de6-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56de6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56de6-107">Beschreibt das Deck Blatt "Front (Anfang)".</span><span class="sxs-lookup"><span data-stu-id="56de6-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="56de6-108">Jedes Dokument enthält ein separates Blatt.</span><span class="sxs-lookup"><span data-stu-id="56de6-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="56de6-109">Das Deckblatt sollte auf der Seite PageMediaSize und PageMediaType gedruckt werden, die für die erste Seite des Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56de6-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="56de6-110">Das Deck Blatt sollte in Verarbeitungsoptionen (z. b. DocumentDuplex, DocumentNUp) integriert werden, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="56de6-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="56de6-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56de6-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56de6-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="56de6-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="56de6-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="56de6-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="56de6-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56de6-114">Element Information</span></span>



| <span data-ttu-id="56de6-115">Name</span><span class="sxs-lookup"><span data-stu-id="56de6-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56de6-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="56de6-116">Element Type</span></span> <br/>   | <span data-ttu-id="56de6-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="56de6-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="56de6-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="56de6-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56de6-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="56de6-119">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="56de6-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="56de6-120">Notes</span></span> <br/>          | <span data-ttu-id="56de6-121">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="56de6-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="56de6-122">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="56de6-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="56de6-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="56de6-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="56de6-124">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="56de6-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="56de6-125">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="56de6-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="56de6-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="56de6-126">Structural Content</span></span>

<span data-ttu-id="56de6-127">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="56de6-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="56de6-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="56de6-128">Structure Variables</span></span>

<span data-ttu-id="56de6-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="56de6-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56de6-130">Name</span><span class="sxs-lookup"><span data-stu-id="56de6-130">Name</span></span>                               | <span data-ttu-id="56de6-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="56de6-131">Data type</span></span>         | <span data-ttu-id="56de6-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="56de6-132">Unit</span></span>                  | <span data-ttu-id="56de6-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="56de6-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="56de6-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56de6-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="56de6-135">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="56de6-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="56de6-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56de6-136">string</span></span><br/> | <span data-ttu-id="56de6-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="56de6-137">characters</span></span><br/> | <span data-ttu-id="56de6-138">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="56de6-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="56de6-139">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="56de6-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="56de6-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="56de6-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="56de6-141">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="56de6-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="56de6-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56de6-142">string</span></span><br/> | <span data-ttu-id="56de6-143">–</span><span class="sxs-lookup"><span data-stu-id="56de6-143">n/a</span></span><br/>        | <span data-ttu-id="56de6-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="56de6-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="56de6-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="56de6-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="56de6-146">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="56de6-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="56de6-147">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="56de6-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="56de6-148">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="56de6-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="56de6-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56de6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56de6-150">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="56de6-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




