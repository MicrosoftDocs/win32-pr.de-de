---
title: Servicinput info-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das servicinput info-Element ist das Hauptelement für das ServiceInfo.xml Dokument.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Servicinput info-Element, Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361917"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="ca726-106">Servicinput info-Element</span><span class="sxs-lookup"><span data-stu-id="ca726-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="ca726-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="ca726-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ca726-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca726-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ca726-109">Das **servicinput Info** -Element ist das Hauptelement für das ServiceInfo.xml Dokument.</span><span class="sxs-lookup"><span data-stu-id="ca726-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="ca726-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca726-110">Attributes</span></span>



| <span data-ttu-id="ca726-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="ca726-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="ca726-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca726-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca726-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span><span class="sxs-lookup"><span data-stu-id="ca726-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="ca726-114">Die Version der ServiceInfo.xml Datei.</span><span class="sxs-lookup"><span data-stu-id="ca726-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="ca726-115">Version 1,00 wird für Windows Media Player unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca726-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="ca726-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Schlüssel** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="ca726-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="ca726-117">Die Dienst Schlüssel Zeichenfolge, die den Online Store eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ca726-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="ca726-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**Contentpartner**</span><span class="sxs-lookup"><span data-stu-id="ca726-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="ca726-119">Gibt an, ob der Online Shop ein Typ-1-Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="ca726-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="ca726-120">Der Wert "true" gibt an, dass der Speicher ein Typ-1-Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="ca726-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="ca726-121">Der Wert "false" gibt an, dass es sich bei dem Speicher nicht um einen Speicher vom Typ 1 handelt. Das heißt, es handelt sich um einen Speicher vom Typ 2.</span><span class="sxs-lookup"><span data-stu-id="ca726-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="ca726-122">Der Standardwert ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="ca726-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="ca726-123">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="ca726-123">Parent/Child Elements</span></span>



| <span data-ttu-id="ca726-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ca726-124">Hierarchy</span></span>       | <span data-ttu-id="ca726-125">Element</span><span class="sxs-lookup"><span data-stu-id="ca726-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca726-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca726-126">Parent elements</span></span> | <span data-ttu-id="ca726-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ca726-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ca726-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca726-128">Child elements</span></span>  | <span data-ttu-id="ca726-129">**Albuminfo**, **buycd**, **Color**, **Description**, **FriendlyName**, **HtmlView**, **Image**, **Infocenter**, **install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="ca726-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ca726-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca726-130">Remarks</span></span>

<span data-ttu-id="ca726-131">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca726-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="ca726-132">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ca726-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="ca726-133">Die Anforderung enthält auch alle Parameter, die Sie mithilfe des Befehlszeilen Parameters "serviceextra" von Windows Media Player Setup angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ca726-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="ca726-134">Name</span><span class="sxs-lookup"><span data-stu-id="ca726-134">Name</span></span>         | <span data-ttu-id="ca726-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ca726-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca726-136">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="ca726-136">*geoid*</span></span>      | <span data-ttu-id="ca726-137">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="ca726-137">Windows geographical location ID.</span></span> <span data-ttu-id="ca726-138">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca726-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="ca726-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="ca726-139">*locale*</span></span>     | <span data-ttu-id="ca726-140">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="ca726-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="ca726-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="ca726-141">*userlocale*</span></span> | <span data-ttu-id="ca726-142">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="ca726-142">Windows locale ID.</span></span> <span data-ttu-id="ca726-143">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca726-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="ca726-144">*version*</span><span class="sxs-lookup"><span data-stu-id="ca726-144">*version*</span></span>    | <span data-ttu-id="ca726-145">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="ca726-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="ca726-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca726-146">Requirements</span></span>



| <span data-ttu-id="ca726-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca726-147">Requirement</span></span> | <span data-ttu-id="ca726-148">Wert</span><span class="sxs-lookup"><span data-stu-id="ca726-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="ca726-149">Version</span><span class="sxs-lookup"><span data-stu-id="ca726-149">Version</span></span><br/> | <span data-ttu-id="ca726-150">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ca726-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca726-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca726-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca726-152">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="ca726-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="ca726-153">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="ca726-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="ca726-154">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="ca726-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





