---
title: Iagentnotifysink-Größe
description: Iagentnotifysink-Größe
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515908"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="74712-103">Iagentnotifysink:: size</span><span class="sxs-lookup"><span data-stu-id="74712-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="74712-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="74712-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="74712-105">Benachrichtigt eine Client Anwendung, wenn die Größe des Zeichens geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="74712-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="74712-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="74712-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="74712-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="74712-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="74712-108">Der Bezeichner des Zeichens, dessen Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="74712-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="74712-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lwidth*</span><span class="sxs-lookup"><span data-stu-id="74712-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="74712-110">Die Breite des Animations Rahmens des Zeichens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="74712-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="74712-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lheight*</span><span class="sxs-lookup"><span data-stu-id="74712-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="74712-112">Die Höhe des Animations Rahmens des Zeichens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="74712-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="74712-113">Dieses Ereignis wird an alle Clients des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="74712-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="74712-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74712-114">See Also</span></span>

<span data-ttu-id="74712-115">[**Iagentcharacter:: GetSize**](iagentcharacter--getsize.md), [ **iagentcharacter:: SetSize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="74712-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




