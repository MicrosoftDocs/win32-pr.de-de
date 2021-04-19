---
description: Media Foundation wird initialisiert.
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Media Foundation wird initialisiert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363892"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="3cc39-103">Media Foundation wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="3cc39-103">Initializing Media Foundation</span></span>

<span data-ttu-id="3cc39-104">Vor der Verwendung von Microsoft Media Foundation-Objekten oder-Schnittstellen müssen Sie die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="3cc39-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="3cc39-105">Übergeben Sie die Konstante **MF- \_ Version**.</span><span class="sxs-lookup"><span data-stu-id="3cc39-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="3cc39-106">Die [**MF Startup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion initialisiert die Media Foundation Plattform.</span><span class="sxs-lookup"><span data-stu-id="3cc39-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="3cc39-107">Wenn **MF Startup** eine Fehler \_ hafte \_ Start Version von MF E zurückgibt \_ \_ , bedeutet dies, dass Ihre Anwendung mit einer Version der Media Foundation-Header kompiliert wurde, die nicht mit den Media Foundation DLLs auf dem System identisch ist.</span><span class="sxs-lookup"><span data-stu-id="3cc39-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="3cc39-108">Für jeden [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)-Rückruf muss Ihre Anwendung [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3cc39-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="3cc39-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cc39-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cc39-110">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="3cc39-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="3cc39-111">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="3cc39-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



