---
title: Installieren von Kompressoren und Debug
description: Installieren von Kompressoren und Debug
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Videokomprimierungs-Manager (VCM), Installieren von Kompressoren
- VCM (Videokomprimierungs-Manager), Installieren von Kompressoren
- Icinstall-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309679"
---
# <a name="installing-compressors-and-decompressors"></a><span data-ttu-id="f907e-106">Installieren von Kompressoren und Debug</span><span class="sxs-lookup"><span data-stu-id="f907e-106">Installing Compressors and Decompressors</span></span>

<span data-ttu-id="f907e-107">Das folgende Beispiel zeigt, wie eine Anwendung eine Funktion mit der Funktion [**icinstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) als Kompressor oder Debug installieren kann.</span><span class="sxs-lookup"><span data-stu-id="f907e-107">The following example shows how an application can install a function as a compressor or decompressor using the [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) function.</span></span>


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




