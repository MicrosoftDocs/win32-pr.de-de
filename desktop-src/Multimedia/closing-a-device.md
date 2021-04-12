---
title: Schließen eines Geräts
description: Schließen eines Geräts
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388009"
---
# <a name="closing-a-device"></a><span data-ttu-id="faf33-104">Schließen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="faf33-104">Closing a Device</span></span>

<span data-ttu-id="faf33-105">Der [**Close**](close.md) ([**MCI \_ Close**](mci-close.md))-Befehl gibt den Zugriff auf ein Gerät oder eine Datei frei.</span><span class="sxs-lookup"><span data-stu-id="faf33-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="faf33-106">MCI gibt ein Gerät frei, wenn es von allen Tasks, die ein Gerät verwenden, geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="faf33-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="faf33-107">Um MCI bei der Verwaltung der Geräte zu unterstützen, muss die Anwendung jedes Gerät oder jede Datei schließen, wenn Sie Sie nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="faf33-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="faf33-108">Wenn Sie ein externes MCI-Gerät schließen, das anstelle von Dateien (z. b. CD-Audiodatei) ein eigenes Medium verwendet, verlässt der Treiber das Gerät im aktuellen Betriebsmodus.</span><span class="sxs-lookup"><span data-stu-id="faf33-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="faf33-109">Wenn Sie also ein CD-Audiogerät schließen, das abgespielt wird, auch wenn der Gerätetreiber aus dem Arbeitsspeicher freigegeben wird, wird das CD-Audiogerät weiterhin abgespielt, bis das Ende seines Inhalts erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="faf33-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="faf33-110">Wenn Sie eine Anwendung mit geöffneten MCI-Geräten schließen, können Sie verhindern, dass andere Anwendungen diese Geräte verwenden, bis Windows neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="faf33-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




