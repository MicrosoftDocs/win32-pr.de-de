---
title: Iagentnotifysink im Leerlauf
description: Iagentnotifysink im Leerlauf
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339437"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="4d591-103">Iagentnotifysink:: Leerlauf</span><span class="sxs-lookup"><span data-stu-id="4d591-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="4d591-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4d591-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="4d591-105">Benachrichtigt eine Client Anwendung, wenn sich der **Leerlauf** Zustand eines Zeichens geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4d591-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="4d591-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4d591-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="4d591-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="4d591-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="4d591-108">Der Bezeichner der Anforderung, die gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4d591-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="4d591-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span><span class="sxs-lookup"><span data-stu-id="4d591-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="4d591-110">Startflag.</span><span class="sxs-lookup"><span data-stu-id="4d591-110">Start flag.</span></span> <span data-ttu-id="4d591-111">Dieser boolesche Wert ist **true** , wenn das Zeichen mit der Leerlaufzeit beginnt, und **false** , wenn es nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4d591-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="4d591-112">Mithilfe dieses Ereignisses können Sie nachverfolgen, wann der Microsoft-Agent-Server die Leerlauf Verarbeitung für ein Zeichen startet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="4d591-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d591-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d591-113">See Also</span></span>

<span data-ttu-id="4d591-114">[**Iagentcharacter:: getidleon**](iagentcharacter--getidleon.md), [ **iagentcharacter:: abtidleon**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="4d591-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




