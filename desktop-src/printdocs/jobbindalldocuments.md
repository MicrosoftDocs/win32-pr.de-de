---
description: Erfahren Sie mehr über das JobBindAllDocuments-Element, das beschreibt, wie die Methode der Bindung beschrieben wird. Alle Dokumente im Auftrag werden miteinander gebunden.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5abff455756b2abc1d84bf2cff470fa49c93278
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409083"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="a93be-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="a93be-104">JobBindAllDocuments</span></span>

<span data-ttu-id="a93be-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a93be-105">This topic is not current.</span></span> <span data-ttu-id="a93be-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a93be-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a93be-107">Beschreibt die Bindungsmethode.</span><span class="sxs-lookup"><span data-stu-id="a93be-107">Describes the method of binding.</span></span> <span data-ttu-id="a93be-108">Alle Dokumente im Auftrag werden miteinander gebunden.</span><span class="sxs-lookup"><span data-stu-id="a93be-108">All documents in the job are bound together.</span></span> <span data-ttu-id="a93be-109">JobBindAllDocuments und DocumentBinding schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="a93be-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="a93be-110">Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a93be-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="a93be-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a93be-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a93be-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a93be-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a93be-113">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="a93be-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a93be-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a93be-114">Element Information</span></span>



| <span data-ttu-id="a93be-115">Name</span><span class="sxs-lookup"><span data-stu-id="a93be-115">Name</span></span> | <span data-ttu-id="a93be-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a93be-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a93be-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a93be-117">Element Type</span></span> <br/>   | <span data-ttu-id="a93be-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="a93be-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="a93be-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a93be-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a93be-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a93be-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="a93be-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a93be-121">Notes</span></span> <br/>          | <span data-ttu-id="a93be-122">Top, Bottom, Left und Right sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a93be-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a93be-123">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a93be-123">Structural Content</span></span>

<span data-ttu-id="a93be-124">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a93be-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="a93be-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a93be-125">Structure Variables</span></span>

<span data-ttu-id="a93be-126">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a93be-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a93be-127">Name</span><span class="sxs-lookup"><span data-stu-id="a93be-127">Name</span></span>                               | <span data-ttu-id="a93be-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a93be-128">Data type</span></span>          | <span data-ttu-id="a93be-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="a93be-129">Unit</span></span>                  | <span data-ttu-id="a93be-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a93be-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a93be-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a93be-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93be-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a93be-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a93be-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a93be-133">string</span></span><br/>  | <span data-ttu-id="a93be-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a93be-134">characters</span></span><br/> | <span data-ttu-id="a93be-135">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a93be-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a93be-136">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a93be-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a93be-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a93be-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a93be-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a93be-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a93be-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a93be-139">string</span></span><br/>  | <span data-ttu-id="a93be-140">–</span><span class="sxs-lookup"><span data-stu-id="a93be-140">n/a</span></span><br/>        | <span data-ttu-id="a93be-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a93be-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a93be-142">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a93be-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="a93be-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="a93be-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="a93be-144">integer</span><span class="sxs-lookup"><span data-stu-id="a93be-144">integer</span></span><br/> | <span data-ttu-id="a93be-145">Mikron</span><span class="sxs-lookup"><span data-stu-id="a93be-145">microns</span></span><br/>    | <span data-ttu-id="a93be-146">Größer 0</span><span class="sxs-lookup"><span data-stu-id="a93be-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a93be-147">Definiert den minimalen Bindungssteg für die angegebene Endbindung.</span><span class="sxs-lookup"><span data-stu-id="a93be-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="a93be-148">Der Bundsteg wird relativ zum Rand der physischen Mediendimension in Mikron gemessen.</span><span class="sxs-lookup"><span data-stu-id="a93be-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a93be-149">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="a93be-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a93be-150">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a93be-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a93be-151">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a93be-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a93be-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a93be-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93be-153">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a93be-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




