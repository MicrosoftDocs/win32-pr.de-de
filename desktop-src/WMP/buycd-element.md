---
title: Buycd-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Buycd-Element
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Fenster "buycd-Element" Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368511"
---
# <a name="buycd-element"></a><span data-ttu-id="93304-105">Buycd-Element</span><span class="sxs-lookup"><span data-stu-id="93304-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="93304-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="93304-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="93304-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93304-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="93304-108">Das Element " **buycd** " gibt die URLs für Webseiten an, die von Windows Media Player angezeigt werden, wenn der Benutzer sich für einen Kauf entscheidet.</span><span class="sxs-lookup"><span data-stu-id="93304-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="93304-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="93304-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="93304-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**Mediaplayerurl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="93304-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="93304-111">Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Kauf in Windows Media Player bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93304-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="93304-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**Mediacenterurl**</span><span class="sxs-lookup"><span data-stu-id="93304-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="93304-113">Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Kauf in Windows XP Media Center Edition 2004 Update anzubieten.</span><span class="sxs-lookup"><span data-stu-id="93304-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="93304-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**Browserurl**</span><span class="sxs-lookup"><span data-stu-id="93304-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="93304-115">Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Einkauf in einem separaten Browserfenster anzubieten.</span><span class="sxs-lookup"><span data-stu-id="93304-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="93304-116">Diese URL wird auch von Windows XP Service Pack 2 oder höher für das Feature **für Musik Online** verwendet.</span><span class="sxs-lookup"><span data-stu-id="93304-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="93304-117">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="93304-117">Parent/Child Elements</span></span>



| <span data-ttu-id="93304-118">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="93304-118">Hierarchy</span></span>       | <span data-ttu-id="93304-119">Element</span><span class="sxs-lookup"><span data-stu-id="93304-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="93304-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93304-120">Parent elements</span></span> | <span data-ttu-id="93304-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="93304-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="93304-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93304-122">Child elements</span></span>  | <span data-ttu-id="93304-123">Keine</span><span class="sxs-lookup"><span data-stu-id="93304-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="93304-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93304-124">Remarks</span></span>

<span data-ttu-id="93304-125">Wenn der Benutzer auf eine Schaltfläche oder einen Link in Windows Media Player klickt, um eine CD oder DVD zu erwerben, sendet der Player die URL-Anforderung an ServiceTask1 mit Parametern, die mithilfe eines Fragezeichens (?) Abfrage Zeichenfolgen-Trennzeichen angehängt</span><span class="sxs-lookup"><span data-stu-id="93304-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="93304-126">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="93304-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="93304-127">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="93304-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="93304-128">Name</span><span class="sxs-lookup"><span data-stu-id="93304-128">Name</span></span>         | <span data-ttu-id="93304-129">Wert</span><span class="sxs-lookup"><span data-stu-id="93304-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93304-130">*Aufzunehmen*</span><span class="sxs-lookup"><span data-stu-id="93304-130">*Album*</span></span>      | <span data-ttu-id="93304-131">Der Wert des **WM/albumtitle-** Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="93304-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="93304-132">*Interpret*</span><span class="sxs-lookup"><span data-stu-id="93304-132">*Artist*</span></span>     | <span data-ttu-id="93304-133">Der Wert des **WM/Album-** Attributs, sofern vorhanden, oder andernfalls der Wert des **Author** -Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="93304-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="93304-134">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="93304-134">*geoid*</span></span>      | <span data-ttu-id="93304-135">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="93304-135">Windows geographical location ID.</span></span> <span data-ttu-id="93304-136">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="93304-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="93304-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="93304-137">*locale*</span></span>     | <span data-ttu-id="93304-138">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="93304-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="93304-139">*Titel*</span><span class="sxs-lookup"><span data-stu-id="93304-139">*Title*</span></span>      | <span data-ttu-id="93304-140">Der Wert des **Title** -Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="93304-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="93304-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="93304-141">*UFID*</span></span>       | <span data-ttu-id="93304-142">Der Wert des **WM/UniqueFileIdentifier-** Attributs für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="93304-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="93304-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="93304-143">*userlocale*</span></span> | <span data-ttu-id="93304-144">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="93304-144">Windows locale ID.</span></span> <span data-ttu-id="93304-145">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="93304-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="93304-146">*version*</span><span class="sxs-lookup"><span data-stu-id="93304-146">*version*</span></span>    | <span data-ttu-id="93304-147">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="93304-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="93304-148">Windows XP Media Center Edition 2004 stellt Benutzern eine Benutzeroberfläche zur Verfügung, die in einer Entfernung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93304-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="93304-149">Sie sollten Webseiten erstellen, damit der *mediacenterurl* -Parameter auf großen anzeigen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="93304-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="93304-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93304-150">Requirements</span></span>



| <span data-ttu-id="93304-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93304-151">Requirement</span></span> | <span data-ttu-id="93304-152">Wert</span><span class="sxs-lookup"><span data-stu-id="93304-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="93304-153">Version</span><span class="sxs-lookup"><span data-stu-id="93304-153">Version</span></span><br/> | <span data-ttu-id="93304-154">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="93304-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93304-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93304-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93304-156">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="93304-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="93304-157">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="93304-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="93304-158">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="93304-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





