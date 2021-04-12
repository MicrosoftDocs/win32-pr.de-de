---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219107"
---
# <a name="documentnup"></a><span data-ttu-id="89613-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="89613-104">DocumentNUp</span></span>

<span data-ttu-id="89613-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="89613-105">This topic is not current.</span></span> <span data-ttu-id="89613-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="89613-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="89613-107">Beschreibt die Ausgabe und das Format mehrerer logischer Seiten an ein einzelnes physisches Blatt.</span><span class="sxs-lookup"><span data-stu-id="89613-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="89613-108">Jedes Dokument wird separat kompiliert.</span><span class="sxs-lookup"><span data-stu-id="89613-108">Each document is compiled separately.</span></span> <span data-ttu-id="89613-109">"DocumentNUp" und "jobnupalldocumentsangrenzende" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="89613-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="89613-110">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="89613-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="89613-111">Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1, das drei Seiten enthält, und Dokument 2, das zwei Seiten enthält.</span><span class="sxs-lookup"><span data-stu-id="89613-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="89613-112">Jedes Dokument wird separat duplext.</span><span class="sxs-lookup"><span data-stu-id="89613-112">Each document is duplexed separately.</span></span> <span data-ttu-id="89613-113">Die unten gezeigte Präsentations Richtung ist die Option RightBottom.</span><span class="sxs-lookup"><span data-stu-id="89613-113">The presentation direction shown below is the RightBottom option.</span></span>

![ein Diagramm, das zeigt, wie Dokument Seiten basierend auf der DocumentNUp-Einstellung auf einem einzelnen Blatt angelegt werden](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="89613-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="89613-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="89613-116">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="89613-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="89613-117">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="89613-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="89613-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="89613-118">Element Information</span></span>



| <span data-ttu-id="89613-119">Name</span><span class="sxs-lookup"><span data-stu-id="89613-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89613-120">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="89613-120">Element Type</span></span> <br/>   | <span data-ttu-id="89613-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="89613-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="89613-122">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="89613-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="89613-123">Dokument</span><span class="sxs-lookup"><span data-stu-id="89613-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="89613-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="89613-124">Notes</span></span> <br/>          | <span data-ttu-id="89613-125">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="89613-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="89613-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="89613-126">Structural Content</span></span>

<span data-ttu-id="89613-127">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="89613-127">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
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

## <a name="structure-variables"></a><span data-ttu-id="89613-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="89613-128">Structure Variables</span></span>

<span data-ttu-id="89613-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="89613-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="89613-130">Name</span><span class="sxs-lookup"><span data-stu-id="89613-130">Name</span></span>                                           | <span data-ttu-id="89613-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="89613-131">Data type</span></span>          | <span data-ttu-id="89613-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="89613-132">Unit</span></span>                     | <span data-ttu-id="89613-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="89613-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="89613-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="89613-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89613-135">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="89613-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="89613-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="89613-136">string</span></span><br/>  | <span data-ttu-id="89613-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="89613-137">characters</span></span><br/>    | <span data-ttu-id="89613-138">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="89613-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="89613-139">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="89613-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="89613-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="89613-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="89613-141">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="89613-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="89613-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="89613-142">string</span></span><br/>  | <span data-ttu-id="89613-143">–</span><span class="sxs-lookup"><span data-stu-id="89613-143">n/a</span></span><br/>           | <span data-ttu-id="89613-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="89613-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="89613-145">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="89613-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="89613-146">\_Pagespersheetvalue\_</span><span class="sxs-lookup"><span data-stu-id="89613-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="89613-147">integer</span><span class="sxs-lookup"><span data-stu-id="89613-147">integer</span></span><br/> | <span data-ttu-id="89613-148">Logische Seiten</span><span class="sxs-lookup"><span data-stu-id="89613-148">Logical pages</span></span><br/> | <span data-ttu-id="89613-149">Alle ganzzahligen Werte (größer als null).</span><span class="sxs-lookup"><span data-stu-id="89613-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="89613-150">Gibt die Anzahl der logischen Seiten pro physikalischer Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="89613-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="89613-151">Die unterstützte Menge kann eine beliebige Gruppe von Ganzzahlen sein, z.b.</span><span class="sxs-lookup"><span data-stu-id="89613-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="89613-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="89613-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="89613-153">\_Presentationdirectionoptionname\_</span><span class="sxs-lookup"><span data-stu-id="89613-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="89613-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="89613-154">string</span></span><br/>  | <span data-ttu-id="89613-155">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="89613-155">characters</span></span><br/>    | <span data-ttu-id="89613-156">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="89613-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="89613-157">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="89613-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="89613-158">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="89613-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="89613-159">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="89613-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="89613-160">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="89613-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="89613-161">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="89613-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="89613-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89613-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89613-163">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="89613-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




