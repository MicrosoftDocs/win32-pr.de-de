---
title: Erstellen eines renderingkontexts ist nicht aktuell
description: Um einen renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell. Dazu rufen Sie die wglmakecurrent-Funktion mit den Parametern auf, die auf NULL festgelegt sind. Im folgenden finden Sie ein Beispiel für diese einfache Aufgabe.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL unter Windows, renderingkontexte
- Rendern von Kontexten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309796"
---
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="2fa9f-107">Erstellen eines renderingkontexts ist nicht aktuell</span><span class="sxs-lookup"><span data-stu-id="2fa9f-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="2fa9f-108">Um einen renderingkontext von einem Thread zu trennen, machen Sie ihn nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2fa9f-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="2fa9f-109">Dazu rufen Sie die [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) -Funktion mit den Parametern auf, die auf **null** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="2fa9f-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="2fa9f-110">Im folgenden finden Sie ein Beispiel für diese einfache Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2fa9f-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




