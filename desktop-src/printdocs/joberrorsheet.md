---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6724e72a9351efc1d3cc5912b9806fb8d65a85
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998147"
---
# <a name="joberrorsheet"></a><span data-ttu-id="df7d8-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="df7d8-104">JobErrorSheet</span></span>

<span data-ttu-id="df7d8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="df7d8-105">This topic is not current.</span></span> <span data-ttu-id="df7d8-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="df7d8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df7d8-107">Beschreibt die Ausgabe des Fehlerblatts.</span><span class="sxs-lookup"><span data-stu-id="df7d8-107">Describes the error sheet output.</span></span> <span data-ttu-id="df7d8-108">Der gesamte Auftrag hat ein einzelnes Fehlerblatt.</span><span class="sxs-lookup"><span data-stu-id="df7d8-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="df7d8-109">Das Fehlerblatt sollte in der Standardeinstellung PageMediaSize und unter Verwendung des Standardmäßigen PageMediaType ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="df7d8-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="df7d8-110">Das Fehlerblatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="df7d8-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="df7d8-111">Dies bedeutet, dass alle End- oder Verarbeitungsoptionen (z. B. JobDuplex, JobStaple oder JobBinding) das Fehlerblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="df7d8-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="df7d8-112">Das Fehlerblatt sollte als letztes Blatt des Auftrags auftreten.</span><span class="sxs-lookup"><span data-stu-id="df7d8-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="df7d8-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df7d8-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="df7d8-114">Strukturell</span><span class="sxs-lookup"><span data-stu-id="df7d8-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="df7d8-115">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="df7d8-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="df7d8-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df7d8-116">Element Information</span></span>



| <span data-ttu-id="df7d8-117">Name</span><span class="sxs-lookup"><span data-stu-id="df7d8-117">Name</span></span> | <span data-ttu-id="df7d8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="df7d8-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7d8-119">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="df7d8-119">Element Type</span></span> <br/>   | <span data-ttu-id="df7d8-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="df7d8-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="df7d8-121">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="df7d8-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="df7d8-122">Auftrag</span><span class="sxs-lookup"><span data-stu-id="df7d8-122">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="df7d8-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df7d8-123">Notes</span></span> <br/>          | <span data-ttu-id="df7d8-124">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="df7d8-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="df7d8-125">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="df7d8-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="df7d8-126">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="df7d8-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="df7d8-127">URIs, auf die in einem Dokument mit Druckfunktionen oder in PrintTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="df7d8-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="df7d8-128">Dies ist unsicher, da sie möglicherweise nicht wie vorgesehen aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="df7d8-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="df7d8-129">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="df7d8-129">Structural Content</span></span>

<span data-ttu-id="df7d8-130">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="df7d8-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="df7d8-131">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="df7d8-131">Structure Variables</span></span>

<span data-ttu-id="df7d8-132">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="df7d8-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="df7d8-133">Name</span><span class="sxs-lookup"><span data-stu-id="df7d8-133">Name</span></span>                                             | <span data-ttu-id="df7d8-134">Datentyp</span><span class="sxs-lookup"><span data-stu-id="df7d8-134">Data type</span></span>         | <span data-ttu-id="df7d8-135">Einheit</span><span class="sxs-lookup"><span data-stu-id="df7d8-135">Unit</span></span>                  | <span data-ttu-id="df7d8-136">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="df7d8-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="df7d8-137">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="df7d8-137">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="df7d8-138">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="df7d8-138">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="df7d8-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df7d8-139">string</span></span><br/> | <span data-ttu-id="df7d8-140">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="df7d8-140">characters</span></span><br/> | <span data-ttu-id="df7d8-141">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="df7d8-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="df7d8-142">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="df7d8-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="df7d8-143">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="df7d8-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="df7d8-144">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="df7d8-144">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="df7d8-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df7d8-145">string</span></span><br/> | <span data-ttu-id="df7d8-146">–</span><span class="sxs-lookup"><span data-stu-id="df7d8-146">n/a</span></span><br/>        | <span data-ttu-id="df7d8-147">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="df7d8-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="df7d8-148">Definiert die Auswahlkriterien für die Benutzeroberfläche (UI).</span><span class="sxs-lookup"><span data-stu-id="df7d8-148">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="df7d8-149">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="df7d8-149">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="df7d8-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df7d8-150">string</span></span><br/> | <span data-ttu-id="df7d8-151">–</span><span class="sxs-lookup"><span data-stu-id="df7d8-151">n/a</span></span><br/>        | <span data-ttu-id="df7d8-152">Gültiger vollqualifizierter Name, wie durch https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname definiert.</span><span class="sxs-lookup"><span data-stu-id="df7d8-152">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="df7d8-153">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="df7d8-153">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="df7d8-154">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="df7d8-154">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="df7d8-155">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="df7d8-155">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="df7d8-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df7d8-156">string</span></span><br/> | <span data-ttu-id="df7d8-157">–</span><span class="sxs-lookup"><span data-stu-id="df7d8-157">n/a</span></span><br/>        | <span data-ttu-id="df7d8-158">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="df7d8-158">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="df7d8-159">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="df7d8-159">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="df7d8-160">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="df7d8-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="df7d8-161">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="df7d8-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="df7d8-162">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="df7d8-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="df7d8-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df7d8-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df7d8-164">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="df7d8-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




