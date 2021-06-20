---
description: Erfahren Sie mehr über das DocumentBinding-Element, das die Bindungsmethode beschreibt. DocumentBinding und JobBindAllDocuments schließen sich gegenseitig aus.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: DocumentBinding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf2b8f44c90cdef37a6599bf25904949748c82ba
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409463"
---
# <a name="documentbinding"></a><span data-ttu-id="e8a5b-104">DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="e8a5b-104">DocumentBinding</span></span>

<span data-ttu-id="e8a5b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-105">This topic is not current.</span></span> <span data-ttu-id="e8a5b-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e8a5b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8a5b-107">Beschreibt die Bindungsmethode.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-107">Describes the method of binding.</span></span> <span data-ttu-id="e8a5b-108">Jedes Dokument ist separat gebunden.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-108">Each document is bound separately.</span></span> <span data-ttu-id="e8a5b-109">DocumentBinding und JobBindAllDocuments schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="e8a5b-110">Es liegt an dem Treiber, die Einschränkungsbehandlung zwischen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="e8a5b-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e8a5b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e8a5b-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e8a5b-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e8a5b-113">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="e8a5b-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e8a5b-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e8a5b-114">Element Information</span></span>



| <span data-ttu-id="e8a5b-115">Name</span><span class="sxs-lookup"><span data-stu-id="e8a5b-115">Name</span></span> | <span data-ttu-id="e8a5b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e8a5b-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a5b-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e8a5b-117">Element Type</span></span> <br/>   | <span data-ttu-id="e8a5b-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="e8a5b-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e8a5b-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e8a5b-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e8a5b-120">Dokument</span><span class="sxs-lookup"><span data-stu-id="e8a5b-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="e8a5b-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8a5b-121">Notes</span></span> <br/>          | <span data-ttu-id="e8a5b-122">Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e8a5b-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e8a5b-123">Structural Content</span></span>

<span data-ttu-id="e8a5b-124">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e8a5b-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e8a5b-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e8a5b-125">Structure Variables</span></span>

<span data-ttu-id="e8a5b-126">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e8a5b-127">Name</span><span class="sxs-lookup"><span data-stu-id="e8a5b-127">Name</span></span>                               | <span data-ttu-id="e8a5b-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e8a5b-128">Data type</span></span>          | <span data-ttu-id="e8a5b-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="e8a5b-129">Unit</span></span>                  | <span data-ttu-id="e8a5b-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e8a5b-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e8a5b-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e8a5b-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a5b-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="e8a5b-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e8a5b-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e8a5b-133">string</span></span><br/>  | <span data-ttu-id="e8a5b-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e8a5b-134">characters</span></span><br/> | <span data-ttu-id="e8a5b-135">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e8a5b-136">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e8a5b-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e8a5b-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e8a5b-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e8a5b-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e8a5b-139">string</span></span><br/>  | <span data-ttu-id="e8a5b-140">–</span><span class="sxs-lookup"><span data-stu-id="e8a5b-140">n/a</span></span><br/>        | <span data-ttu-id="e8a5b-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="e8a5b-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e8a5b-142">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="e8a5b-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="e8a5b-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="e8a5b-144">Integer</span><span class="sxs-lookup"><span data-stu-id="e8a5b-144">Integer</span></span><br/> | <span data-ttu-id="e8a5b-145">Mikron</span><span class="sxs-lookup"><span data-stu-id="e8a5b-145">microns</span></span><br/>    | <span data-ttu-id="e8a5b-146">Größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="e8a5b-147">Definiert den minimalen Bindungssteg für die angegebene Endbindung.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="e8a5b-148">Der Bundsteg wird relativ zum Rand der physischen Mediendimension in Mikron gemessen.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e8a5b-149">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="e8a5b-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e8a5b-150">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="e8a5b-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e8a5b-151">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="e8a5b-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e8a5b-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8a5b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a5b-153">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e8a5b-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




