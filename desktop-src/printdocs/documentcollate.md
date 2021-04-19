---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b022d9c8067f330e14697932382c4c8f058a8f3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357174"
---
# <a name="documentcollate"></a><span data-ttu-id="11507-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="11507-104">DocumentCollate</span></span>

<span data-ttu-id="11507-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="11507-105">This topic is not current.</span></span> <span data-ttu-id="11507-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11507-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11507-107">Beschreibt die Sortierungs Merkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="11507-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="11507-108">Alle Seiten in den einzelnen Dokumenten werden sortiert.</span><span class="sxs-lookup"><span data-stu-id="11507-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="11507-109">DocumentCollate und JobCollateAllDocuments schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="11507-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="11507-110">Das Verhalten und die Implementierung, ob sowohl als auch nur eines dieser Schlüsselwörter implementiert ist, wird dem Treiber überlassen.</span><span class="sxs-lookup"><span data-stu-id="11507-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="11507-111">Die folgenden Regeln sollten für die COLLATE-Implementierung befolgt werden:</span><span class="sxs-lookup"><span data-stu-id="11507-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="11507-112">Element Definition und-Regeln</span><span class="sxs-lookup"><span data-stu-id="11507-112">Element Definition and Rules</span></span>

<span data-ttu-id="11507-113">Sie müssen zuerst die Regeln für jobcollatealldocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="11507-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="11507-114">Beachten Sie, dass in einer Konvertierungs Einstellung von PrintTicket zu DEVMODE, in der JobCollateAllDocuments nicht vom Treiber unterstützt wird, der Treiber das geeignete Verhalten auswählen muss (JobCollateAllDocuments = on oder Off).</span><span class="sxs-lookup"><span data-stu-id="11507-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="11507-115">Die Auswahl kann auch abhängig von anderen PrintTicket-Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="11507-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="11507-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="11507-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="11507-117">Auf: Print (DocumentCopiesAllPages)-Kopien der einzelnen Dokumente, wiederholen Sie die JobCopiesAllDocuments-Zeiten.</span><span class="sxs-lookup"><span data-stu-id="11507-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="11507-118">Aus: für jedes Dokument wird Print (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen kopiert.</span><span class="sxs-lookup"><span data-stu-id="11507-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="11507-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="11507-119">DocumentCollate</span></span>

<span data-ttu-id="11507-120">Auf: für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines Dokuments, das zusammenhängend gedruckt wird, werden in diesem Dokument COLLATE-Blätter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11507-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="11507-121">Aus: für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, werden alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen gedruckt.</span><span class="sxs-lookup"><span data-stu-id="11507-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="11507-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="11507-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="11507-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="11507-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="11507-124">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="11507-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="11507-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="11507-125">Element Information</span></span>



| <span data-ttu-id="11507-126">Name</span><span class="sxs-lookup"><span data-stu-id="11507-126">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="11507-127">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="11507-127">Element Type</span></span> <br/>   | <span data-ttu-id="11507-128">Funktion</span><span class="sxs-lookup"><span data-stu-id="11507-128">Feature</span></span><br/>  |
| <span data-ttu-id="11507-129">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="11507-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11507-130">Dokument</span><span class="sxs-lookup"><span data-stu-id="11507-130">Document</span></span><br/> |
| <span data-ttu-id="11507-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11507-131">Notes</span></span> <br/>          | <span data-ttu-id="11507-132">Keine</span><span class="sxs-lookup"><span data-stu-id="11507-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="11507-133">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="11507-133">Structural Content</span></span>

<span data-ttu-id="11507-134">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="11507-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="11507-135">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="11507-135">Structure Variables</span></span>

<span data-ttu-id="11507-136">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="11507-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11507-137">Name</span><span class="sxs-lookup"><span data-stu-id="11507-137">Name</span></span>                               | <span data-ttu-id="11507-138">Datentyp</span><span class="sxs-lookup"><span data-stu-id="11507-138">Data type</span></span>         | <span data-ttu-id="11507-139">Einheit</span><span class="sxs-lookup"><span data-stu-id="11507-139">Unit</span></span>                  | <span data-ttu-id="11507-140">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="11507-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="11507-141">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11507-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="11507-142">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="11507-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="11507-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11507-143">string</span></span><br/> | <span data-ttu-id="11507-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="11507-144">characters</span></span><br/> | <span data-ttu-id="11507-145">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="11507-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="11507-146">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="11507-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="11507-147">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="11507-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="11507-148">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="11507-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="11507-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11507-149">string</span></span><br/> | <span data-ttu-id="11507-150">–</span><span class="sxs-lookup"><span data-stu-id="11507-150">n/a</span></span><br/>        | <span data-ttu-id="11507-151">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="11507-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="11507-152">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="11507-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="11507-153">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="11507-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="11507-154">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="11507-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="11507-155">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="11507-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="11507-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11507-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11507-157">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="11507-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




