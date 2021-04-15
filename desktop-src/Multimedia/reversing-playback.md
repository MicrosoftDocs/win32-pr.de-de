---
title: Umkehren der Wiedergabe
description: Umkehren der Wiedergabe
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Mciwndplayreverse-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388274"
---
# <a name="reversing-playback"></a><span data-ttu-id="b3f70-104">Umkehren der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="b3f70-104">Reversing Playback</span></span>

<span data-ttu-id="b3f70-105">Einige Geräte unterstützen die Wiedergabe in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="b3f70-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="b3f70-106">Sie können den Inhalt eines solchen Geräts in umgekehrter Richtung wiedergeben, indem Sie das [**mciwndplayreverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3f70-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="b3f70-107">Dieses Makro definiert den Wiedergabe Bereich von der aktuellen Wiedergabe Position bis zum Anfang des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="b3f70-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="b3f70-108">Das Digital-Video-Gerät, mciavi. DRV kann rückwärts abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="b3f70-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="b3f70-109">Geräte, die nicht rückwärts wiedergegeben werden können, z. b. CD-Audiodaten, können eine Fehlermeldung ausgeben, wenn **mciwndplayreverse** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b3f70-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




