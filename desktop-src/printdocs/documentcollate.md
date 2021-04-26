---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959613299c53996ce7d66171d2da1518f28b9298
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993997"
---
# <a name="documentcollate"></a><span data-ttu-id="848e0-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="848e0-104">DocumentCollate</span></span>

<span data-ttu-id="848e0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="848e0-105">This topic is not current.</span></span> <span data-ttu-id="848e0-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="848e0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="848e0-107">Beschreibt die Sortiermerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="848e0-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="848e0-108">Alle Seiten in jedem einzelnen Dokument werden sortiert.</span><span class="sxs-lookup"><span data-stu-id="848e0-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="848e0-109">DocumentCollate und JobCollateAlldocuments schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="848e0-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="848e0-110">Das Verhalten und die Implementierung, ob beide oder nur eines dieser Schlüsselwörter implementiert ist, bleibt dem Treiber überlassen.</span><span class="sxs-lookup"><span data-stu-id="848e0-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="848e0-111">Im Folgenden finden Sie die Regeln, die für die Collate-Implementierung befolgt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="848e0-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="848e0-112">Elementdefinition und Regeln</span><span class="sxs-lookup"><span data-stu-id="848e0-112">Element Definition and Rules</span></span>

<span data-ttu-id="848e0-113">Sie müssen zuerst die Regeln für JobCollateAllDocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="848e0-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="848e0-114">Beachten Sie, dass in einer Konvertierungseinstellung von PrintTicket in Devmode, bei der JobCollateAllDocuments vom Treiber nicht unterstützt wird, der Treiber das geeignete Verhalten auswählen muss (JobCollateAllDocuments = ON oder OFF).</span><span class="sxs-lookup"><span data-stu-id="848e0-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="848e0-115">Außerdem kann die Auswahl abhängig von anderen PrintTicket-Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="848e0-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="848e0-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="848e0-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="848e0-117">EIN: Drucken Sie (DocumentCopiesAllPages) Kopien jedes Dokuments, und wiederholen Sie die Zeiten von JobCopiesAllDocuments.</span><span class="sxs-lookup"><span data-stu-id="848e0-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="848e0-118">OFF: Für jedes Dokument werden Druckkopien (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen kopiert.</span><span class="sxs-lookup"><span data-stu-id="848e0-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="848e0-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="848e0-119">DocumentCollate</span></span>

<span data-ttu-id="848e0-120">ON: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines Dokuments, die zusammenhängend gedruckt werden, sortieren Sie blätter in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="848e0-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="848e0-121">OFF: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, drucken Sie alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen.</span><span class="sxs-lookup"><span data-stu-id="848e0-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="848e0-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="848e0-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="848e0-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="848e0-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="848e0-124">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="848e0-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="848e0-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="848e0-125">Element Information</span></span>



| <span data-ttu-id="848e0-126">Name</span><span class="sxs-lookup"><span data-stu-id="848e0-126">Name</span></span> | <span data-ttu-id="848e0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="848e0-127">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="848e0-128">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="848e0-128">Element Type</span></span> <br/>   | <span data-ttu-id="848e0-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="848e0-129">Feature</span></span><br/>  |
| <span data-ttu-id="848e0-130">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="848e0-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="848e0-131">Dokument</span><span class="sxs-lookup"><span data-stu-id="848e0-131">Document</span></span><br/> |
| <span data-ttu-id="848e0-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="848e0-132">Notes</span></span> <br/>          | <span data-ttu-id="848e0-133">Keine</span><span class="sxs-lookup"><span data-stu-id="848e0-133">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="848e0-134">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="848e0-134">Structural Content</span></span>

<span data-ttu-id="848e0-135">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="848e0-135">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="848e0-136">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="848e0-136">Structure Variables</span></span>

<span data-ttu-id="848e0-137">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="848e0-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="848e0-138">Name</span><span class="sxs-lookup"><span data-stu-id="848e0-138">Name</span></span>                               | <span data-ttu-id="848e0-139">Datentyp</span><span class="sxs-lookup"><span data-stu-id="848e0-139">Data type</span></span>         | <span data-ttu-id="848e0-140">Einheit</span><span class="sxs-lookup"><span data-stu-id="848e0-140">Unit</span></span>                  | <span data-ttu-id="848e0-141">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="848e0-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="848e0-142">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="848e0-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="848e0-143">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="848e0-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="848e0-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="848e0-144">string</span></span><br/> | <span data-ttu-id="848e0-145">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="848e0-145">characters</span></span><br/> | <span data-ttu-id="848e0-146">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="848e0-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="848e0-147">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="848e0-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="848e0-148">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="848e0-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="848e0-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="848e0-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="848e0-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="848e0-150">string</span></span><br/> | <span data-ttu-id="848e0-151">–</span><span class="sxs-lookup"><span data-stu-id="848e0-151">n/a</span></span><br/>        | <span data-ttu-id="848e0-152">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="848e0-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="848e0-153">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="848e0-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="848e0-154">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="848e0-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="848e0-155">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="848e0-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="848e0-156">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="848e0-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="848e0-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="848e0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="848e0-158">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="848e0-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




