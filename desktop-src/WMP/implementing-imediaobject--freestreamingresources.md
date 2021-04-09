---
title: Implementieren von imediaobject-freestreamingresources
description: Implementieren von imediaobject-freestreamingresources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
- Echo DSP-Plug-in-Beispiel, Freigeben von Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855803"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="d0118-109">Implementieren von imediaobject:: freestreamingresources</span><span class="sxs-lookup"><span data-stu-id="d0118-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="d0118-110">Es ist wichtig, dass Ihr Code jeden zugeordneten Arbeitsspeicher freigibt, bevor das Plug-in-Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="d0118-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="d0118-111">Windows Media Player ruft **freestreamingresources** auf, um dies zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d0118-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="d0118-112">Aus Sicherheitsgründen enthält das Beispiel **, das vom** Plug-in-Assistenten erstellt wurde, einen aufzurufenden **freestreamingresources** -Befehl, um sicherzustellen, dass der Arbeitsspeicher freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0118-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="d0118-113">Sie müssen den folgenden Code für das Echo-Beispiel zu " **freestreamingresources** " hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="d0118-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d0118-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0118-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0118-115">**Arbeiten mit Streamingressourcen**</span><span class="sxs-lookup"><span data-stu-id="d0118-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




