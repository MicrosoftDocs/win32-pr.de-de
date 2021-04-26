---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995677"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="c5764-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="c5764-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="c5764-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c5764-105">This topic is not current.</span></span> <span data-ttu-id="c5764-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c5764-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5764-107">Gibt einen relativen URI zum Paketstamm zu einem INTS-Profil an, das in einem XPS-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c5764-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="c5764-108">Die Verarbeitung dieser Option hängt von der Einstellung des Features PageDeviceColorSpaceUsage ab.</span><span class="sxs-lookup"><span data-stu-id="c5764-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="c5764-109">Es wird davon ausgegangen, dass sich alle Elemente, die dieses Profil verwenden, bereits im entsprechenden Gerätefarbraum befinden und nicht im Treiber oder Gerät farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c5764-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="c5764-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c5764-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c5764-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c5764-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c5764-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c5764-112">Element Information</span></span>



| <span data-ttu-id="c5764-113">Name</span><span class="sxs-lookup"><span data-stu-id="c5764-113">Name</span></span> | <span data-ttu-id="c5764-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c5764-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5764-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c5764-115">Element Type</span></span> <br/>   | <span data-ttu-id="c5764-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c5764-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c5764-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c5764-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c5764-118">Seite</span><span class="sxs-lookup"><span data-stu-id="c5764-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c5764-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5764-119">Notes</span></span> <br/>          | <span data-ttu-id="c5764-120">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5764-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="c5764-121">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="c5764-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c5764-122">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c5764-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c5764-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c5764-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c5764-124">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c5764-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c5764-125">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="c5764-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c5764-126">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c5764-126">Structure Content</span></span>

<span data-ttu-id="c5764-127">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="c5764-127">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c5764-128">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5764-128">Structure Properties</span></span>

<span data-ttu-id="c5764-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c5764-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c5764-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5764-130">Property</span></span>                | <span data-ttu-id="c5764-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c5764-131">xsi:type</span></span>           | <span data-ttu-id="c5764-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c5764-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c5764-133">DataType</span><span class="sxs-lookup"><span data-stu-id="c5764-133">DataType</span></span><br/>     | <span data-ttu-id="c5764-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5764-134">string</span></span><br/>  | <span data-ttu-id="c5764-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5764-135">xs:string</span></span><br/>       |
| <span data-ttu-id="c5764-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5764-136">DefaultValue</span></span><br/> | <span data-ttu-id="c5764-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5764-137">string</span></span><br/>  | <span data-ttu-id="c5764-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="c5764-138">undefined</span></span><br/>       |
| <span data-ttu-id="c5764-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c5764-139">MaxLength</span></span><br/>    | <span data-ttu-id="c5764-140">integer</span><span class="sxs-lookup"><span data-stu-id="c5764-140">integer</span></span><br/> | <span data-ttu-id="c5764-141">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="c5764-141">undefined</span></span><br/>       |
| <span data-ttu-id="c5764-142">Minlength</span><span class="sxs-lookup"><span data-stu-id="c5764-142">MinLength</span></span><br/>    | <span data-ttu-id="c5764-143">integer</span><span class="sxs-lookup"><span data-stu-id="c5764-143">integer</span></span><br/> | <span data-ttu-id="c5764-144">1</span><span class="sxs-lookup"><span data-stu-id="c5764-144">1</span></span><br/>               |
| <span data-ttu-id="c5764-145">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="c5764-145">Mandatory</span></span><br/>    | <span data-ttu-id="c5764-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5764-146">string</span></span><br/>  | <span data-ttu-id="c5764-147">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="c5764-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c5764-148">Unittype</span><span class="sxs-lookup"><span data-stu-id="c5764-148">UnitType</span></span><br/>     | <span data-ttu-id="c5764-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5764-149">string</span></span><br/>  | <span data-ttu-id="c5764-150">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c5764-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c5764-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5764-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5764-152">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c5764-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




