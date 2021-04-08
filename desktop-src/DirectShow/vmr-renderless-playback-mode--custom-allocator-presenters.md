---
description: VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757668"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="67eb0-103">VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)</span><span class="sxs-lookup"><span data-stu-id="67eb0-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="67eb0-104">Im renderlosen Wiedergabemodus führt VMR das Rendering nicht aus.</span><span class="sxs-lookup"><span data-stu-id="67eb0-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="67eb0-105">Stattdessen wird eine von der Anwendung bereitgestellte benutzerdefinierte Zuordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="67eb0-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="67eb0-106">Dieser Modus ist nützlich für Spiele und andere Arten von Anwendungen, die über anspruchsvolle Video Effekte verfügen.</span><span class="sxs-lookup"><span data-stu-id="67eb0-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="67eb0-107">Der renderlose Wiedergabemodus ermöglicht es den Anwendungen, ihre eigene DirectDraw-Oberfläche (VMR-7) oder Direct3D Surface (VMR-9) zu erstellen und zu steuern und zum Zeitpunkt der Präsentation auf die Video Bits zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="67eb0-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="67eb0-108">Im renderlosen Modus lädt VMR-9 seine Mischungs Komponente nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="67eb0-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="67eb0-109">Im renderlosen Wiedergabemodus führt die Anwendung die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="67eb0-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="67eb0-110">Verwaltet das Wiedergabe Fenster.</span><span class="sxs-lookup"><span data-stu-id="67eb0-110">Manages the playback window.</span></span>
-   <span data-ttu-id="67eb0-111">Ordnet das DirectDraw-oder Direct3D-Objekt und den abschließenden Frame Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="67eb0-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="67eb0-112">Benachrichtigt den Rest des Wiedergabe Systems des verwendeten Objekts.</span><span class="sxs-lookup"><span data-stu-id="67eb0-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="67eb0-113">Stellt den Frame Puffer zur richtigen Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="67eb0-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="67eb0-114">Behandelt alle Änderungen im Auflösungsmodus, überwachen Änderungen und Oberflächen Verluste.</span><span class="sxs-lookup"><span data-stu-id="67eb0-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="67eb0-115">Er muss das restliche Wiedergabe System dieser Ereignisse informieren.</span><span class="sxs-lookup"><span data-stu-id="67eb0-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="67eb0-116">Die VMR führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="67eb0-116">The VMR does the following:</span></span>

-   <span data-ttu-id="67eb0-117">Behandelt alle Zeitüberschreitungen im Zusammenhang mit der Darstellung des Video Frames.</span><span class="sxs-lookup"><span data-stu-id="67eb0-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="67eb0-118">Stellt Qualitäts Steuerungsinformationen für die Anwendung und den Rest des Wiedergabe Systems bereit.</span><span class="sxs-lookup"><span data-stu-id="67eb0-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="67eb0-119">Stellt eine konsistente Schnittstelle zu den Upstreamkomponenten des Wiedergabe Systems dar, die nicht wissen, dass die Anwendung die Frame Puffer Zuordnung bereitstellt und das Rendering ausführt.</span><span class="sxs-lookup"><span data-stu-id="67eb0-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="67eb0-120">Bietet eine beliebige Mischung aus Videostreams, die vor dem Rendering erforderlich sein können.</span><span class="sxs-lookup"><span data-stu-id="67eb0-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="67eb0-121">Da Deinterlacing durch den Mixer ausgeführt wird, hat der zuordnerpräsentator immer Deinterlacing-Frames empfangen.</span><span class="sxs-lookup"><span data-stu-id="67eb0-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="67eb0-122">Weitere Informationen finden Sie unter [Festlegen von deinterlace-Einstellungen](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="67eb0-123">Weitere Informationen zum Bereitstellen einer benutzerdefinierten Zuweisung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="67eb0-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="67eb0-124">Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7</span><span class="sxs-lookup"><span data-stu-id="67eb0-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="67eb0-125">Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9</span><span class="sxs-lookup"><span data-stu-id="67eb0-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="67eb0-126">Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors</span><span class="sxs-lookup"><span data-stu-id="67eb0-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



