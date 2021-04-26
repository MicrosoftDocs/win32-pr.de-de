---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998427"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="5d19d-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="5d19d-104">JobAccountingSheet</span></span>

<span data-ttu-id="5d19d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5d19d-105">This topic is not current.</span></span> <span data-ttu-id="5d19d-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5d19d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d19d-107">Beschreibt das Buchhaltungsblatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d19d-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="5d19d-108">Das Buchhaltungsblatt sollte in der Standardeinstellung PageMediaSize und unter Verwendung des Standardmäßigen PageMediaType ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5d19d-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="5d19d-109">Das Buchhaltungsblatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="5d19d-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="5d19d-110">Dies bedeutet, dass alle Abschluss- oder Verarbeitungsoptionen (z. B. JobDuplex, JobStaple oder JobBinding) das Buchhaltungsblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="5d19d-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="5d19d-111">Das Buchhaltungsblatt kann nach Ermessen des Implementers als erste oder letzte Seite des Auftrags angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5d19d-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="5d19d-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5d19d-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5d19d-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5d19d-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5d19d-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5d19d-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5d19d-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5d19d-115">Element Information</span></span>



| <span data-ttu-id="5d19d-116">Name</span><span class="sxs-lookup"><span data-stu-id="5d19d-116">Name</span></span> | <span data-ttu-id="5d19d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5d19d-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5d19d-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5d19d-118">Element Type</span></span> <br/>   | <span data-ttu-id="5d19d-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="5d19d-119">Feature</span></span><br/> |
| <span data-ttu-id="5d19d-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5d19d-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5d19d-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5d19d-121">Job</span></span><br/>     |
| <span data-ttu-id="5d19d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d19d-122">Notes</span></span> <br/>          | <span data-ttu-id="5d19d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="5d19d-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5d19d-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="5d19d-124">Structural Content</span></span>

<span data-ttu-id="5d19d-125">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="5d19d-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="5d19d-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="5d19d-126">Structure Variables</span></span>

<span data-ttu-id="5d19d-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5d19d-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5d19d-128">Name</span><span class="sxs-lookup"><span data-stu-id="5d19d-128">Name</span></span>                               | <span data-ttu-id="5d19d-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d19d-129">Data type</span></span>         | <span data-ttu-id="5d19d-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="5d19d-130">Unit</span></span>                  | <span data-ttu-id="5d19d-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="5d19d-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5d19d-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5d19d-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5d19d-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="5d19d-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5d19d-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d19d-134">string</span></span><br/> | <span data-ttu-id="5d19d-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5d19d-135">characters</span></span><br/> | <span data-ttu-id="5d19d-136">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5d19d-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5d19d-137">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5d19d-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="5d19d-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5d19d-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5d19d-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5d19d-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d19d-140">string</span></span><br/> | <span data-ttu-id="5d19d-141">–</span><span class="sxs-lookup"><span data-stu-id="5d19d-141">n/a</span></span><br/>        | <span data-ttu-id="5d19d-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="5d19d-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5d19d-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5d19d-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5d19d-144">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="5d19d-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5d19d-145">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="5d19d-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5d19d-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="5d19d-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="5d19d-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d19d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d19d-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5d19d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




