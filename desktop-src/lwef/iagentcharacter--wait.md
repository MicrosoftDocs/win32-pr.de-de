---
title: Iagentcharacter-Wartezeit
description: Iagentcharacter-Wartezeit
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310747"
---
# <a name="iagentcharacterwait"></a><span data-ttu-id="5fa75-103">Iagentcharacter:: Wait</span><span class="sxs-lookup"><span data-stu-id="5fa75-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="5fa75-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5fa75-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="5fa75-105">Enthält die Animations Warteschlange des Zeichens bei der angegebenen Animation (Anforderung), bis eine andere Anforderung für ein anderes Zeichen abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5fa75-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="5fa75-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5fa75-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5fa75-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*</span><span class="sxs-lookup"><span data-stu-id="5fa75-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5fa75-108">Die ID der Anforderung, auf die gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fa75-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="5fa75-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="5fa75-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5fa75-110">Adresse einer Variablen, die die **warte** Anforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="5fa75-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="5fa75-111">Verwenden Sie diese Methode nur, wenn Sie mehrere (gleichzeitige) Zeichen unterstützen und ihre Interaktion Sequenzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5fa75-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="5fa75-112">(Bei einem einzelnen Zeichen wird jede Animations Anforderung sequenziell wiedergegeben, nachdem die vorherige Anforderung abgeschlossen wurde.) Wenn Sie zwei Zeichen haben und möchten, dass die Animations Anforderung eines Zeichens wartet, bis die Animation des anderen Zeichens abgeschlossen ist, legen Sie die **Wait** -Methode auf die Animations Anforderungs-ID des anderen Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="5fa75-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




