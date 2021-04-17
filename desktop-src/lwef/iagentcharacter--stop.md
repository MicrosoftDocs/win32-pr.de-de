---
title: Iagentcharacter-Vorgang wird beendet
description: Iagentcharacter-Vorgang wird beendet
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388563"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="f0ee9-103">Iagentcharacter:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="f0ee9-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="f0ee9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f0ee9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="f0ee9-105">Beendet die angegebene Animation (Anforderung) und entfernt Sie aus der Animations Warteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f0ee9-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="f0ee9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f0ee9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f0ee9-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*</span><span class="sxs-lookup"><span data-stu-id="f0ee9-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f0ee9-108">Die ID der Anforderung, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ee9-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="f0ee9-109">**Stop** kann auch verwendet werden, um alle [**Vorbereitungs**](iagentcharacter--prepare.md) Aufrufe in der Warteschlange anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="f0ee9-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0ee9-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0ee9-110">See Also</span></span>

<span data-ttu-id="f0ee9-111">[**Iagentcharacter::P repare**](iagentcharacter--prepare.md), [ **iagentcharacter:: stopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="f0ee9-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




