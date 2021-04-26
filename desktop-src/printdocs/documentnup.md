---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab531a2095e83aa35f3dff450270c2a5b4520d62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996287"
---
# <a name="documentnup"></a><span data-ttu-id="b7b69-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="b7b69-104">DocumentNUp</span></span>

<span data-ttu-id="b7b69-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b7b69-105">This topic is not current.</span></span> <span data-ttu-id="b7b69-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b7b69-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7b69-107">Beschreibt die Ausgabe und das Format mehrerer logischer Seiten auf einem einzelnen physischen Blatt.</span><span class="sxs-lookup"><span data-stu-id="b7b69-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="b7b69-108">Jedes Dokument wird separat kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b7b69-108">Each document is compiled separately.</span></span> <span data-ttu-id="b7b69-109">DocumentNUp und JobNUpAllDocuments Schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="b7b69-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="b7b69-110">Der Treiber muss die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b7b69-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="b7b69-111">Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1 mit drei Seiten und Dokument 2 mit zwei Seiten.</span><span class="sxs-lookup"><span data-stu-id="b7b69-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="b7b69-112">Jedes Dokument wird separat verduplext.</span><span class="sxs-lookup"><span data-stu-id="b7b69-112">Each document is duplexed separately.</span></span> <span data-ttu-id="b7b69-113">Die unten gezeigte Darstellungsrichtung ist die RightBottom-Option.</span><span class="sxs-lookup"><span data-stu-id="b7b69-113">The presentation direction shown below is the RightBottom option.</span></span>

![Diagramm, das zeigt, wie Dokumentseiten basierend auf der Documentnupeinstellung auf einem einzelnen Blatt dargestellt werden](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="b7b69-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b7b69-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7b69-116">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b7b69-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b7b69-117">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b7b69-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b7b69-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b7b69-118">Element Information</span></span>



| <span data-ttu-id="b7b69-119">Name</span><span class="sxs-lookup"><span data-stu-id="b7b69-119">Name</span></span> | <span data-ttu-id="b7b69-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b7b69-120">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b69-121">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b7b69-121">Element Type</span></span> <br/>   | <span data-ttu-id="b7b69-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="b7b69-122">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="b7b69-123">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b7b69-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7b69-124">Dokument</span><span class="sxs-lookup"><span data-stu-id="b7b69-124">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="b7b69-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7b69-125">Notes</span></span> <br/>          | <span data-ttu-id="b7b69-126">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und y-Achse bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="b7b69-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b7b69-127">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b7b69-127">Structural Content</span></span>

<span data-ttu-id="b7b69-128">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7b69-128">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b7b69-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="b7b69-129">Structure Variables</span></span>

<span data-ttu-id="b7b69-130">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b7b69-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7b69-131">Name</span><span class="sxs-lookup"><span data-stu-id="b7b69-131">Name</span></span>                                           | <span data-ttu-id="b7b69-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b7b69-132">Data type</span></span>          | <span data-ttu-id="b7b69-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="b7b69-133">Unit</span></span>                     | <span data-ttu-id="b7b69-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="b7b69-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b7b69-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b7b69-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b69-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="b7b69-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="b7b69-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b7b69-137">string</span></span><br/>  | <span data-ttu-id="b7b69-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b7b69-138">characters</span></span><br/>    | <span data-ttu-id="b7b69-139">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="b7b69-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7b69-140">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="b7b69-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7b69-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="b7b69-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="b7b69-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b7b69-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="b7b69-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b7b69-143">string</span></span><br/>  | <span data-ttu-id="b7b69-144">–</span><span class="sxs-lookup"><span data-stu-id="b7b69-144">n/a</span></span><br/>           | <span data-ttu-id="b7b69-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="b7b69-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b7b69-146">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b7b69-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="b7b69-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="b7b69-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="b7b69-148">integer</span><span class="sxs-lookup"><span data-stu-id="b7b69-148">integer</span></span><br/> | <span data-ttu-id="b7b69-149">Logische Seiten</span><span class="sxs-lookup"><span data-stu-id="b7b69-149">Logical pages</span></span><br/> | <span data-ttu-id="b7b69-150">Alle ganzen Zahlen (größer als Null).</span><span class="sxs-lookup"><span data-stu-id="b7b69-150">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="b7b69-151">Gibt die Anzahl logischer Seiten pro physischem Blatt an.</span><span class="sxs-lookup"><span data-stu-id="b7b69-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="b7b69-152">Der unterstützte Satz kann ein beliebiger Satz von ganzen Zahlen sein, z. B.</span><span class="sxs-lookup"><span data-stu-id="b7b69-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="b7b69-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="b7b69-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="b7b69-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="b7b69-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="b7b69-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b7b69-155">string</span></span><br/>  | <span data-ttu-id="b7b69-156">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b7b69-156">characters</span></span><br/>    | <span data-ttu-id="b7b69-157">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="b7b69-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7b69-158">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="b7b69-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7b69-159">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="b7b69-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b7b69-160">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="b7b69-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b7b69-161">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="b7b69-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b7b69-162">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="b7b69-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b7b69-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7b69-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7b69-164">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b7b69-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




