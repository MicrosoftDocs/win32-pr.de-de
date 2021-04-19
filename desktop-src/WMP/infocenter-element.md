---
title: InfoCenter-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | InfoCenter-Element
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- InfoCenter-Element Fenster Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359257"
---
# <a name="infocenter-element"></a><span data-ttu-id="2f047-105">InfoCenter-Element</span><span class="sxs-lookup"><span data-stu-id="2f047-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="2f047-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="2f047-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2f047-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f047-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2f047-108">Das **Infocenter** -Element gibt die URL der **Webseite an, die von Windows** Media Player in der Info Center-Ansichts Funktion von angezeigt wird, wenn der Online Store aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2f047-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="2f047-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f047-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="2f047-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="2f047-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="2f047-111">Die URL für die Webseite, die von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2f047-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="2f047-112">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="2f047-112">Parent/Child Elements</span></span>



| <span data-ttu-id="2f047-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="2f047-113">Hierarchy</span></span>       | <span data-ttu-id="2f047-114">Element</span><span class="sxs-lookup"><span data-stu-id="2f047-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="2f047-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f047-115">Parent elements</span></span> | <span data-ttu-id="2f047-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="2f047-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="2f047-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f047-117">Child elements</span></span>  | <span data-ttu-id="2f047-118">Keine</span><span class="sxs-lookup"><span data-stu-id="2f047-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="2f047-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f047-119">Remarks</span></span>

<span data-ttu-id="2f047-120">Der Benutzer steuert, wann die Info Center Ansicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2f047-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="2f047-121">Zum Abrufen von Informationen über das aktuell wiedergegebene Medien Element müssen Sie eine Instanz von Windows Media Player-Steuerelement in Ihre Webseite einbetten und das Player-Objektmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f047-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="2f047-122">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f047-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="2f047-123">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2f047-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="2f047-124">Name</span><span class="sxs-lookup"><span data-stu-id="2f047-124">Name</span></span>         | <span data-ttu-id="2f047-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2f047-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f047-126">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="2f047-126">*geoid*</span></span>      | <span data-ttu-id="2f047-127">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="2f047-127">Windows geographical location ID.</span></span> <span data-ttu-id="2f047-128">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f047-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="2f047-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="2f047-129">*locale*</span></span>     | <span data-ttu-id="2f047-130">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="2f047-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="2f047-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="2f047-131">*userlocale*</span></span> | <span data-ttu-id="2f047-132">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="2f047-132">Windows locale ID.</span></span> <span data-ttu-id="2f047-133">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f047-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="2f047-134">*version*</span><span class="sxs-lookup"><span data-stu-id="2f047-134">*version*</span></span>    | <span data-ttu-id="2f047-135">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="2f047-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="2f047-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f047-136">Requirements</span></span>



| <span data-ttu-id="2f047-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f047-137">Requirement</span></span> | <span data-ttu-id="2f047-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2f047-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="2f047-139">Version</span><span class="sxs-lookup"><span data-stu-id="2f047-139">Version</span></span><br/> | <span data-ttu-id="2f047-140">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2f047-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f047-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f047-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f047-142">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="2f047-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="2f047-143">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="2f047-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="2f047-144">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="2f047-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





