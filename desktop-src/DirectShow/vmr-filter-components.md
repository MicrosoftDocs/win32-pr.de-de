---
description: VMR-Filter Komponenten
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: VMR-Filter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529510"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="22b97-103">VMR-Filter Komponenten</span><span class="sxs-lookup"><span data-stu-id="22b97-103">VMR Filter Components</span></span>

<span data-ttu-id="22b97-104">Die VMR verwendet einen modularen Entwurf, der es Anwendungen ermöglicht, Sie für viele verschiedene renderingszenarios zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="22b97-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="22b97-105">Abhängig von der Konfiguration enthält VMR zwischen zwei und fünf unter Komponenten (zusätzlich zu den zugehörigen Eingabe Pins).</span><span class="sxs-lookup"><span data-stu-id="22b97-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR im Fenstermodus mit mehreren Streams](images/vmr-multiple-streams.png)

<span data-ttu-id="22b97-107">**Mixer:** Der Mixer ist ein COM-Objekt, das für das Mischen mehrerer Streams zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="22b97-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="22b97-108">Deinterlacing tritt auch innerhalb des Mischers auf.</span><span class="sxs-lookup"><span data-stu-id="22b97-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="22b97-109">Der Mixer wird von VMR geladen, wenn mehrere Eingabestreams erkannt werden oder wenn das Eingabe Video mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="22b97-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="22b97-110">Der Mixer sammelt Informationen zu jedem Eingabedaten Strom und sortiert die Streams in der richtigen Z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="22b97-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="22b97-111">Er ist dafür verantwortlich, zu bestimmen, wann jede Eingabe-PIN eine Stichprobe empfängt, und die Bildkomposition zum richtigen Zeitpunkt anzuweisen, die eigentliche Mischung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22b97-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="22b97-112">Der Mixer berechnet auch den Zeitstempel, der auf jedes Ausgabe Bild angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22b97-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="22b97-113">Wenn die Anwendung eine Bitmap bereitstellt, die oberhalb des zusammengesetzten Bilds angezeigt werden soll, ist der Mixer dafür verantwortlich, sicherzustellen, dass die Bitmap auch dann im oberen Bereich angezeigt wird, wenn die Z-Reihenfolge der Eingabedaten Ströme geändert wird.</span><span class="sxs-lookup"><span data-stu-id="22b97-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="22b97-114">**Bild Compositor:** Der Bild Compositor ist ein COM-Objekt, das die tatsächliche Mischung der Eingabedaten Ströme auf eine einzelne DirectDraw-oder Direct3D-Oberfläche durchführt, die von der Zuordnung-Presenter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="22b97-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="22b97-115">VMR bietet einen Standard-Bild Kompositions Tor, mit dem Anwendungen 2D-Alpha Mischungs Effekte durchführen können.</span><span class="sxs-lookup"><span data-stu-id="22b97-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="22b97-116">Anwendungen können einen benutzerdefinierten Bild Compositor bereitstellen, um andere 2D-und 3D-Effekte zu ermöglichen, z. b. das Anwenden von Texturen auf Teile des Bilds, die Pixel Mischung pro Pixel, die Zuordnung des Bilds zum stationären oder das Verschieben von 3D-Objekten usw.</span><span class="sxs-lookup"><span data-stu-id="22b97-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="22b97-117">**Zuordnung-Presenter:** Der zuordnerpräsentator ist ein COM-Objekt, das das DirectDraw-oder Direct3D-Objekt zuordnet und die Kommunikation mit der Grafikkarte behandelt.</span><span class="sxs-lookup"><span data-stu-id="22b97-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="22b97-118">Die Zeichnung kann entweder als kippen oder als Blit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="22b97-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="22b97-119">Sie können Ihren eigenen Zuordnungs-Presenter einbinden, um das DirectDraw-oder Direct3D-Objekt zu erstellen und zu steuern und/oder um zur Präsentationszeit Zugriff auf die Video Bits zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22b97-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="22b97-120">**Fenster-Manager:** Der Fenster-Manager wird nur im Fenstermodus verwendet.</span><span class="sxs-lookup"><span data-stu-id="22b97-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="22b97-121">Der Fenster-Manager unterstützt die Legacy-Schnittstellen [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) aus Gründen der Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="22b97-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22b97-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22b97-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22b97-123">Informationen zum Video Mischungs Rendering</span><span class="sxs-lookup"><span data-stu-id="22b97-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



