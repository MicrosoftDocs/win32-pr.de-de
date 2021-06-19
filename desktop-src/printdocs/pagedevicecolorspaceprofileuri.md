---
description: Erfahren Sie mehr über den PageDeviceColorSpaceProfileURI-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396645"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="df943-105">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="df943-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="df943-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="df943-106">This topic is not current.</span></span> <span data-ttu-id="df943-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="df943-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df943-108">Gibt einen relativen URI zum Paketstamm zu einem in einem XPS-Dokument enthaltenen XPS-Profil an.</span><span class="sxs-lookup"><span data-stu-id="df943-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="df943-109">Die Verarbeitung dieser Option hängt von der Einstellung des PageDeviceColorSpaceUsage-Features ab.</span><span class="sxs-lookup"><span data-stu-id="df943-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="df943-110">Bei allen Elementen, die dieses Profil verwenden, wird davon ausgegangen, dass sie sich bereits im entsprechenden Gerätefarbraum befinden und im Treiber oder Gerät nicht farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="df943-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="df943-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df943-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="df943-112">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="df943-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="df943-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df943-113">Element Information</span></span>



| <span data-ttu-id="df943-114">Name</span><span class="sxs-lookup"><span data-stu-id="df943-114">Name</span></span> | <span data-ttu-id="df943-115">Wert</span><span class="sxs-lookup"><span data-stu-id="df943-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df943-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="df943-116">Element Type</span></span> <br/>   | <span data-ttu-id="df943-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="df943-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="df943-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="df943-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="df943-119">Seite</span><span class="sxs-lookup"><span data-stu-id="df943-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="df943-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df943-120">Notes</span></span> <br/>          | <span data-ttu-id="df943-121">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df943-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="df943-122">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="df943-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="df943-123">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="df943-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="df943-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="df943-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="df943-125">URIs, auf die in einem Dokument mit Druckfunktionen oder in PrintTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="df943-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="df943-126">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="df943-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="df943-127">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="df943-127">Structure Content</span></span>

<span data-ttu-id="df943-128">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="df943-128">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="df943-129">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="df943-129">Structure Properties</span></span>

<span data-ttu-id="df943-130">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df943-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="df943-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df943-131">Property</span></span>                | <span data-ttu-id="df943-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="df943-132">xsi:type</span></span>           | <span data-ttu-id="df943-133">Wert</span><span class="sxs-lookup"><span data-stu-id="df943-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="df943-134">DataType</span><span class="sxs-lookup"><span data-stu-id="df943-134">DataType</span></span><br/>     | <span data-ttu-id="df943-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df943-135">string</span></span><br/>  | <span data-ttu-id="df943-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="df943-136">xs:string</span></span><br/>       |
| <span data-ttu-id="df943-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="df943-137">DefaultValue</span></span><br/> | <span data-ttu-id="df943-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df943-138">string</span></span><br/>  | <span data-ttu-id="df943-139">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="df943-139">undefined</span></span><br/>       |
| <span data-ttu-id="df943-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="df943-140">MaxLength</span></span><br/>    | <span data-ttu-id="df943-141">integer</span><span class="sxs-lookup"><span data-stu-id="df943-141">integer</span></span><br/> | <span data-ttu-id="df943-142">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="df943-142">undefined</span></span><br/>       |
| <span data-ttu-id="df943-143">Minlength</span><span class="sxs-lookup"><span data-stu-id="df943-143">MinLength</span></span><br/>    | <span data-ttu-id="df943-144">integer</span><span class="sxs-lookup"><span data-stu-id="df943-144">integer</span></span><br/> | <span data-ttu-id="df943-145">1</span><span class="sxs-lookup"><span data-stu-id="df943-145">1</span></span><br/>               |
| <span data-ttu-id="df943-146">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="df943-146">Mandatory</span></span><br/>    | <span data-ttu-id="df943-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df943-147">string</span></span><br/>  | <span data-ttu-id="df943-148">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="df943-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="df943-149">Unittype</span><span class="sxs-lookup"><span data-stu-id="df943-149">UnitType</span></span><br/>     | <span data-ttu-id="df943-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df943-150">string</span></span><br/>  | <span data-ttu-id="df943-151">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="df943-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="df943-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df943-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df943-153">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="df943-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




