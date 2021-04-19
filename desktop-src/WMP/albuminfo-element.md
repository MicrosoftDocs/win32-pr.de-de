---
title: Albuminfo-Element
description: Das Element "Albuminfo" gibt die URL für die Webseite an, die von Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medien Element anzeigen möchte.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Fenster Media Player des Albuminfo-Elements
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361526"
---
# <a name="albuminfo-element"></a><span data-ttu-id="883c8-104">Albuminfo-Element</span><span class="sxs-lookup"><span data-stu-id="883c8-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="883c8-105">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="883c8-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="883c8-106">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="883c8-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="883c8-107">Das Element " **Albuminfo** " gibt die URL für die Webseite an, die von Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medien Element anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="883c8-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="883c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="883c8-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="883c8-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="883c8-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="883c8-110">Die URL für die Webseite, die von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="883c8-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="883c8-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="883c8-111">Parent/Child Elements</span></span>



| <span data-ttu-id="883c8-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="883c8-112">Hierarchy</span></span>       | <span data-ttu-id="883c8-113">Element</span><span class="sxs-lookup"><span data-stu-id="883c8-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="883c8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="883c8-114">Parent elements</span></span> | <span data-ttu-id="883c8-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="883c8-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="883c8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="883c8-116">Child elements</span></span>  | <span data-ttu-id="883c8-117">Keine</span><span class="sxs-lookup"><span data-stu-id="883c8-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="883c8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="883c8-118">Remarks</span></span>

<span data-ttu-id="883c8-119">Wenn der Benutzer auf eine Schaltfläche in Windows Media Player klickt, um zusätzliche Informationen zu einem bestimmten Medien Element anzuzeigen, sendet der Player die URL-Anforderung mit Parametern, die mithilfe eines Fragezeichens (?) Abfrage Zeichenfolgen-Trennzeichen angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="883c8-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="883c8-120">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="883c8-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="883c8-121">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="883c8-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="883c8-122">Name</span><span class="sxs-lookup"><span data-stu-id="883c8-122">Name</span></span>         | <span data-ttu-id="883c8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="883c8-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="883c8-124">*Aufzunehmen*</span><span class="sxs-lookup"><span data-stu-id="883c8-124">*Album*</span></span>      | <span data-ttu-id="883c8-125">Der Wert des **WM/albumtitle-** Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="883c8-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="883c8-126">*Interpret*</span><span class="sxs-lookup"><span data-stu-id="883c8-126">*Artist*</span></span>     | <span data-ttu-id="883c8-127">Der Wert des **WM/Album-** Attributs, sofern vorhanden, oder andernfalls der Wert des **Author** -Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="883c8-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="883c8-128">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="883c8-128">*geoid*</span></span>      | <span data-ttu-id="883c8-129">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="883c8-129">Windows geographical location ID.</span></span> <span data-ttu-id="883c8-130">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="883c8-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="883c8-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="883c8-131">*locale*</span></span>     | <span data-ttu-id="883c8-132">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="883c8-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="883c8-133">*Titel*</span><span class="sxs-lookup"><span data-stu-id="883c8-133">*Title*</span></span>      | <span data-ttu-id="883c8-134">Der Wert des **Title** -Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="883c8-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="883c8-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="883c8-135">*UFID*</span></span>       | <span data-ttu-id="883c8-136">Der Wert des **WM/UniqueFileIdentifier-** Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="883c8-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="883c8-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="883c8-137">*userlocale*</span></span> | <span data-ttu-id="883c8-138">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="883c8-138">Windows locale ID.</span></span> <span data-ttu-id="883c8-139">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="883c8-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="883c8-140">*version*</span><span class="sxs-lookup"><span data-stu-id="883c8-140">*version*</span></span>    | <span data-ttu-id="883c8-141">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="883c8-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="883c8-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="883c8-142">Requirements</span></span>



| <span data-ttu-id="883c8-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="883c8-143">Requirement</span></span> | <span data-ttu-id="883c8-144">Wert</span><span class="sxs-lookup"><span data-stu-id="883c8-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="883c8-145">Version</span><span class="sxs-lookup"><span data-stu-id="883c8-145">Version</span></span><br/> | <span data-ttu-id="883c8-146">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="883c8-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="883c8-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="883c8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883c8-148">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="883c8-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="883c8-149">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="883c8-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="883c8-150">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="883c8-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





