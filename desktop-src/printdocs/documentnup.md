---
description: Erfahren Sie mehr über das DocumentNUp-Element, das die Ausgabe und das Format mehrerer logischer Seiten für ein einzelnes physisches Blatt beschreibt.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b49bd4fa3eb9f2b3b0083fc8022dbd6f41d090e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409263"
---
# <a name="documentnup"></a><span data-ttu-id="458b4-103">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="458b4-103">DocumentNUp</span></span>

<span data-ttu-id="458b4-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="458b4-104">This topic is not current.</span></span> <span data-ttu-id="458b4-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="458b4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="458b4-106">Beschreibt die Ausgabe und das Format mehrerer logischer Seiten zu einem einzelnen physischen Blatt.</span><span class="sxs-lookup"><span data-stu-id="458b4-106">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="458b4-107">Jedes Dokument wird separat kompiliert.</span><span class="sxs-lookup"><span data-stu-id="458b4-107">Each document is compiled separately.</span></span> <span data-ttu-id="458b4-108">DocumentNUp und JobNUpAllDocumentsContiguously schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="458b4-108">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="458b4-109">Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="458b4-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="458b4-110">Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1 mit 3 Seiten und Dokument 2 mit 2 Seiten.</span><span class="sxs-lookup"><span data-stu-id="458b4-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="458b4-111">Jedes Dokument ist separat duplexed.</span><span class="sxs-lookup"><span data-stu-id="458b4-111">Each document is duplexed separately.</span></span> <span data-ttu-id="458b4-112">Die unten gezeigte Präsentationsrichtung ist die RightBottom-Option.</span><span class="sxs-lookup"><span data-stu-id="458b4-112">The presentation direction shown below is the RightBottom option.</span></span>

![Diagramm, das zeigt, wie Dokumentseiten basierend auf der DocumentNup-Einstellung auf einem einzelnen Blatt angeordnet werden](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="458b4-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="458b4-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="458b4-115">Strukturell</span><span class="sxs-lookup"><span data-stu-id="458b4-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="458b4-116">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="458b4-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="458b4-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="458b4-117">Element Information</span></span>



| <span data-ttu-id="458b4-118">Name</span><span class="sxs-lookup"><span data-stu-id="458b4-118">Name</span></span> | <span data-ttu-id="458b4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="458b4-119">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="458b4-120">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="458b4-120">Element Type</span></span> <br/>   | <span data-ttu-id="458b4-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="458b4-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="458b4-122">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="458b4-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="458b4-123">Dokument</span><span class="sxs-lookup"><span data-stu-id="458b4-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="458b4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="458b4-124">Notes</span></span> <br/>          | <span data-ttu-id="458b4-125">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="458b4-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="458b4-126">Strukturell</span><span class="sxs-lookup"><span data-stu-id="458b4-126">Structural Content</span></span>

<span data-ttu-id="458b4-127">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="458b4-127">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="458b4-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="458b4-128">Structure Variables</span></span>

<span data-ttu-id="458b4-129">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="458b4-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="458b4-130">Name</span><span class="sxs-lookup"><span data-stu-id="458b4-130">Name</span></span>                                           | <span data-ttu-id="458b4-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="458b4-131">Data type</span></span>          | <span data-ttu-id="458b4-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="458b4-132">Unit</span></span>                     | <span data-ttu-id="458b4-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="458b4-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="458b4-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="458b4-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="458b4-135">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="458b4-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="458b4-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="458b4-136">string</span></span><br/>  | <span data-ttu-id="458b4-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="458b4-137">characters</span></span><br/>    | <span data-ttu-id="458b4-138">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="458b4-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="458b4-139">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="458b4-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="458b4-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="458b4-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="458b4-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="458b4-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="458b4-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="458b4-142">string</span></span><br/>  | <span data-ttu-id="458b4-143">–</span><span class="sxs-lookup"><span data-stu-id="458b4-143">n/a</span></span><br/>           | <span data-ttu-id="458b4-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="458b4-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="458b4-145">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="458b4-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="458b4-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="458b4-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="458b4-147">integer</span><span class="sxs-lookup"><span data-stu-id="458b4-147">integer</span></span><br/> | <span data-ttu-id="458b4-148">Logische Seiten</span><span class="sxs-lookup"><span data-stu-id="458b4-148">Logical pages</span></span><br/> | <span data-ttu-id="458b4-149">Alle ganzen Zahlen (größer als Null).</span><span class="sxs-lookup"><span data-stu-id="458b4-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="458b4-150">Gibt die Anzahl logischer Seiten pro physischem Blatt an.</span><span class="sxs-lookup"><span data-stu-id="458b4-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="458b4-151">Der unterstützte Satz kann ein beliebiger Satz von ganzen Zahlen sein, z. B.</span><span class="sxs-lookup"><span data-stu-id="458b4-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="458b4-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="458b4-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="458b4-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="458b4-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="458b4-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="458b4-154">string</span></span><br/>  | <span data-ttu-id="458b4-155">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="458b4-155">characters</span></span><br/>    | <span data-ttu-id="458b4-156">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="458b4-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="458b4-157">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="458b4-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="458b4-158">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="458b4-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="458b4-159">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="458b4-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="458b4-160">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="458b4-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="458b4-161">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="458b4-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="458b4-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="458b4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="458b4-163">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="458b4-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




