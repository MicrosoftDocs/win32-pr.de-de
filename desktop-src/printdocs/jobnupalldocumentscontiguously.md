---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f90620ac99bf97e85acb22c723a938c31605bd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998087"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="78bd9-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="78bd9-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="78bd9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="78bd9-105">This topic is not current.</span></span> <span data-ttu-id="78bd9-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="78bd9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="78bd9-107">Beschreibt die Ausgabe mehrerer logischer Seiten auf einem einzelnen physischen Blatt.</span><span class="sxs-lookup"><span data-stu-id="78bd9-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="78bd9-108">Alle Dokumente im Auftrag werden zusammenhängend kompiliert.</span><span class="sxs-lookup"><span data-stu-id="78bd9-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="78bd9-109">JobNUpAllDocumentsContiguously und DocumentNUp schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="78bd9-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="78bd9-110">Der Treiber muss die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="78bd9-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="78bd9-111">Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1 mit drei Seiten und Dokument 2 mit zwei Seiten.</span><span class="sxs-lookup"><span data-stu-id="78bd9-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="78bd9-112">Jedes Dokument im Auftrag ist zusammenhängend verduplext.</span><span class="sxs-lookup"><span data-stu-id="78bd9-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="78bd9-113">Die in diesem Beispiel gezeigten Präsentationsrichtungen sind die RightBottom-Option.</span><span class="sxs-lookup"><span data-stu-id="78bd9-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![Diagramm, das zeigt, wie Dokumentseiten basierend auf der Documentnupeinstellung auf einem einzelnen Blatt dargestellt werden](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="78bd9-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="78bd9-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="78bd9-116">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="78bd9-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="78bd9-117">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="78bd9-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="78bd9-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="78bd9-118">Element Information</span></span>



| <span data-ttu-id="78bd9-119">Name</span><span class="sxs-lookup"><span data-stu-id="78bd9-119">Name</span></span> | <span data-ttu-id="78bd9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="78bd9-120">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bd9-121">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="78bd9-121">Element Type</span></span> <br/>   | <span data-ttu-id="78bd9-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="78bd9-122">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="78bd9-123">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="78bd9-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="78bd9-124">Auftrag</span><span class="sxs-lookup"><span data-stu-id="78bd9-124">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="78bd9-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78bd9-125">Notes</span></span> <br/>          | <span data-ttu-id="78bd9-126">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der Höhe und Breite bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="78bd9-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="78bd9-127">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="78bd9-127">Structural Content</span></span>

<span data-ttu-id="78bd9-128">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="78bd9-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="78bd9-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="78bd9-129">Structure Variables</span></span>

<span data-ttu-id="78bd9-130">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78bd9-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="78bd9-131">Name</span><span class="sxs-lookup"><span data-stu-id="78bd9-131">Name</span></span>                                           | <span data-ttu-id="78bd9-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="78bd9-132">Data type</span></span>          | <span data-ttu-id="78bd9-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="78bd9-133">Unit</span></span>                     | <span data-ttu-id="78bd9-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="78bd9-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="78bd9-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="78bd9-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bd9-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="78bd9-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="78bd9-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="78bd9-137">string</span></span><br/>  | <span data-ttu-id="78bd9-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="78bd9-138">characters</span></span><br/>    | <span data-ttu-id="78bd9-139">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="78bd9-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="78bd9-140">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="78bd9-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="78bd9-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="78bd9-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="78bd9-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="78bd9-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="78bd9-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="78bd9-143">string</span></span><br/>  | <span data-ttu-id="78bd9-144">–</span><span class="sxs-lookup"><span data-stu-id="78bd9-144">n/a</span></span><br/>           | <span data-ttu-id="78bd9-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="78bd9-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="78bd9-146">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="78bd9-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="78bd9-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="78bd9-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="78bd9-148">integer</span><span class="sxs-lookup"><span data-stu-id="78bd9-148">integer</span></span><br/> | <span data-ttu-id="78bd9-149">Logische Seiten</span><span class="sxs-lookup"><span data-stu-id="78bd9-149">Logical pages</span></span><br/> | <span data-ttu-id="78bd9-150">Alle ganzen Zahlen (größer als null).</span><span class="sxs-lookup"><span data-stu-id="78bd9-150">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="78bd9-151">Gibt die Anzahl logischer Seiten pro physischem Blatt an.</span><span class="sxs-lookup"><span data-stu-id="78bd9-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="78bd9-152">Der unterstützte Satz kann ein beliebiger Satz von ganzen Zahlen sein, z. B.</span><span class="sxs-lookup"><span data-stu-id="78bd9-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="78bd9-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="78bd9-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="78bd9-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="78bd9-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="78bd9-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="78bd9-155">string</span></span><br/>  | <span data-ttu-id="78bd9-156">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="78bd9-156">characters</span></span><br/>    | <span data-ttu-id="78bd9-157">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="78bd9-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="78bd9-158">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="78bd9-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="78bd9-159">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="78bd9-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="78bd9-160">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="78bd9-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="78bd9-161">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="78bd9-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="78bd9-162">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="78bd9-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="78bd9-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78bd9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78bd9-164">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="78bd9-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




