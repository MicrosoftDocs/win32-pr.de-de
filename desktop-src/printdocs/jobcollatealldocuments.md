---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7d3ba5b55ece6d7237846ae8ef969c0a3d17e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998357"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="360f7-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="360f7-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="360f7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="360f7-105">This topic is not current.</span></span> <span data-ttu-id="360f7-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="360f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="360f7-107">Beschreibt die Sortierungsmerkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="360f7-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="360f7-108">Alle Dokumente in jedem einzelnen Auftrag werden sortiert.</span><span class="sxs-lookup"><span data-stu-id="360f7-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="360f7-109">DocumentCollate und JobCollateAlldocuments schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="360f7-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="360f7-110">Das Verhalten und die Implementierung, ob beide oder nur eines dieser Schlüsselwörter implementiert wird, bleiben dem Treiber erhalten.</span><span class="sxs-lookup"><span data-stu-id="360f7-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="360f7-111">Im Folgenden finden Sie die Regeln, die für die Collate-Implementierung befolgt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="360f7-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="360f7-112">Elementdefinition und Regeln</span><span class="sxs-lookup"><span data-stu-id="360f7-112">Element Definition and Rules</span></span>

<span data-ttu-id="360f7-113">Sie müssen zuerst die Regeln für JobCollateAllDocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="360f7-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="360f7-114">Beachten Sie, dass es in einer Konvertierungseinstellung "PrintTicket in Devmode", bei der JobCollateAllDocuments vom Treiber nicht unterstützt wird, Aufgabe des Treibers ist, das geeignete Verhalten zu wählen (JobCollateAllDocuments = ON oder OFF).</span><span class="sxs-lookup"><span data-stu-id="360f7-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="360f7-115">Außerdem kann die Auswahl abhängig von anderen PrintTicket-Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="360f7-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="360f7-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="360f7-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="360f7-117">ON: Drucken Sie (DocumentCopiesAllPages) Kopien jedes Dokuments, wiederholen Sie JobCopiesAllDocuments-Zeiten.</span><span class="sxs-lookup"><span data-stu-id="360f7-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="360f7-118">OFF: Für jedes Dokument kopiert print (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen.</span><span class="sxs-lookup"><span data-stu-id="360f7-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="360f7-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="360f7-119">DocumentCollate</span></span>

<span data-ttu-id="360f7-120">ON: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines zusammenhängend gedruckten Dokuments werden die Blätter in diesem Dokument sortiert.</span><span class="sxs-lookup"><span data-stu-id="360f7-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="360f7-121">OFF: Drucken Sie für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen.</span><span class="sxs-lookup"><span data-stu-id="360f7-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="360f7-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="360f7-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="360f7-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="360f7-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="360f7-124">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="360f7-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="360f7-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="360f7-125">Element Information</span></span>



| <span data-ttu-id="360f7-126">Name</span><span class="sxs-lookup"><span data-stu-id="360f7-126">Name</span></span> | <span data-ttu-id="360f7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="360f7-127">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="360f7-128">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="360f7-128">Element Type</span></span> <br/>   | <span data-ttu-id="360f7-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="360f7-129">Feature</span></span><br/> |
| <span data-ttu-id="360f7-130">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="360f7-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="360f7-131">Auftrag</span><span class="sxs-lookup"><span data-stu-id="360f7-131">Job</span></span><br/>     |
| <span data-ttu-id="360f7-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="360f7-132">Notes</span></span> <br/>          | <span data-ttu-id="360f7-133">Keine</span><span class="sxs-lookup"><span data-stu-id="360f7-133">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="360f7-134">Strukturell</span><span class="sxs-lookup"><span data-stu-id="360f7-134">Structural Content</span></span>

<span data-ttu-id="360f7-135">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="360f7-135">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="360f7-136">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="360f7-136">Structure Variables</span></span>

<span data-ttu-id="360f7-137">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="360f7-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="360f7-138">Name</span><span class="sxs-lookup"><span data-stu-id="360f7-138">Name</span></span>                               | <span data-ttu-id="360f7-139">Datentyp</span><span class="sxs-lookup"><span data-stu-id="360f7-139">Data type</span></span>         | <span data-ttu-id="360f7-140">Einheit</span><span class="sxs-lookup"><span data-stu-id="360f7-140">Unit</span></span>                  | <span data-ttu-id="360f7-141">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="360f7-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="360f7-142">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="360f7-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="360f7-143">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="360f7-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="360f7-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="360f7-144">string</span></span><br/> | <span data-ttu-id="360f7-145">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="360f7-145">characters</span></span><br/> | <span data-ttu-id="360f7-146">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="360f7-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="360f7-147">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="360f7-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="360f7-148">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="360f7-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="360f7-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="360f7-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="360f7-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="360f7-150">string</span></span><br/> | <span data-ttu-id="360f7-151">–</span><span class="sxs-lookup"><span data-stu-id="360f7-151">n/a</span></span><br/>        | <span data-ttu-id="360f7-152">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="360f7-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="360f7-153">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="360f7-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="360f7-154">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="360f7-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="360f7-155">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="360f7-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="360f7-156">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="360f7-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




