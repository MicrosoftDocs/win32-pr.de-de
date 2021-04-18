---
description: In diesem Abschnitt wird beschrieben, wie Sie die Audiowiedergabe und Videowiedergabe in der Anwendung mithilfe von Microsoft Media Foundation implementieren.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Audio-/Videowiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344984"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="59772-103">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="59772-103">Audio/Video Playback</span></span>

<span data-ttu-id="59772-104">In diesem Abschnitt wird beschrieben, wie Sie die Audiowiedergabe und Videowiedergabe in der Anwendung mithilfe von Microsoft Media Foundation implementieren.</span><span class="sxs-lookup"><span data-stu-id="59772-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="59772-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="59772-105">In this section</span></span>



| <span data-ttu-id="59772-106">Thema</span><span class="sxs-lookup"><span data-stu-id="59772-106">Topic</span></span>                                                                                               | <span data-ttu-id="59772-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59772-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59772-108">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59772-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="59772-109">In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des [Medien Sitzungs](media-session.md) Objekts wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59772-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="59772-110">Wiedergeben geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="59772-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="59772-111">Abspielen von Dateien, die von DRM geschützte Medien enthalten.</span><span class="sxs-lookup"><span data-stu-id="59772-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="59772-112">So finden Sie die Dauer einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="59772-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="59772-113">So ermitteln Sie die Dauer einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="59772-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="59772-114">Suchen, schnelles vorwärts und umgekehrtes spielen</span><span class="sxs-lookup"><span data-stu-id="59772-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="59772-115">Dieses Thema enthält Beispielcode zum Verwalten von Such-und Raten Änderungen, wenn die [Medien Sitzung](media-session.md) für die Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59772-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="59772-116">Festlegen der Endzeit für die Wiedergabe Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="59772-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="59772-117">In diesem Thema wird beschrieben, wie eine Endzeit für die Wiedergabe bei Verwendung der [Medien Sitzung](media-session.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="59772-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="59772-118">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="59772-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="59772-119">Der Enhanced Video Renderer (EVR) ist eine Komponente, die ein Video zum Benutzer Monitor anzeigt.</span><span class="sxs-lookup"><span data-stu-id="59772-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="59772-120">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="59772-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="59772-121">Der streamingaudiorenderer (SAR) ist eine Medien Senke, die Audiodaten rendert.</span><span class="sxs-lookup"><span data-stu-id="59772-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="59772-122">MF Play</span><span class="sxs-lookup"><span data-stu-id="59772-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="59772-123">Die mfplay-API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="59772-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="59772-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59772-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59772-125">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="59772-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="59772-126">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="59772-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="59772-127">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59772-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




