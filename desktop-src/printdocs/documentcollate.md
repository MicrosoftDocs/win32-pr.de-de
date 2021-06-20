---
description: Erfahren Sie mehr über das DocumentCollate-Element, das die Sortierungsmerkmale der Ausgabe beschreibt.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409453"
---
# <a name="documentcollate"></a><span data-ttu-id="4b253-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="4b253-103">DocumentCollate</span></span>

<span data-ttu-id="4b253-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4b253-104">This topic is not current.</span></span> <span data-ttu-id="4b253-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4b253-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b253-106">Beschreibt die Sortierungsmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4b253-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="4b253-107">Alle Seiten in jedem einzelnen Dokument werden sortiert.</span><span class="sxs-lookup"><span data-stu-id="4b253-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="4b253-108">DocumentCollate und JobCollateAlldocuments schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="4b253-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="4b253-109">Das Verhalten und die Implementierung, ob beide oder nur eines dieser Schlüsselwörter implementiert wird, bleiben dem Treiber erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b253-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="4b253-110">Im Folgenden finden Sie die Regeln, die für die Collate-Implementierung befolgt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="4b253-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="4b253-111">Elementdefinition und Regeln</span><span class="sxs-lookup"><span data-stu-id="4b253-111">Element Definition and Rules</span></span>

<span data-ttu-id="4b253-112">Sie müssen zuerst die Regeln für JobCollateAllDocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4b253-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="4b253-113">Beachten Sie, dass es in einer Konvertierungseinstellung "PrintTicket in Devmode", bei der JobCollateAllDocuments vom Treiber nicht unterstützt wird, Aufgabe des Treibers ist, das geeignete Verhalten zu wählen (JobCollateAllDocuments = ON oder OFF).</span><span class="sxs-lookup"><span data-stu-id="4b253-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="4b253-114">Außerdem kann die Auswahl abhängig von anderen PrintTicket-Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4b253-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="4b253-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="4b253-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="4b253-116">ON: Drucken Sie (DocumentCopiesAllPages)-Kopien jedes Dokuments, wiederholen Sie JobCopiesAllDocuments-Zeiten.</span><span class="sxs-lookup"><span data-stu-id="4b253-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="4b253-117">OFF: Für jedes Dokument kopiert print (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen.</span><span class="sxs-lookup"><span data-stu-id="4b253-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="4b253-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="4b253-118">DocumentCollate</span></span>

<span data-ttu-id="4b253-119">ON: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines zusammenhängend gedruckten Dokuments werden die Blätter in diesem Dokument sortiert.</span><span class="sxs-lookup"><span data-stu-id="4b253-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="4b253-120">OFF: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, drucken Sie alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen.</span><span class="sxs-lookup"><span data-stu-id="4b253-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="4b253-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4b253-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="4b253-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4b253-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="4b253-123">XML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="4b253-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4b253-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4b253-124">Element Information</span></span>



| <span data-ttu-id="4b253-125">Name</span><span class="sxs-lookup"><span data-stu-id="4b253-125">Name</span></span> | <span data-ttu-id="4b253-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4b253-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="4b253-127">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4b253-127">Element Type</span></span> <br/>   | <span data-ttu-id="4b253-128">Funktion</span><span class="sxs-lookup"><span data-stu-id="4b253-128">Feature</span></span><br/>  |
| <span data-ttu-id="4b253-129">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4b253-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4b253-130">Dokument</span><span class="sxs-lookup"><span data-stu-id="4b253-130">Document</span></span><br/> |
| <span data-ttu-id="4b253-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4b253-131">Notes</span></span> <br/>          | <span data-ttu-id="4b253-132">Keine</span><span class="sxs-lookup"><span data-stu-id="4b253-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="4b253-133">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="4b253-133">Structural Content</span></span>

<span data-ttu-id="4b253-134">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="4b253-134">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4b253-135">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4b253-135">Structure Variables</span></span>

<span data-ttu-id="4b253-136">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4b253-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4b253-137">Name</span><span class="sxs-lookup"><span data-stu-id="4b253-137">Name</span></span>                               | <span data-ttu-id="4b253-138">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4b253-138">Data type</span></span>         | <span data-ttu-id="4b253-139">Einheit</span><span class="sxs-lookup"><span data-stu-id="4b253-139">Unit</span></span>                  | <span data-ttu-id="4b253-140">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4b253-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4b253-141">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4b253-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4b253-142">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="4b253-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4b253-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4b253-143">string</span></span><br/> | <span data-ttu-id="4b253-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4b253-144">characters</span></span><br/> | <span data-ttu-id="4b253-145">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4b253-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4b253-146">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4b253-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4b253-147">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4b253-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4b253-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4b253-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4b253-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4b253-149">string</span></span><br/> | <span data-ttu-id="4b253-150">–</span><span class="sxs-lookup"><span data-stu-id="4b253-150">n/a</span></span><br/>        | <span data-ttu-id="4b253-151">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4b253-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4b253-152">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4b253-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4b253-153">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="4b253-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4b253-154">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="4b253-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4b253-155">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4b253-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4b253-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b253-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b253-157">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4b253-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




