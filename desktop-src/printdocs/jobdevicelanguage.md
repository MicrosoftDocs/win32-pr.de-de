---
description: Erfahren Sie mehr über das JobDeviceLanguage-Element, das die Gerätesprachen beschreibt, die zum Senden von Daten vom Treiber an ein physisches Gerät unterstützt werden.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408994"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="44c3d-103">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="44c3d-103">JobDeviceLanguage</span></span>

<span data-ttu-id="44c3d-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="44c3d-104">This topic is not current.</span></span> <span data-ttu-id="44c3d-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="44c3d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="44c3d-106">Beschreibt die Gerätesprachen, die zum Senden von Daten vom Treiber an ein physisches Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="44c3d-106">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="44c3d-107">Dies wird häufig als "Sprache der Seitenbeschreibung" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44c3d-107">This is often called "Page Description Language".</span></span> <span data-ttu-id="44c3d-108">Dieses Schlüsselwort definiert, welche Seitenbeschreibungssprache vom Treiber und vom physischen Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="44c3d-108">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="44c3d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="44c3d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="44c3d-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="44c3d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="44c3d-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="44c3d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="44c3d-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="44c3d-112">Element Information</span></span>



| <span data-ttu-id="44c3d-113">Name</span><span class="sxs-lookup"><span data-stu-id="44c3d-113">Name</span></span> | <span data-ttu-id="44c3d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="44c3d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="44c3d-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="44c3d-115">Element Type</span></span> <br/>   | <span data-ttu-id="44c3d-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="44c3d-116">Feature</span></span><br/> |
| <span data-ttu-id="44c3d-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="44c3d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="44c3d-118">Auftrag</span><span class="sxs-lookup"><span data-stu-id="44c3d-118">Job</span></span><br/>     |
| <span data-ttu-id="44c3d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44c3d-119">Notes</span></span> <br/>          | <span data-ttu-id="44c3d-120">Keine</span><span class="sxs-lookup"><span data-stu-id="44c3d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="44c3d-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="44c3d-121">Structural Content</span></span>

<span data-ttu-id="44c3d-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="44c3d-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="44c3d-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="44c3d-123">Structure Variables</span></span>

<span data-ttu-id="44c3d-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44c3d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="44c3d-125">Name</span><span class="sxs-lookup"><span data-stu-id="44c3d-125">Name</span></span>                                 | <span data-ttu-id="44c3d-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="44c3d-126">Data type</span></span>         | <span data-ttu-id="44c3d-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="44c3d-127">Unit</span></span>                  | <span data-ttu-id="44c3d-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="44c3d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="44c3d-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="44c3d-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="44c3d-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="44c3d-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="44c3d-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44c3d-131">string</span></span><br/> | <span data-ttu-id="44c3d-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="44c3d-132">characters</span></span><br/> | <span data-ttu-id="44c3d-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="44c3d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="44c3d-134">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="44c3d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="44c3d-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="44c3d-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="44c3d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="44c3d-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="44c3d-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44c3d-137">string</span></span><br/> | <span data-ttu-id="44c3d-138">–</span><span class="sxs-lookup"><span data-stu-id="44c3d-138">n/a</span></span><br/>        | <span data-ttu-id="44c3d-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="44c3d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="44c3d-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="44c3d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="44c3d-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="44c3d-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="44c3d-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44c3d-142">string</span></span><br/> | <span data-ttu-id="44c3d-143">–</span><span class="sxs-lookup"><span data-stu-id="44c3d-143">n/a</span></span><br/>        | <span data-ttu-id="44c3d-144">Keine.</span><span class="sxs-lookup"><span data-stu-id="44c3d-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="44c3d-145">Gibt die Sprachebene an (z. B. PS Level 2).</span><span class="sxs-lookup"><span data-stu-id="44c3d-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="44c3d-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="44c3d-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="44c3d-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44c3d-147">string</span></span><br/> | <span data-ttu-id="44c3d-148">–</span><span class="sxs-lookup"><span data-stu-id="44c3d-148">n/a</span></span><br/>        | <span data-ttu-id="44c3d-149">Keine.</span><span class="sxs-lookup"><span data-stu-id="44c3d-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="44c3d-150">Gibt die Sprachcodierung an (z. B. ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="44c3d-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="44c3d-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="44c3d-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="44c3d-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44c3d-152">string</span></span><br/> | <span data-ttu-id="44c3d-153">–</span><span class="sxs-lookup"><span data-stu-id="44c3d-153">n/a</span></span><br/>        | <span data-ttu-id="44c3d-154">Keine.</span><span class="sxs-lookup"><span data-stu-id="44c3d-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="44c3d-155">Gibt die Sprachversion an.</span><span class="sxs-lookup"><span data-stu-id="44c3d-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="44c3d-156">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="44c3d-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="44c3d-157">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="44c3d-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="44c3d-158">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="44c3d-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="44c3d-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44c3d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c3d-160">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="44c3d-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




