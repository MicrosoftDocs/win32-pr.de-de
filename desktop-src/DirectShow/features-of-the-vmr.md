---
description: Features von VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Features von VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339674"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="40b93-103">Features von VMR</span><span class="sxs-lookup"><span data-stu-id="40b93-103">Features of the VMR</span></span>

<span data-ttu-id="40b93-104">Der Video Mischungs-Renderer 7 (VMR-7) unterstützt die folgenden neuen Features:</span><span class="sxs-lookup"><span data-stu-id="40b93-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="40b93-105">Echte Mischung mehrerer Videostreams mithilfe der Alpha Mischungs Funktionen von Direct3D-Hardware Geräten.</span><span class="sxs-lookup"><span data-stu-id="40b93-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="40b93-106">Die Möglichkeit zum Einbinden Ihrer eigenen Zusammensetzung-Komponente, um Effekte und Übergänge zwischen mehreren Videostreams zu implementieren, die in die VMR eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40b93-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="40b93-107">Echtes fensterloses Rendering.</span><span class="sxs-lookup"><span data-stu-id="40b93-107">True windowless rendering.</span></span> <span data-ttu-id="40b93-108">Es ist nicht mehr erforderlich, das Videowiedergabe Fenster zu einem untergeordneten Element des Anwendungsfensters zu machen, um die Videowiedergabe zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="40b93-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="40b93-109">Der neue fensterlose Renderingmodus von VMR ermöglicht Anwendungen das einfache Hosten der Videowiedergabe innerhalb eines beliebigen Fensters, ohne Fenster Meldungen an den Renderer für die Rendererspezifische Verarbeitung weiterleiten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="40b93-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="40b93-110">Ein neuer renderloser Wiedergabemodus, in dem Anwendungen eine eigene zuordnerkomponente bereitstellen können, um Zugriff auf das decodierte Video Bild zu erhalten, bevor es auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="40b93-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="40b93-111">Verbesserte Unterstützung für PCs, die mit mehreren Monitoren ausgestattet sind.</span><span class="sxs-lookup"><span data-stu-id="40b93-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="40b93-112">Unterstützung für die neue DirectX-Video Beschleunigung-Architektur von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40b93-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="40b93-113">Unterstützung für hochwertige Videowiedergabe gleichzeitig auf mehreren Fenstern.</span><span class="sxs-lookup"><span data-stu-id="40b93-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="40b93-114">Unterstützung für den exklusiven DirectDraw-Modus</span><span class="sxs-lookup"><span data-stu-id="40b93-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="40b93-115">100% Abwärtskompatibilität mit vorhandenen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="40b93-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="40b93-116">Unterstützung für Frame Step und eine zuverlässige Möglichkeit, das aktuelle Bild zu erfassen, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="40b93-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="40b93-117">Die Möglichkeit für Anwendungen, ihre eigenen statischen Bilddaten (z. b. Kanal Logos oder UI-Komponenten) problemlos mit dem Video in eine reibungslose flimmerfreie Weise zu mischen.</span><span class="sxs-lookup"><span data-stu-id="40b93-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="40b93-118">VMR-9 unterstützt alle oben aufgeführten Features sowie die folgenden:</span><span class="sxs-lookup"><span data-stu-id="40b93-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="40b93-119">Die Möglichkeit zum Verarbeiten von Videodaten direkt mit Direct3D-APIs wie z. b. Pixel-Shadern.</span><span class="sxs-lookup"><span data-stu-id="40b93-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="40b93-120">Verbesserte Unterstützung für Zeilen Sprung Videoinhalte.</span><span class="sxs-lookup"><span data-stu-id="40b93-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="40b93-121">Unterstützung für alle von DirectX unterstützten Plattformen.</span><span class="sxs-lookup"><span data-stu-id="40b93-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b93-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40b93-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b93-123">Informationen zum Video Mischungs Rendering</span><span class="sxs-lookup"><span data-stu-id="40b93-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



