---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: Jobnupalldocumentszusammen hängend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351998"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="7f266-104">Jobnupalldocumentszusammen hängend</span><span class="sxs-lookup"><span data-stu-id="7f266-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="7f266-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7f266-105">This topic is not current.</span></span> <span data-ttu-id="7f266-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7f266-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7f266-107">Beschreibt die Ausgabe mehrerer logischer Seiten an ein einzelnes physisches Blatt.</span><span class="sxs-lookup"><span data-stu-id="7f266-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="7f266-108">Alle Dokumente im Auftrag werden zusammenhängend zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="7f266-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="7f266-109">Jobnupalldocumentsangrenzenden und DocumentNUp schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7f266-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="7f266-110">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7f266-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="7f266-111">Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1, das drei Seiten enthält, und Dokument 2, das zwei Seiten enthält.</span><span class="sxs-lookup"><span data-stu-id="7f266-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="7f266-112">Jedes Dokument im Auftrag wird zusammenhängend synchron.</span><span class="sxs-lookup"><span data-stu-id="7f266-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="7f266-113">Die im Beispiel gezeigten Präsentations Richtungen sind die Option RightBottom.</span><span class="sxs-lookup"><span data-stu-id="7f266-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![ein Diagramm, das zeigt, wie Dokument Seiten basierend auf der DocumentNUp-Einstellung auf einem einzelnen Blatt angelegt werden](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="7f266-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7f266-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7f266-116">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7f266-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7f266-117">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7f266-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7f266-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7f266-118">Element Information</span></span>



| <span data-ttu-id="7f266-119">Name</span><span class="sxs-lookup"><span data-stu-id="7f266-119">Name</span></span>                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f266-120">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7f266-120">Element Type</span></span> <br/>   | <span data-ttu-id="7f266-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="7f266-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="7f266-122">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="7f266-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7f266-123">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7f266-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="7f266-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f266-124">Notes</span></span> <br/>          | <span data-ttu-id="7f266-125">"Top", "Bottom", "Left" und "Right" sind relativ zu "PageImageableSize", wobei "TopLeft" durch den Ursprung der Höhe und der Breite gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7f266-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7f266-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="7f266-126">Structural Content</span></span>

<span data-ttu-id="7f266-127">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="7f266-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7f266-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="7f266-128">Structure Variables</span></span>

<span data-ttu-id="7f266-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7f266-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7f266-130">Name</span><span class="sxs-lookup"><span data-stu-id="7f266-130">Name</span></span>                                           | <span data-ttu-id="7f266-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7f266-131">Data type</span></span>          | <span data-ttu-id="7f266-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="7f266-132">Unit</span></span>                     | <span data-ttu-id="7f266-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="7f266-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7f266-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7f266-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f266-135">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="7f266-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="7f266-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f266-136">string</span></span><br/>  | <span data-ttu-id="7f266-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7f266-137">characters</span></span><br/>    | <span data-ttu-id="7f266-138">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="7f266-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7f266-139">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="7f266-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7f266-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="7f266-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="7f266-141">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="7f266-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="7f266-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f266-142">string</span></span><br/>  | <span data-ttu-id="7f266-143">–</span><span class="sxs-lookup"><span data-stu-id="7f266-143">n/a</span></span><br/>           | <span data-ttu-id="7f266-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="7f266-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7f266-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7f266-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="7f266-146">\_Pagespersheetvalue\_</span><span class="sxs-lookup"><span data-stu-id="7f266-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="7f266-147">integer</span><span class="sxs-lookup"><span data-stu-id="7f266-147">integer</span></span><br/> | <span data-ttu-id="7f266-148">Logische Seiten</span><span class="sxs-lookup"><span data-stu-id="7f266-148">Logical pages</span></span><br/> | <span data-ttu-id="7f266-149">Alle ganzzahligen Werte (größer als null).</span><span class="sxs-lookup"><span data-stu-id="7f266-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="7f266-150">Gibt die Anzahl der logischen Seiten pro physikalischer Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="7f266-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="7f266-151">Die unterstützte Menge kann eine beliebige Gruppe von Ganzzahlen sein, z.b.</span><span class="sxs-lookup"><span data-stu-id="7f266-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="7f266-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="7f266-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="7f266-153">\_Presentationdirectionoptionname\_</span><span class="sxs-lookup"><span data-stu-id="7f266-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="7f266-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f266-154">string</span></span><br/>  | <span data-ttu-id="7f266-155">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7f266-155">characters</span></span><br/>    | <span data-ttu-id="7f266-156">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="7f266-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7f266-157">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="7f266-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7f266-158">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="7f266-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7f266-159">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7f266-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7f266-160">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="7f266-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7f266-161">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="7f266-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7f266-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f266-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f266-163">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="7f266-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




