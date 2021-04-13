---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: Jobaccountingsheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6d906833dc067155c9d98d50ed47e898a446e2
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351908"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="0b6cf-104">Jobaccountingsheet</span><span class="sxs-lookup"><span data-stu-id="0b6cf-104">JobAccountingSheet</span></span>

<span data-ttu-id="0b6cf-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-105">This topic is not current.</span></span> <span data-ttu-id="0b6cf-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0b6cf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0b6cf-107">Beschreibt das Buchhaltungs Blatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="0b6cf-108">Das Buchhaltungs Blatt sollte auf der Standardseite PageMediaSize ausgegeben werden und den Standardwert PageMediaType verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="0b6cf-109">Das Buchhaltungs Blatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="0b6cf-110">Dies bedeutet, dass alle Beendigungs-oder Verarbeitungsoptionen (z. b. jobduplex, jobstaple oder jobbinding) kein Buchhaltungs Blatt enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="0b6cf-111">Das Buchhaltungs Blatt kann als erste oder letzte Seite des Auftrags nach dem Ermessen des Implementierers auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="0b6cf-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0b6cf-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0b6cf-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0b6cf-114">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0b6cf-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0b6cf-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-115">Element Information</span></span>



| <span data-ttu-id="0b6cf-116">Name</span><span class="sxs-lookup"><span data-stu-id="0b6cf-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="0b6cf-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0b6cf-117">Element Type</span></span> <br/>   | <span data-ttu-id="0b6cf-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="0b6cf-118">Feature</span></span><br/> |
| <span data-ttu-id="0b6cf-119">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="0b6cf-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0b6cf-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b6cf-120">Job</span></span><br/>     |
| <span data-ttu-id="0b6cf-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b6cf-121">Notes</span></span> <br/>          | <span data-ttu-id="0b6cf-122">Keine</span><span class="sxs-lookup"><span data-stu-id="0b6cf-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0b6cf-123">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0b6cf-123">Structural Content</span></span>

<span data-ttu-id="0b6cf-124">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="0b6cf-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0b6cf-125">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-125">Structure Variables</span></span>

<span data-ttu-id="0b6cf-126">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0b6cf-127">Name</span><span class="sxs-lookup"><span data-stu-id="0b6cf-127">Name</span></span>                               | <span data-ttu-id="0b6cf-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0b6cf-128">Data type</span></span>         | <span data-ttu-id="0b6cf-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="0b6cf-129">Unit</span></span>                  | <span data-ttu-id="0b6cf-130">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0b6cf-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0b6cf-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0b6cf-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0b6cf-132">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="0b6cf-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0b6cf-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b6cf-133">string</span></span><br/> | <span data-ttu-id="0b6cf-134">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0b6cf-134">characters</span></span><br/> | <span data-ttu-id="0b6cf-135">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0b6cf-136">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0b6cf-137">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0b6cf-138">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="0b6cf-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0b6cf-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b6cf-139">string</span></span><br/> | <span data-ttu-id="0b6cf-140">–</span><span class="sxs-lookup"><span data-stu-id="0b6cf-140">n/a</span></span><br/>        | <span data-ttu-id="0b6cf-141">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="0b6cf-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0b6cf-142">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0b6cf-143">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0b6cf-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0b6cf-144">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0b6cf-145">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="0b6cf-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0b6cf-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b6cf-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b6cf-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0b6cf-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




