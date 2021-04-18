---
title: Aktivieren der Synchronisierung mit Windows Media Player
description: Aktivieren der Synchronisierung mit Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Device Manager, Synchronisierung mit Windows Media Player
- Device Manager, Synchronisierung mit Windows Media Player
- Programmier Handbuch, Synchronisierung mit Windows Media Player
- Dienstanbieter, Synchronisierung mit Windows-Media Player
- Erstellen von Dienstanbietern, Synchronisierung mit Windows Media Player
- Synchronisierung mit Windows-Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340658"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="4c6f8-109">Aktivieren der Synchronisierung mit Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="4c6f8-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="4c6f8-110">Sie können ein Gerät für die Teilnahme an der automatischen Synchronisierung mit Windows Media Player aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4c6f8-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="4c6f8-111">Automatische Synchronisierung bedeutet Folgendes: Wenn ein Benutzer bestimmtes synchronisiertes Gerät eine Verbindung mit dem Computer herstellt, werden von Windows Media Player automatisch Dateien vom Gerät heruntergeladen, aktualisiert oder gelöscht, ohne dass zusätzliche Benutzereingaben erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4c6f8-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="4c6f8-112">Standardmäßig werden die folgenden Geräte mit Windows Media Player synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="4c6f8-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="4c6f8-113">MTP-Geräte</span><span class="sxs-lookup"><span data-stu-id="4c6f8-113">MTP devices</span></span>
-   <span data-ttu-id="4c6f8-114">Massenspeichergeräte</span><span class="sxs-lookup"><span data-stu-id="4c6f8-114">Mass-storage devices</span></span>
-   <span data-ttu-id="4c6f8-115">Windows CE Geräte (Windows Media Player 10 Mobile und höher)</span><span class="sxs-lookup"><span data-stu-id="4c6f8-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="4c6f8-116">Damit alle anderen Geräte mit Windows Media Player synchronisiert werden können, müssen die folgenden Anforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="4c6f8-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="4c6f8-117">Vom Gerät muss eine PAP-Geräteschnittstelle mit {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE} angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c6f8-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="4c6f8-118">Die vom Dienstanbieter zurückgegebenen Geräte Objekte müssen die **IMDSPDevice3** -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4c6f8-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="4c6f8-119">Der Geräteparameter useextendedwmdm muss auf den **DWORD** -Wert 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4c6f8-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="4c6f8-120">Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="4c6f8-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="4c6f8-121">Der Dienstanbieter sollte die folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="4c6f8-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="4c6f8-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="4c6f8-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="4c6f8-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="4c6f8-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="4c6f8-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="4c6f8-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="4c6f8-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c6f8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6f8-126">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="4c6f8-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="4c6f8-127">**Geräteparameter**</span><span class="sxs-lookup"><span data-stu-id="4c6f8-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




