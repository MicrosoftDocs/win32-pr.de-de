---
title: Unterbrechung von iagentcharacter
description: Unterbrechung von iagentcharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948604"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="19965-103">Iagentcharacter:: Interrupt</span><span class="sxs-lookup"><span data-stu-id="19965-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="19965-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="19965-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="19965-105">Unterbricht die angegebene Animation (Anforderung) eines anderen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="19965-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="19965-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="19965-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="19965-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="19965-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="19965-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*</span><span class="sxs-lookup"><span data-stu-id="19965-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="19965-109">Eine ID der zu unterbrechenden Anforderung.</span><span class="sxs-lookup"><span data-stu-id="19965-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="19965-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="19965-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="19965-111">Adresse einer Variablen, die die **interruptanforderungs** -ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="19965-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="19965-112">Wenn Sie mehrere Zeichen laden, können Sie mit dieser Methode die Animation zwischen Zeichen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="19965-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="19965-113">Wenn sich z. b. ein anderes Zeichen in einer Schleifen Animation befindet, beendet diese Methode die Schleifen Animation und startet die nächste Animation in der Warteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="19965-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="19965-114">Der **Interrupt** stoppt die vorhandene Animation, aber die Animations Warteschlange des Zeichens wird nicht geleert.</span><span class="sxs-lookup"><span data-stu-id="19965-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="19965-115">Die nächste Animation wird in der Warteschlange des Zeichens gestartet.</span><span class="sxs-lookup"><span data-stu-id="19965-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="19965-116">Verwenden Sie die Stop-Methode, um die Warteschlange eines Zeichens [**anzuhalten**](/windows/desktop/lwef/iagentcharacter--stop) und zu leeren.</span><span class="sxs-lookup"><span data-stu-id="19965-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="19965-117">Sie können diese Methode nicht verwenden, um ein Zeichen selbst zu unterbrechen, da der Microsoft-Agent-Server die **Interrupt** -Methode in der Animations Warteschlange des Zeichens zur warte</span><span class="sxs-lookup"><span data-stu-id="19965-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="19965-118">Daher können Sie nur **Interrupt** verwenden, um die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.</span><span class="sxs-lookup"><span data-stu-id="19965-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 