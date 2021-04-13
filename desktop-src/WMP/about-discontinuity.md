---
title: Informationen über Diskontinuität
description: Informationen über Diskontinuität
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audiodiskontinuität
- DSP-Plug-ins, Audiodiskontinuität
- audiodsp-Plug-ins, Diskontinuität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388025"
---
# <a name="about-discontinuity"></a><span data-ttu-id="d0f96-108">Informationen über Diskontinuität</span><span class="sxs-lookup"><span data-stu-id="d0f96-108">About Discontinuity</span></span>

<span data-ttu-id="d0f96-109">Zu jedem Zeitpunkt kann Windows Media Player eine Unterbrechung im Eingabestream durch Aufrufen der **imediaobject::D iscontinuity** -Methode signalisieren.</span><span class="sxs-lookup"><span data-stu-id="d0f96-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="d0f96-110">Dies tritt regelmäßig am Anfang und am Ende eines Streams und vor jedem Suchvorgang auf, oder wenn Streaming-Inhalte aus irgendeinem Grund unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="d0f96-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="d0f96-111">Das Beispiel-DSP-Plug-in, das vom Assistenten für Windows-Media Player-Plug-ins generiert wird, muss aus folgenden Gründen nicht mit Diskontinuitäten behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="d0f96-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="d0f96-112">PCM-Beispiele sind atomarisch, d. h., Sie können ohne Rücksicht auf die anderen Beispiele im Stream verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d0f96-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="d0f96-113">Einige Videoformate enthalten Daten, die von Keyframes und komprimierten Beispielen abhängen.</span><span class="sxs-lookup"><span data-stu-id="d0f96-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="d0f96-114">Der Beispielcode wird so geschrieben, dass der Client immer gezwungen wird, die gesamte Ausgabe zu verarbeiten, bevor das Plug-in mehr Eingaben akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d0f96-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="d0f96-115">Die Standard Implementierung von **imediaobject::D iscontinuity** gibt einfach S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d0f96-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0f96-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0f96-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f96-117">**Implementieren eines audiodsp-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="d0f96-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




