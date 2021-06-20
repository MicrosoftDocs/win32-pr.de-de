---
description: Erfahren Sie mehr über das JobAccountingSheet-Element, das das Buchhaltungsblatt beschreibt, das für den Auftrag ausgegeben werden soll.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409094"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="15da8-103">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="15da8-103">JobAccountingSheet</span></span>

<span data-ttu-id="15da8-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="15da8-104">This topic is not current.</span></span> <span data-ttu-id="15da8-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="15da8-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15da8-106">Beschreibt das Buchhaltungsblatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="15da8-106">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="15da8-107">Das Buchhaltungsblatt sollte in der Standardeinstellung PageMediaSize und unter Verwendung des Standardmäßigen PageMediaType ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15da8-107">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="15da8-108">Das Buchhaltungsblatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="15da8-108">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="15da8-109">Dies bedeutet, dass alle Abschluss- oder Verarbeitungsoptionen (z. B. JobDuplex, JobStaple oder JobBinding) das Buchhaltungsblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="15da8-109">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="15da8-110">Das Buchhaltungsblatt kann nach Ermessen des Implementers als erste oder letzte Seite des Auftrags angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15da8-110">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="15da8-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15da8-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="15da8-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="15da8-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="15da8-113">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="15da8-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="15da8-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15da8-114">Element Information</span></span>



| <span data-ttu-id="15da8-115">Name</span><span class="sxs-lookup"><span data-stu-id="15da8-115">Name</span></span> | <span data-ttu-id="15da8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="15da8-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="15da8-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="15da8-117">Element Type</span></span> <br/>   | <span data-ttu-id="15da8-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="15da8-118">Feature</span></span><br/> |
| <span data-ttu-id="15da8-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="15da8-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15da8-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="15da8-120">Job</span></span><br/>     |
| <span data-ttu-id="15da8-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15da8-121">Notes</span></span> <br/>          | <span data-ttu-id="15da8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="15da8-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="15da8-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="15da8-123">Structural Content</span></span>

<span data-ttu-id="15da8-124">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="15da8-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="15da8-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="15da8-125">Structure Variables</span></span>

<span data-ttu-id="15da8-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="15da8-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15da8-127">Name</span><span class="sxs-lookup"><span data-stu-id="15da8-127">Name</span></span>                               | <span data-ttu-id="15da8-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="15da8-128">Data type</span></span>         | <span data-ttu-id="15da8-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="15da8-129">Unit</span></span>                  | <span data-ttu-id="15da8-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="15da8-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="15da8-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="15da8-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="15da8-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="15da8-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="15da8-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15da8-133">string</span></span><br/> | <span data-ttu-id="15da8-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="15da8-134">characters</span></span><br/> | <span data-ttu-id="15da8-135">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="15da8-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="15da8-136">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="15da8-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="15da8-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="15da8-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="15da8-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15da8-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="15da8-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15da8-139">string</span></span><br/> | <span data-ttu-id="15da8-140">–</span><span class="sxs-lookup"><span data-stu-id="15da8-140">n/a</span></span><br/>        | <span data-ttu-id="15da8-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="15da8-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="15da8-142">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="15da8-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="15da8-143">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="15da8-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="15da8-144">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="15da8-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="15da8-145">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="15da8-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="15da8-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15da8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15da8-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="15da8-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




