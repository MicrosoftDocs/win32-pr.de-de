---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3576611dcdc746342b8ed1b2c3d7ebf8fb779
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103961267"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="a69f0-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="a69f0-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="a69f0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a69f0-105">This topic is not current.</span></span> <span data-ttu-id="a69f0-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a69f0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a69f0-107">Beschreibt die Heften Merkmale der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a69f0-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="a69f0-108">Alle Dokumente im Auftrag werden mit einem heftet verknüpft.</span><span class="sxs-lookup"><span data-stu-id="a69f0-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="a69f0-109">Die Schlüsselwörter JobStapleAllDocuments und DocumentStaple schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="a69f0-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="a69f0-110">Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a69f0-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="a69f0-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a69f0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a69f0-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a69f0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a69f0-113">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a69f0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a69f0-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a69f0-114">Element Information</span></span>



| <span data-ttu-id="a69f0-115">Name</span><span class="sxs-lookup"><span data-stu-id="a69f0-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a69f0-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a69f0-116">Element Type</span></span> <br/>   | <span data-ttu-id="a69f0-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="a69f0-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="a69f0-118">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="a69f0-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a69f0-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a69f0-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="a69f0-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="a69f0-120">Notes</span></span> <br/>          | <span data-ttu-id="a69f0-121">"Top", "Bottom", "Left" und "Right" sind relativ zu PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a69f0-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a69f0-122">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a69f0-122">Structural Content</span></span>

<span data-ttu-id="a69f0-123">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a69f0-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="a69f0-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a69f0-124">Structure Variables</span></span>

<span data-ttu-id="a69f0-125">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a69f0-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a69f0-126">Name</span><span class="sxs-lookup"><span data-stu-id="a69f0-126">Name</span></span>                               | <span data-ttu-id="a69f0-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a69f0-127">Data type</span></span>          | <span data-ttu-id="a69f0-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="a69f0-128">Unit</span></span>                       | <span data-ttu-id="a69f0-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a69f0-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a69f0-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a69f0-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a69f0-131">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="a69f0-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a69f0-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a69f0-132">string</span></span><br/>  | <span data-ttu-id="a69f0-133">Zeichen</span><span class="sxs-lookup"><span data-stu-id="a69f0-133">Characters</span></span><br/>      | <span data-ttu-id="a69f0-134">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="a69f0-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a69f0-135">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a69f0-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a69f0-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="a69f0-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="a69f0-137">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="a69f0-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a69f0-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a69f0-138">string</span></span><br/>  | <span data-ttu-id="a69f0-139">–</span><span class="sxs-lookup"><span data-stu-id="a69f0-139">n/a</span></span><br/>             | <span data-ttu-id="a69f0-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a69f0-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a69f0-141">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a69f0-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="a69f0-142">\_Anglevalue\_</span><span class="sxs-lookup"><span data-stu-id="a69f0-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="a69f0-143">integer</span><span class="sxs-lookup"><span data-stu-id="a69f0-143">integer</span></span><br/> | <span data-ttu-id="a69f0-144">Grad</span><span class="sxs-lookup"><span data-stu-id="a69f0-144">degrees</span></span><br/>         | <span data-ttu-id="a69f0-145">Größer 0</span><span class="sxs-lookup"><span data-stu-id="a69f0-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a69f0-146">Gibt den Stapel Winkel relativ zur Breite von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="a69f0-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="a69f0-147">Der Stapel Winkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="a69f0-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="a69f0-148">\_Sheetcapacityvalue\_</span><span class="sxs-lookup"><span data-stu-id="a69f0-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="a69f0-149">integer</span><span class="sxs-lookup"><span data-stu-id="a69f0-149">integer</span></span><br/> | <span data-ttu-id="a69f0-150">Medien Blätter</span><span class="sxs-lookup"><span data-stu-id="a69f0-150">sheets of media</span></span><br/> | <span data-ttu-id="a69f0-151">Größer 0</span><span class="sxs-lookup"><span data-stu-id="a69f0-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a69f0-152">Gibt die Anzahl der Blätter an, die von der Heften-Option für den aktuell ausgewählten MediaType unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a69f0-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a69f0-153">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a69f0-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a69f0-154">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a69f0-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a69f0-155">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a69f0-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a69f0-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a69f0-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a69f0-157">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="a69f0-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




