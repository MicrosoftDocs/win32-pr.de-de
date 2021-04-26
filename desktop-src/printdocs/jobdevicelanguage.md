---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b9f85b44ae9fdc6efb66ce5b72bb68c5187790
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998297"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="e21a4-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="e21a4-104">JobDeviceLanguage</span></span>

<span data-ttu-id="e21a4-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e21a4-105">This topic is not current.</span></span> <span data-ttu-id="e21a4-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e21a4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e21a4-107">Beschreibt die Gerätesprachen, die zum Senden von Daten vom Treiber an ein physisches Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e21a4-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="e21a4-108">Dies wird häufig als "Sprache der Seitenbeschreibung" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e21a4-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="e21a4-109">Dieses Schlüsselwort definiert, welche Seitenbeschreibungssprache vom Treiber und vom physischen Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e21a4-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="e21a4-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e21a4-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e21a4-111">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e21a4-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e21a4-112">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="e21a4-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e21a4-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e21a4-113">Element Information</span></span>



| <span data-ttu-id="e21a4-114">Name</span><span class="sxs-lookup"><span data-stu-id="e21a4-114">Name</span></span> | <span data-ttu-id="e21a4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e21a4-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e21a4-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e21a4-116">Element Type</span></span> <br/>   | <span data-ttu-id="e21a4-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="e21a4-117">Feature</span></span><br/> |
| <span data-ttu-id="e21a4-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e21a4-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e21a4-119">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e21a4-119">Job</span></span><br/>     |
| <span data-ttu-id="e21a4-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e21a4-120">Notes</span></span> <br/>          | <span data-ttu-id="e21a4-121">Keine</span><span class="sxs-lookup"><span data-stu-id="e21a4-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e21a4-122">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e21a4-122">Structural Content</span></span>

<span data-ttu-id="e21a4-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="e21a4-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="e21a4-124">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e21a4-124">Structure Variables</span></span>

<span data-ttu-id="e21a4-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e21a4-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e21a4-126">Name</span><span class="sxs-lookup"><span data-stu-id="e21a4-126">Name</span></span>                                 | <span data-ttu-id="e21a4-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e21a4-127">Data type</span></span>         | <span data-ttu-id="e21a4-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="e21a4-128">Unit</span></span>                  | <span data-ttu-id="e21a4-129">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e21a4-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e21a4-130">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e21a4-130">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e21a4-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="e21a4-131">\_OptionName\_</span></span><br/>            | <span data-ttu-id="e21a4-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e21a4-132">string</span></span><br/> | <span data-ttu-id="e21a4-133">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e21a4-133">characters</span></span><br/> | <span data-ttu-id="e21a4-134">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="e21a4-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e21a4-135">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="e21a4-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e21a4-136">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="e21a4-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e21a4-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e21a4-137">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="e21a4-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e21a4-138">string</span></span><br/> | <span data-ttu-id="e21a4-139">–</span><span class="sxs-lookup"><span data-stu-id="e21a4-139">n/a</span></span><br/>        | <span data-ttu-id="e21a4-140">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="e21a4-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e21a4-141">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e21a4-141">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="e21a4-142">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="e21a4-142">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="e21a4-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e21a4-143">string</span></span><br/> | <span data-ttu-id="e21a4-144">–</span><span class="sxs-lookup"><span data-stu-id="e21a4-144">n/a</span></span><br/>        | <span data-ttu-id="e21a4-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="e21a4-145">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="e21a4-146">Gibt die Sprachebene an (z. B. PS Level 2).</span><span class="sxs-lookup"><span data-stu-id="e21a4-146">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="e21a4-147">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="e21a4-147">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="e21a4-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e21a4-148">string</span></span><br/> | <span data-ttu-id="e21a4-149">–</span><span class="sxs-lookup"><span data-stu-id="e21a4-149">n/a</span></span><br/>        | <span data-ttu-id="e21a4-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="e21a4-150">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="e21a4-151">Gibt die Sprachcodierung an (z. B. ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="e21a4-151">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="e21a4-152">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="e21a4-152">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="e21a4-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e21a4-153">string</span></span><br/> | <span data-ttu-id="e21a4-154">–</span><span class="sxs-lookup"><span data-stu-id="e21a4-154">n/a</span></span><br/>        | <span data-ttu-id="e21a4-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="e21a4-155">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="e21a4-156">Gibt die Sprachversion an.</span><span class="sxs-lookup"><span data-stu-id="e21a4-156">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e21a4-157">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e21a4-157">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e21a4-158">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="e21a4-158">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e21a4-159">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="e21a4-159">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="e21a4-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e21a4-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e21a4-161">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e21a4-161">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




