---
title: Schleifen Wiedergabe für mciwnd
description: Schleifen Wiedergabe (mciwnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106370977"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="c2a84-103">Schleifen Wiedergabe für mciwnd</span><span class="sxs-lookup"><span data-stu-id="c2a84-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="c2a84-104">Mciwnd unterstützt die Wiedergabe als fortlaufende Schleife.</span><span class="sxs-lookup"><span data-stu-id="c2a84-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="c2a84-105">Sie können den Inhalt einer Datei oder eines Geräts wiederholt als Schleife wiedergeben, indem Sie das Makro [**mciwndtartrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) in Kombination mit der **Wiedergabe** Schaltfläche auf der Symbolleiste verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2a84-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="c2a84-106">Das Videowiedergabe Gerät MCIAVI unterstützt Wiedergabe Schleifen.</span><span class="sxs-lookup"><span data-stu-id="c2a84-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="c2a84-107">Verwenden Sie das [**mciwndgetrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) -Makro, um zu bestimmen, ob die fortlaufende Wiedergabe aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c2a84-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




