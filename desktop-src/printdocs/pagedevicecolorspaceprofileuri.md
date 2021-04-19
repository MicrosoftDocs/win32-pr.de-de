---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: Pagede vicecolorspaceprofileuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357171"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="43833-104">Pagede vicecolorspaceprofileuri</span><span class="sxs-lookup"><span data-stu-id="43833-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="43833-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="43833-105">This topic is not current.</span></span> <span data-ttu-id="43833-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="43833-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="43833-107">Gibt einen relativen URI zum Paket Stamm an ein in einem XPS-Dokument enthaltenes ICC-Profil an.</span><span class="sxs-lookup"><span data-stu-id="43833-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="43833-108">Die Verarbeitung dieser Option hängt von der Einstellung der pagedevicecolorspaceusage-Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="43833-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="43833-109">Es wird davon ausgegangen, dass alle Elemente, die dieses Profil verwenden, sich bereits im entsprechenden Geräte Farbraum befinden und im Treiber oder Gerät nicht farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="43833-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="43833-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="43833-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="43833-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="43833-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="43833-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="43833-112">Element Information</span></span>



| <span data-ttu-id="43833-113">Name</span><span class="sxs-lookup"><span data-stu-id="43833-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43833-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="43833-114">Element Type</span></span> <br/>   | <span data-ttu-id="43833-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="43833-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="43833-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="43833-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="43833-117">Seite</span><span class="sxs-lookup"><span data-stu-id="43833-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="43833-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="43833-118">Notes</span></span> <br/>          | <span data-ttu-id="43833-119">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen Print Tickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43833-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="43833-120">XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="43833-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="43833-121">Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="43833-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="43833-122">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="43833-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="43833-123">URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="43833-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="43833-124">Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.</span><span class="sxs-lookup"><span data-stu-id="43833-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="43833-125">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="43833-125">Structure Content</span></span>

<span data-ttu-id="43833-126">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="43833-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="43833-127">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43833-127">Structure Properties</span></span>

<span data-ttu-id="43833-128">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="43833-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="43833-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="43833-129">Property</span></span>                | <span data-ttu-id="43833-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="43833-130">xsi:type</span></span>           | <span data-ttu-id="43833-131">Wert</span><span class="sxs-lookup"><span data-stu-id="43833-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="43833-132">DataType</span><span class="sxs-lookup"><span data-stu-id="43833-132">DataType</span></span><br/>     | <span data-ttu-id="43833-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43833-133">string</span></span><br/>  | <span data-ttu-id="43833-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="43833-134">xs:string</span></span><br/>       |
| <span data-ttu-id="43833-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="43833-135">DefaultValue</span></span><br/> | <span data-ttu-id="43833-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43833-136">string</span></span><br/>  | <span data-ttu-id="43833-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="43833-137">undefined</span></span><br/>       |
| <span data-ttu-id="43833-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="43833-138">MaxLength</span></span><br/>    | <span data-ttu-id="43833-139">integer</span><span class="sxs-lookup"><span data-stu-id="43833-139">integer</span></span><br/> | <span data-ttu-id="43833-140">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="43833-140">undefined</span></span><br/>       |
| <span data-ttu-id="43833-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="43833-141">MinLength</span></span><br/>    | <span data-ttu-id="43833-142">integer</span><span class="sxs-lookup"><span data-stu-id="43833-142">integer</span></span><br/> | <span data-ttu-id="43833-143">1</span><span class="sxs-lookup"><span data-stu-id="43833-143">1</span></span><br/>               |
| <span data-ttu-id="43833-144">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="43833-144">Mandatory</span></span><br/>    | <span data-ttu-id="43833-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43833-145">string</span></span><br/>  | <span data-ttu-id="43833-146">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="43833-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="43833-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="43833-147">UnitType</span></span><br/>     | <span data-ttu-id="43833-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43833-148">string</span></span><br/>  | <span data-ttu-id="43833-149">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="43833-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="43833-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43833-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43833-151">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="43833-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




