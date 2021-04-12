---
title: Benutzerdefinierte Datei-und Datenstrom Handler
description: Benutzerdefinierte Datei-und Datenstrom Handler
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Video für Windows (Vfw), benutzerdefinierte Datei Handler
- Video für Windows (Vfw), benutzerdefinierte Datenstrom Handler
- Video für Windows (Vfw), Datei Handler
- Video für Windows (Vfw), Datenstrom Handler
- VFW (Video für Windows), benutzerdefinierte Datei Handler
- VFW (Video für Windows), benutzerdefinierte Datenstrom Handler
- VFW (Video für Windows), Datei Handler
- VFW (Video für Windows), Datenstrom Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471413"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="64f10-111">Benutzerdefinierte Datei-und Datenstrom Handler</span><span class="sxs-lookup"><span data-stu-id="64f10-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="64f10-112">Datei-und Datenstrom Handler sind Treiber, die konsistente Schnittstellen für eine Anwendung bereitstellen, die multimediarewendungen steuert.</span><span class="sxs-lookup"><span data-stu-id="64f10-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="64f10-113">In den Datei-und Datenstrom Handlern, die im Betriebssystem enthalten sind, werden Video-und Waveform-Audiodaten verwendet, die in Audiodateien mit überlappende (AVI) und Waveform-Audiodateien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="64f10-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="64f10-114">Sie können Handler schreiben, damit Ihre Anwendung multimediarewendungen aus einer anderen Quelle schreiben oder darauf zugreifen kann, z. b. eine Datei, die ein proprietäres Format aufweist, eine AVI-Datei, die erweitert wurde, um zusätzliche Datenströme zu enthalten, oder ein Handler, der seine eigenen Multimedia-Daten generiert.</span><span class="sxs-lookup"><span data-stu-id="64f10-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="64f10-115">Wenn Sie über ein benutzerdefiniertes Dateiformat für AVI-Daten verfügen, das Sie mit den [avifile-Funktionen und-Makros](avifile-functions-and-macros.md)verwenden möchten, müssen Sie einen benutzerdefinierten Handler schreiben.</span><span class="sxs-lookup"><span data-stu-id="64f10-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="64f10-116">Informationen zu benutzerdefinierten Datei-und streamhandlern</span><span class="sxs-lookup"><span data-stu-id="64f10-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="64f10-117">Verwenden von benutzerdefinierten Datei-und streamhandlern</span><span class="sxs-lookup"><span data-stu-id="64f10-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="64f10-118">Benutzerdefinierte Datei-und streamhandlerreferenz</span><span class="sxs-lookup"><span data-stu-id="64f10-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




