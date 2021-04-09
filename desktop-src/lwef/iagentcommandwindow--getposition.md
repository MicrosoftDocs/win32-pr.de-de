---
title: Iagentcommandwindow GetPosition
description: Iagentcommandwindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947802"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="707c3-103">Iagentcommandwindow:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="707c3-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="707c3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="707c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="707c3-105">Ruft die Position des sprach Befehls Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="707c3-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="707c3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="707c3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="707c3-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*</span><span class="sxs-lookup"><span data-stu-id="707c3-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="707c3-108">Adresse einer Variablen, die die Bildschirm Koordinate des linken Rands des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="707c3-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="707c3-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*</span><span class="sxs-lookup"><span data-stu-id="707c3-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="707c3-110">Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="707c3-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="707c3-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="707c3-111">See Also</span></span>

[<span data-ttu-id="707c3-112">**Iagentcommandwindow:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="707c3-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 




