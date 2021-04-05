---
title: Iagentnotifysink-Lesezeichen
description: Iagentnotifysink-Lesezeichen
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709311"
---
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="cd851-103">Iagentnotifysink:: Bookmark</span><span class="sxs-lookup"><span data-stu-id="cd851-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="cd851-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="cd851-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="cd851-105">Benachrichtigt eine Client Anwendung, wenn Ihr Lesezeichen abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cd851-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="cd851-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cd851-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cd851-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwbookmarkid*</span><span class="sxs-lookup"><span data-stu-id="cd851-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="cd851-108">Der Bezeichner des Lesezeichens, das zum Auslösen des Ereignisses geführt hat.</span><span class="sxs-lookup"><span data-stu-id="cd851-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="cd851-109">Wenn Sie Lesezeichen Tags in eine [**Sprech**](speak-method.md) Methode einbeziehen, können Sie nachverfolgen, wann Sie mit diesem Ereignis auftreten.</span><span class="sxs-lookup"><span data-stu-id="cd851-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd851-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd851-110">See Also</span></span>

<span data-ttu-id="cd851-111">[**Iagentcharacter::**](iagentcharacter--speak.md)Speech, [Microsoft Agent Speech Output-Tags](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="cd851-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




