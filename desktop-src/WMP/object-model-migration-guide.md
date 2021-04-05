---
title: Handbuch für die Migration des Objektmodells
description: Handbuch für die Migration des Objektmodells
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player, Migrations Handbuch
- Windows Media Player-Objektmodell, Migrations Handbuch
- Objektmodell, Migrations Handbuch
- Windows Media Player ActiveX-Steuerelement, Migrations Handbuch
- ActiveX-Steuerelement, Migrations Handbuch
- Windows Media Player Mobile ActiveX-Steuerelement, Migrations Handbuch
- Windows Media Player Mobile, Objektmodell
- Windows Media Player Mobile, Migrations Handbuch
- Migrations Handbuch, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037390"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="a389d-113">Handbuch für die Migration des Objektmodells</span><span class="sxs-lookup"><span data-stu-id="a389d-113">Object Model Migration Guide</span></span>

<span data-ttu-id="a389d-114">In Windows Media Player 7 wurde ein neues Objektmodell eingeführt, das einen umfangreichen neuen Funktions Satz bietet, mit dem Sie Ihre Webseiten erweitern können.</span><span class="sxs-lookup"><span data-stu-id="a389d-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="a389d-115">Nachfolgende Versionen haben das Objektmodell der Version 7 mit zusätzlichen Eigenschaften, Methoden und Ereignissen erweitert.</span><span class="sxs-lookup"><span data-stu-id="a389d-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="a389d-116">Das neue-Objektmodell unterscheidet sich jedoch erheblich vom Windows Media Player 6,4-Objektmodell. Sie müssen also wissen, wie Sie Ihren vorhandenen Code aktualisieren können, wenn Sie Windows Media Player 7 und höher in Ihren Projekten unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="a389d-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="a389d-117">Ein Beispiel, das veranschaulicht, wie Sie die Windows Media Player-Version und den aktuellen Browser des Benutzers erkennen, finden Sie im Beispiel mit dem Namen "Detection", das mit diesem SDK installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a389d-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="a389d-118">Weitere Informationen zu Beispielen finden Sie unter [Beispiele](samples.md).</span><span class="sxs-lookup"><span data-stu-id="a389d-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="a389d-119">Dieses Handbuch bezieht sich auf das neue Objektmodell als das Objektmodell Windows Media Player 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a389d-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="a389d-120">Ausführliche Informationen zu den Funktionen, die in den einzelnen Versionen von Windows Media Player verfügbar sind, finden Sie unter [Objektmodell Referenz für die Skript](object-model-reference-for-scripting.md)Erstellung.</span><span class="sxs-lookup"><span data-stu-id="a389d-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="a389d-121">Diese Probleme mit dem Objektmodell werden in den folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="a389d-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="a389d-122">Unterschiede zwischen den Objekt Modellen</span><span class="sxs-lookup"><span data-stu-id="a389d-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="a389d-123">Verwenden des Objektmodells Windows Media Player 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="a389d-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="a389d-124">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="a389d-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="a389d-125">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="a389d-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="a389d-126">Untertitel</span><span class="sxs-lookup"><span data-stu-id="a389d-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="a389d-127">DVD</span><span class="sxs-lookup"><span data-stu-id="a389d-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="a389d-128">Vergleich von detaillierten Objekt Modellen</span><span class="sxs-lookup"><span data-stu-id="a389d-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="a389d-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a389d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a389d-130">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="a389d-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




