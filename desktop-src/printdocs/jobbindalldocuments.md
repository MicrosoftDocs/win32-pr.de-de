---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: Jobbindalldocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b0067e737168bc70b712eaf16ce712446510923
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106354294"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="b019f-104">Jobbindalldocuments</span><span class="sxs-lookup"><span data-stu-id="b019f-104">JobBindAllDocuments</span></span>

<span data-ttu-id="b019f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b019f-105">This topic is not current.</span></span> <span data-ttu-id="b019f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b019f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b019f-107">Beschreibt die Bindungsmethode.</span><span class="sxs-lookup"><span data-stu-id="b019f-107">Describes the method of binding.</span></span> <span data-ttu-id="b019f-108">Alle Dokumente im Auftrag werden gleich gebunden.</span><span class="sxs-lookup"><span data-stu-id="b019f-108">All documents in the job are bound together.</span></span> <span data-ttu-id="b019f-109">Jobbindalldocuments und documentbinding schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="b019f-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="b019f-110">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b019f-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="b019f-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b019f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b019f-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b019f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b019f-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b019f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b019f-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b019f-114">Element Information</span></span>



| <span data-ttu-id="b019f-115">Name</span><span class="sxs-lookup"><span data-stu-id="b019f-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b019f-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b019f-116">Element Type</span></span> <br/>   | <span data-ttu-id="b019f-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="b019f-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="b019f-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="b019f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b019f-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b019f-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="b019f-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b019f-120">Notes</span></span> <br/>          | <span data-ttu-id="b019f-121">"Top", "Bottom", "Left" und "Right" sind relativ zu "PageImageableSize".</span><span class="sxs-lookup"><span data-stu-id="b019f-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b019f-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b019f-122">Structural Content</span></span>

<span data-ttu-id="b019f-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="b019f-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b019f-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="b019f-124">Structure Variables</span></span>

<span data-ttu-id="b019f-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b019f-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b019f-126">Name</span><span class="sxs-lookup"><span data-stu-id="b019f-126">Name</span></span>                               | <span data-ttu-id="b019f-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b019f-127">Data type</span></span>          | <span data-ttu-id="b019f-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="b019f-128">Unit</span></span>                  | <span data-ttu-id="b019f-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="b019f-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b019f-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b019f-130">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b019f-131">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="b019f-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b019f-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b019f-132">string</span></span><br/>  | <span data-ttu-id="b019f-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b019f-133">characters</span></span><br/> | <span data-ttu-id="b019f-134">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="b019f-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b019f-135">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="b019f-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b019f-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="b019f-136">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="b019f-137">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="b019f-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b019f-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b019f-138">string</span></span><br/>  | <span data-ttu-id="b019f-139">–</span><span class="sxs-lookup"><span data-stu-id="b019f-139">n/a</span></span><br/>        | <span data-ttu-id="b019f-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="b019f-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b019f-141">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b019f-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="b019f-142">\_Bindingguttervalue\_</span><span class="sxs-lookup"><span data-stu-id="b019f-142">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="b019f-143">integer</span><span class="sxs-lookup"><span data-stu-id="b019f-143">integer</span></span><br/> | <span data-ttu-id="b019f-144">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="b019f-144">microns</span></span><br/>    | <span data-ttu-id="b019f-145">Größer 0</span><span class="sxs-lookup"><span data-stu-id="b019f-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="b019f-146">Definiert den minimalen Bindungs bundbundpunkt für die angegebene abschließende Bindung.</span><span class="sxs-lookup"><span data-stu-id="b019f-146">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="b019f-147">Der bundstein wird in Mikrometern relativ zum Rand der physischen Medien Dimension gemessen.</span><span class="sxs-lookup"><span data-stu-id="b019f-147">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b019f-148">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b019f-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b019f-149">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="b019f-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b019f-150">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="b019f-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b019f-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b019f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b019f-152">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b019f-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




