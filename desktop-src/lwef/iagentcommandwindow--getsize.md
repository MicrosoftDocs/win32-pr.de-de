---
title: Iagentcommandwindow GetSize
description: Iagentcommandwindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341870"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="3bd37-103">Iagentcommandwindow:: GetSize</span><span class="sxs-lookup"><span data-stu-id="3bd37-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="3bd37-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3bd37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="3bd37-105">Ruft die aktuelle Größe des Sprachbefehle Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="3bd37-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="3bd37-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3bd37-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3bd37-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*</span><span class="sxs-lookup"><span data-stu-id="3bd37-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="3bd37-108">Adresse einer Variablen, die die Breite des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="3bd37-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="3bd37-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*</span><span class="sxs-lookup"><span data-stu-id="3bd37-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="3bd37-110">Adresse einer Variablen, die die Höhe des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.</span><span class="sxs-lookup"><span data-stu-id="3bd37-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3bd37-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3bd37-111">See Also</span></span>

[<span data-ttu-id="3bd37-112">**Iagentcommandwindow:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="3bd37-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 




