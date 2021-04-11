---
description: Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218210"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="990fa-103">Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors</span><span class="sxs-lookup"><span data-stu-id="990fa-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="990fa-104">In seltenen Fällen möchten Sie möglicherweise das Video Rendering mit der Aktualisierungsrate des Monitors genau synchronisieren, damit jedes Mal, wenn der Monitor aktualisiert wird, genau ein neuer Frame angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="990fa-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="990fa-105">Die zuverlässigste Methode hierfür ist das Erstellen eines benutzerdefinierten zuordcators, der einen Flip-Vorgang anstelle eines Blit-Vorgangs verwendet, um die Video Bits in die primäre Oberfläche zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="990fa-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="990fa-106">"Kippen" wird bei jeder Aktualisierung des Monitors aufgerufen. wenn der Videostream also keine Zeitstempel enthält, wird der VMR so schnell wie möglich auf die primäre Oberfläche rendern, aber die Oberfläche blockiert den Stream, bis der Flip-Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="990fa-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="990fa-107">Dies bedeutet, dass der nächste Frame immer auf die primäre Oberfläche wartet, wenn der Monitor aktualisiert wird, solange die CPU nicht überlastet ist.</span><span class="sxs-lookup"><span data-stu-id="990fa-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="990fa-108">Wenn jedoch ein anderer CPU-intensiver Prozess ausgeführt wird, kann es passieren, dass der DirectShow-streamingingthread nicht schnell genug an die primäre Oberfläche geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="990fa-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="990fa-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="990fa-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="990fa-110">VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)</span><span class="sxs-lookup"><span data-stu-id="990fa-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



