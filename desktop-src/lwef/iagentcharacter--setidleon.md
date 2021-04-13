---
title: Iagentcharacter-/tidleon
description: Iagentcharacter-/tidleon
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388805"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="e2594-103">Iagentcharacter::/tidleon</span><span class="sxs-lookup"><span data-stu-id="e2594-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="e2594-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e2594-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="e2594-105">Legt die automatische Leerlauf Verarbeitung für ein Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="e2594-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="e2594-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e2594-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e2594-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Böller*</span><span class="sxs-lookup"><span data-stu-id="e2594-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="e2594-108">Flag für Leerlauf Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e2594-108">Idle processing flag.</span></span> <span data-ttu-id="e2594-109">Wenn dieser Parameter **true** ist, spielt der Microsoft-Agent automatisch **idck** State-Animationen.</span><span class="sxs-lookup"><span data-stu-id="e2594-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="e2594-110">Der Server legt automatisch einen Timeout Wert fest, nachdem die letzte Animation für ein Zeichen wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e2594-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="e2594-111">Wenn das Intervall des Zeit Gebers abgelaufen ist, beginnt der Server mit den **idck** Zuständen für ein Zeichen, wobei die zugehörigen **idlinger** -Animationen in regelmäßigen Abständen abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="e2594-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="e2594-112">Wenn Sie die **idlinger** -Zustands Animationen selbst verwalten möchten, legen Sie die-Eigenschaft auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="e2594-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="e2594-113">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e2594-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2594-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2594-114">See Also</span></span>

[<span data-ttu-id="e2594-115">**Iagentcharacter:: getidleon**</span><span class="sxs-lookup"><span data-stu-id="e2594-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




