---
title: Rechte Konstanten
description: Rechte Konstanten
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Media-Format-SDK, Konstanten
- Digital Rights Management (DRM), Konstanten
- DRM (Digital Rights Management), Konstanten
- Erweiterte APIs für den DRM-Client, Konstanten
- Erweiterte Client-APIs, Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100782"
---
# <a name="rights-constants"></a><span data-ttu-id="ac1e0-108">Rechte Konstanten</span><span class="sxs-lookup"><span data-stu-id="ac1e0-108">Rights Constants</span></span>

<span data-ttu-id="ac1e0-109">Die in der folgenden Tabelle aufgeführten Konstanten dienen zum Identifizieren von DRM-Aktionen und zum Erstellen von Listen mit Aktionen.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="ac1e0-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="ac1e0-110">Constant</span></span>                                        | <span data-ttu-id="ac1e0-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac1e0-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1e0-112">g \_ wszwmdrm- \_ Aktions Listen- \_ Tag</span><span class="sxs-lookup"><span data-stu-id="ac1e0-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="ac1e0-113">Definiert den XML-Elementnamen für eine Aktionsliste.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="ac1e0-114">g \_ wszwmdrm \_ Action- \_ Tag</span><span class="sxs-lookup"><span data-stu-id="ac1e0-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="ac1e0-115">Definiert den XML-Elementnamen für einen Eintrag in einer Aktionsliste.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="ac1e0-116">g \_ wszwmdrm \_ right- \_ Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="ac1e0-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="ac1e0-117">Definiert die Zeichenfolge, mit der Inhalt wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="ac1e0-118">g \_ wszwmdrm- \_ Rechte \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="ac1e0-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="ac1e0-119">Definiert die Zeichenfolge für das Recht, Inhalte zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="ac1e0-120">g \_ wszwmdrm \_ right \_ Playlist \_ Burn</span><span class="sxs-lookup"><span data-stu-id="ac1e0-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="ac1e0-121">Definiert die Zeichenfolge für das Recht, Inhalte als Teil einer Wiedergabeliste auf CD zu brennen.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ac1e0-122">g \_ wszwmdrm \_ right \_ Create \_ Miniatur \_ Bild</span><span class="sxs-lookup"><span data-stu-id="ac1e0-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="ac1e0-123">Definiert die Zeichenfolge für das Recht, ein Miniaturbild aus Videoinhalten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ac1e0-124">g \_ wszwmdrm \_ - \_ Rechte \_ auf \_ CD kopieren</span><span class="sxs-lookup"><span data-stu-id="ac1e0-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="ac1e0-125">Definiert die Zeichenfolge für das Recht, Inhalte auf eine CD zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="ac1e0-126">Neue Lizenzen sollten dieses Recht nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-126">New licenses should not use this right.</span></span> <span data-ttu-id="ac1e0-127">Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, von der Berechtigung "Kopieren" und der Wiedergabeliste "Burn" abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="ac1e0-128">g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="ac1e0-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="ac1e0-129">Definiert die Zeichenfolge für das Recht, Inhalte auf ein Gerät zu kopieren, das der Secure Digital Music Initiative (SDMI) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="ac1e0-130">Neue Lizenzen sollten dieses Recht nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-130">New licenses should not use this right.</span></span> <span data-ttu-id="ac1e0-131">Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, von der Berechtigung zum Kopieren abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="ac1e0-132">g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="ac1e0-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="ac1e0-133">Definiert die Zeichenfolge für das Recht, auf ein Gerät zu kopieren, das nicht der Secure Digital Music Initiative (SDMI) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="ac1e0-134">Neue Lizenzen sollten dieses Recht nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-134">New licenses should not use this right.</span></span> <span data-ttu-id="ac1e0-135">Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, von der Berechtigung zum Kopieren abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="ac1e0-136">g \_ wszwmdrm- \_ Rechte \_ Sicherung</span><span class="sxs-lookup"><span data-stu-id="ac1e0-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="ac1e0-137">Definiert die Zeichenfolge für das Recht zum Sichern der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="ac1e0-138">g \_ wszwmdrm \_ right \_ COLLABORATIVE \_ Play</span><span class="sxs-lookup"><span data-stu-id="ac1e0-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="ac1e0-139">Definiert die Zeichenfolge für das Recht, Inhalte über ein Netzwerk als Teil einer freigegebenen Wiedergabeliste wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac1e0-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="ac1e0-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac1e0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac1e0-141">**Konstanten**</span><span class="sxs-lookup"><span data-stu-id="ac1e0-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




