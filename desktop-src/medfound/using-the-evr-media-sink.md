---
description: Verwenden der EVR-Medien Senke
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Verwenden der EVR-Medien Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354280"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="8043f-103">Verwenden der EVR-Medien Senke</span><span class="sxs-lookup"><span data-stu-id="8043f-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="8043f-104">Die gesteigerte Medien Senke (Enhanced Video Renderer) kann als eigenständige Komponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8043f-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="8043f-105">Häufig wird jedoch eine Anwendung die EVR-Medien Senke in einer Topologie erstellen und dann die Wiedergabe mit der Medien Sitzung steuern.</span><span class="sxs-lookup"><span data-stu-id="8043f-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="8043f-106">Es gibt zwei Möglichkeiten, die EVR-Medien Senke zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="8043f-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="8043f-107">Die [**MF**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) -Funktion erstellt die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="8043f-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="8043f-108">Die [**MF**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion erstellt ein Aktivierungs Objekt für die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="8043f-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="8043f-109">Die EVR-Medien Senke verfügt anfänglich über eine streamsenke, die dem Verweis Datenstrom entspricht.</span><span class="sxs-lookup"><span data-stu-id="8043f-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="8043f-110">Um neue streamsenken hinzuzufügen, nennen Sie [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="8043f-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8043f-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8043f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8043f-112">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="8043f-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="8043f-113">Medien senken</span><span class="sxs-lookup"><span data-stu-id="8043f-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



