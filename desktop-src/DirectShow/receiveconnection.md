---
description: Receiveconnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: Receiveconnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124670"
---
# <a name="receiveconnection"></a><span data-ttu-id="33c50-103">Receiveconnection</span><span class="sxs-lookup"><span data-stu-id="33c50-103">ReceiveConnection</span></span>

<span data-ttu-id="33c50-104">Dieser Mechanismus ermöglicht es einer Ausgabepin, eine Formatänderung an den downstreampeer vorzuschlagen, wenn das neue Format einen größeren Puffer erfordert.</span><span class="sxs-lookup"><span data-stu-id="33c50-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="33c50-105">Die Ausgabe-PIN führt folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="33c50-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="33c50-106">Ruft [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) für die downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="33c50-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="33c50-107">Wenn `ReceiveConnection` erfolgreich ist, wird [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) für die Eingabe-PIN aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="33c50-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="33c50-108">Außerdem muss die Ausgabepin möglicherweise [**imemzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) aufrufen und dann die Zuweisung Decommit und erneut ausführen, um die Puffergrößen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="33c50-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="33c50-109">Stellen Sie sicher, dass Sie alle ausstehenden Beispiele im alten Format bereitstellen, bevor Sie die Puffergröße ändern.</span><span class="sxs-lookup"><span data-stu-id="33c50-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="33c50-110">Einige MPEG-2-Decoder verwenden diesen Mechanismus, um zwischen MPEG-1-und MPEG-2-Ausgabe zu wechseln oder die Videogröße zu ändern.</span><span class="sxs-lookup"><span data-stu-id="33c50-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



