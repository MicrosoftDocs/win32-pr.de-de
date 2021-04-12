---
title: Starten, anhalten und Fortsetzen der Wiedergabe
description: Starten, anhalten und Fortsetzen der Wiedergabe
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Mciwndplay-Makro
- Mciwndpause-Makro
- Mciwndresume-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207387"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="f6c1b-106">Starten, anhalten und Fortsetzen der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="f6c1b-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="f6c1b-107">[**Mciwndplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) ist das allgemeinste Wiedergabe Makro.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="f6c1b-108">Mit diesem Makro können Sie eine Datei oder ein Gerät von der aktuellen Wiedergabe Position wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="f6c1b-109">Die Wiedergabe wird über das Ende des Inhalts ausgeführt, es sei denn, Sie wird unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="f6c1b-110">Sie können ein Gerät, das mit dem [**mciwndpause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) -Makro abgespielt wird, vorübergehend unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="f6c1b-111">Um die Wiedergabe an der angehaltenen Position fortzusetzen, verwenden Sie das [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) -Makro.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="f6c1b-112">Einige Geräte unterstützen nicht die Befehle zum Anhalten und fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="f6c1b-113">Diese Geräte ordnen **mciwndpause** normalerweise dem [**mciwndstopp**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) -Makro zu, das die Wiedergabe oder Aufzeichnung beendet.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="f6c1b-114">Sie können ein Gerät, das Anhalten oder fortsetzen nicht unterstützt, mithilfe von **mciwndplay** neu starten, wodurch die Wiedergabe von der aktuellen Wiedergabe Position aus gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f6c1b-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




